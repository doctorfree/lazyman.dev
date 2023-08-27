---
layout: post
title: Lazyman Neovim Configuration Manager
toc: false
post_style: page
---

## Lazyman Neovim Configuration Manager

The [lazyman](https://lazyman.dev/info/lazyman_command.html) command
can be used to manage the Lazyman Neovim configuration.
The `lazyman` command calls `scripts/lazyman_config.sh` to
manage the Neovim configuration in `~/.config/lazyman/Lazyman`.

## Source for scripts/lazyman_config.sh

```bash
#!/usr/bin/env bash
#
# lazyman_config - configure the Lazyman Neovim configurations
#
# Written by Ronald Record <ronaldrecord@gmail.com>, Spring 2023
#
# shellcheck disable=SC1090,SC2001,SC2002,SC2016,SC2006,SC2086,SC2181,SC2129,SC2059,SC2076

LAZYMAN="nvim-Lazyman"
LMANDIR="${HOME}/.config/${LAZYMAN}"
NVIMCONF="${LMANDIR}/lua/configuration.lua"
CONFBACK="${LMANDIR}/lua/configuration-orig.lua"
GET_CONF="${LMANDIR}/scripts/get_conf.lua"
WEBDEV="${LMANDIR}/scripts/webdev_config.sh"
LZYIDE="${LMANDIR}/scripts/lzyide_config.sh"
FONTDIR="${LMANDIR}/scripts/figlet-fonts"
LOLCAT="lolcat"
BOLD=$(tput bold 2>/dev/null){:target="_blank"}{:rel="noopener noreferrer"}
NORM=$(tput sgr0 2>/dev/null){:target="_blank"}{:rel="noopener noreferrer"}

PLEASE="Please enter your choice"
USEGUI=
# Array with font names
fonts=("Slant" "Shadow" "Small" "Script" "Standard"){:target="_blank"}{:rel="noopener noreferrer"}
# Supported themes
themes=("nightfox" "tokyonight" "dracula" "kanagawa" "catppuccin" "tundra"
        "onedarkpro" "everforest" "monokai-pro"){:target="_blank"}{:rel="noopener noreferrer"}
# Themes with styles
styled_themes=("nightfox" "tokyonight" "dracula" "kanagawa" "catppuccin"
               "onedarkpro" "monokai-pro"){:target="_blank"}{:rel="noopener noreferrer"}

all_lsp_servers=("bashls" "cssmodules_ls" "denols" "dockerls" "eslint" "gopls"
                 "graphql" "html" "jdtls" "jsonls" "julials" "ltex" "lua_ls"
                 "marksman" "pylsp" "pyright" "sqlls" "tailwindcss" "texlab"
                 "tsserver" "vimls" "yamlls"){:target="_blank"}{:rel="noopener noreferrer"}
have_ccls=$(type -p ccls){:target="_blank"}{:rel="noopener noreferrer"}
[ "${have_ccls}" ] && all_lsp_servers+=("ccls"){:target="_blank"}{:rel="noopener noreferrer"}
have_clangd=$(type -p clangd){:target="_blank"}{:rel="noopener noreferrer"}
[ "${have_clangd}" ] && all_lsp_servers+=("clangd"){:target="_blank"}{:rel="noopener noreferrer"}

all_formatters=("actionlint" "goimports" "golangci-lint" "gofumpt"
                "google-java-format" "latexindent" "markdownlint"
                "prettier" "sql-formatter" "shellcheck" "shfmt"
                "stylua" "tflint" "yamllint"){:target="_blank"}{:rel="noopener noreferrer"}
have_beautysh=$(type -p beautysh){:target="_blank"}{:rel="noopener noreferrer"}
[ "${have_beautysh}" ] && all_formatters+=("beautysh"){:target="_blank"}{:rel="noopener noreferrer"}
have_black=$(type -p black){:target="_blank"}{:rel="noopener noreferrer"}
[ "${have_black}" ] && all_formatters+=("black"){:target="_blank"}{:rel="noopener noreferrer"}
have_ruff=$(type -p ruff){:target="_blank"}{:rel="noopener noreferrer"}
[ "${have_ruff}" ] && all_formatters+=("ruff"){:target="_blank"}{:rel="noopener noreferrer"}

lsp_enabled_table=(){:target="_blank"}{:rel="noopener noreferrer"}
for_enabled_table=(){:target="_blank"}{:rel="noopener noreferrer"}
neorg_notes_table=(){:target="_blank"}{:rel="noopener noreferrer"}

usage() {
  printf "\nUsage: lazyman_config [-d] [-i] [-m menu] [-s name value] [-u]"
  printf "\nWhere:"
  printf "\n    -d specifies debug mode"
  printf "\n    -i indicates initialize conditional plugin configurations and exit"
  printf "\n    -m 'menu' specifies the menu to display (conf, form, lsp, plugins)"
  printf "\n    -s 'name value' indicates set the value of configuration 'name' to 'value'"
  printf "\n    -u displays this usage message and exits"
  exit 1
}

prompt_continue() {
  printf "\nPress <Enter> to continue ... "
  read -r yn
}

set_haves() {
  have_fzf=$(type -p fzf){:target="_blank"}{:rel="noopener noreferrer"}
  have_figlet=$(type -p figlet){:target="_blank"}{:rel="noopener noreferrer"}
  have_lolcat=$(type -p lolcat){:target="_blank"}{:rel="noopener noreferrer"}
  have_rich=$(type -p rich){:target="_blank"}{:rel="noopener noreferrer"}
}

show_figlet() {
  if [ "$1" ]; then
    FIG_TEXT="$1"
  else
    FIG_TEXT="Lazyman"
  fi
  # Seed random generator
  RANDOM=$$$(date +%s){:target="_blank"}{:rel="noopener noreferrer"}
  USE_FONT=${fonts[$RANDOM % ${#fonts[@]}]}
  [ "${USE_FONT}" ] || USE_FONT="standard"
  if [ "${have_lolcat}" ]; then
    figlet -c -d "${FONTDIR}" -f "${USE_FONT}" -k -t ${FIG_TEXT} 2>/dev/null | ${LOLCAT}
  else
    figlet -c -d "${FONTDIR}" -f "${USE_FONT}" -k -t ${FIG_TEXT} 2>/dev/null
  fi
}

check_python_version() {
  have_python3=$(type -p python3){:target="_blank"}{:rel="noopener noreferrer"}
  [ "${have_python3}" ] || {
    echo "NO"
    return 3
  }
  major=$(python3 -c 'import sys; print(sys.version_info.major)'){:target="_blank"}{:rel="noopener noreferrer"}
  if [ ${major} -eq 3 ]
  then
    minor=$(python3 -c 'import sys; print(sys.version_info.minor)'){:target="_blank"}{:rel="noopener noreferrer"}
    if [ ${minor} -ge 9 ]
    then
      echo "OK"
      return 0
    else
      echo "NO"
      return 1
    fi
  else
    echo "NO"
    return 2
  fi
}

get_conf_table() {
  confname="$1"
  if [ "${confname}" == "lsp_servers" ]; then
    lsp_enabled_table=(){:target="_blank"}{:rel="noopener noreferrer"}
    while read -r val; do
      lsp_enabled_table+=("$val"){:target="_blank"}{:rel="noopener noreferrer"}
    done < <(NVIM_APPNAME="nvim-Lazyman" nvim -l ${GET_CONF} ${confname} 2>&1){:target="_blank"}{:rel="noopener noreferrer"}
    enable_ccls=$(get_conf_value enable_ccls){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_ccls}" == "true" ]; then
      lsp_enabled_table+=("ccls"){:target="_blank"}{:rel="noopener noreferrer"}
    fi
    enable_clangd=$(get_conf_value enable_clangd){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_clangd}" == "true" ]; then
      lsp_enabled_table+=("clangd"){:target="_blank"}{:rel="noopener noreferrer"}
    fi
  else
    if [ "${confname}" == "formatters_linters" ]; then
      for_enabled_table=(){:target="_blank"}{:rel="noopener noreferrer"}
      while read -r val; do
        for_enabled_table+=("$val"){:target="_blank"}{:rel="noopener noreferrer"}
      done < <(NVIM_APPNAME="nvim-Lazyman" nvim -l ${GET_CONF} ${confname} 2>&1){:target="_blank"}{:rel="noopener noreferrer"}
      while read -r val; do
        for_enabled_table+=("$val"){:target="_blank"}{:rel="noopener noreferrer"}
      done < <(NVIM_APPNAME="nvim-Lazyman" nvim -l ${GET_CONF} "external_formatters" 2>&1){:target="_blank"}{:rel="noopener noreferrer"}
    else
      if [ "${confname}" == "neorg_notes" ]; then
        neorg_notes_table=(){:target="_blank"}{:rel="noopener noreferrer"}
        while read -r val; do
          neorg_notes_table+=("$val"){:target="_blank"}{:rel="noopener noreferrer"}
        done < <(NVIM_APPNAME="nvim-Lazyman" nvim -l ${GET_CONF} ${confname} 2>&1){:target="_blank"}{:rel="noopener noreferrer"}
      fi
    fi
  fi
}

get_conf_value() {
  confname="$1"
  confval=$(NVIM_APPNAME="nvim-Lazyman" nvim -l ${GET_CONF} ${confname} 2>&1){:target="_blank"}{:rel="noopener noreferrer"}
  echo "${confval}"
}

set_conf_value() {
  confname="$1"
  confval="$2"
  grep "conf.${confname} =" "${NVIMCONF}" >/dev/null && {
    case ${confval} in
      true | false | [0-9]){:target="_blank"}{:rel="noopener noreferrer"}
        cat "${NVIMCONF}" \
          | sed -e "s/conf.${confname} =.*/conf.${confname} = ${confval}/" >/tmp/nvim$$
        ;;
      *){:target="_blank"}{:rel="noopener noreferrer"}
        cat "${NVIMCONF}" \
          | sed -e "s/conf.${confname} =.*/conf.${confname} = \"${confval}\"/" >/tmp/nvim$$
        ;;
    esac
    cp /tmp/nvim$$ "${NVIMCONF}"
    rm -f /tmp/nvim$$
  }
}

set_conf_table() {
  marker="$1"
  confval="$2"
  action="$3"
  case ${confval} in
    ccls){:target="_blank"}{:rel="noopener noreferrer"}
      case ${action} in
        disable){:target="_blank"}{:rel="noopener noreferrer"}
          set_conf_value "enable_ccls" "false"
          ;;
        enable){:target="_blank"}{:rel="noopener noreferrer"}
          set_conf_value "enable_ccls" "true"
          ;;
      esac
      ;;
    clangd){:target="_blank"}{:rel="noopener noreferrer"}
      case ${action} in
        disable){:target="_blank"}{:rel="noopener noreferrer"}
          set_conf_value "enable_clangd" "false"
          ;;
        enable){:target="_blank"}{:rel="noopener noreferrer"}
          set_conf_value "enable_clangd" "true"
          ;;
      esac
      ;;
    *){:target="_blank"}{:rel="noopener noreferrer"}
      grep "${marker}" "${NVIMCONF}" | grep "${confval}" >/dev/null && {
        case ${action} in
          disable){:target="_blank"}{:rel="noopener noreferrer"}
            cat "${NVIMCONF}" \
              | sed -E "s/  \"${confval}\",[[:space:]]+--[[:space:]]+${marker}/  -- \"${confval}\", -- ${marker}/" >/tmp/nvim$$
            ;;
          enable){:target="_blank"}{:rel="noopener noreferrer"}
            cat "${NVIMCONF}" \
              | sed -E "s/-- \"${confval}\",[[:space:]]+--[[:space:]]+${marker}/\"${confval}\", -- ${marker}/" >/tmp/nvim$$
            ;;
        esac
        cp /tmp/nvim$$ "${NVIMCONF}"
        rm -f /tmp/nvim$$
      }
      ;;
  esac
}

set_ranger_float() {
  have_ranger=$(type -p ranger){:target="_blank"}{:rel="noopener noreferrer"}
  [ "${have_ranger}" ] || {
    ranger_float=$(get_conf_value enable_ranger_float){:target="_blank"}{:rel="noopener noreferrer"}
    [ "${ranger_float}" == "true" ] && {
      set_conf_value "enable_ranger_float" "false"
    }
  }
}

set_waka_opt() {
  waka="false"
  [ -f "${HOME}"/.wakatime.cfg ] && {
    grep api_key "${HOME}"/.wakatime.cfg >/dev/null && waka="true"
  }
  set_conf_value "enable_wakatime" "${waka}"
}

set_code_explain() {
  if [ -f "${HOME}/.codeexplain/model.bin" ]; then
    pyver=$(check_python_version){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${pyver}" == "OK" ]
    then
      set_conf_value "enable_codeexplain" "true"
    else
      set_conf_value "enable_codeexplain" "false"
    fi
  else
    set_conf_value "enable_codeexplain" "false"
  fi
}

select_theme_style() {
  selected_style="${theme_style}"
  case "$1" in
    kanagawa){:target="_blank"}{:rel="noopener noreferrer"}
      styles=("wave" "dragon" "lotus"){:target="_blank"}{:rel="noopener noreferrer"}
      ;;
    tokyonight){:target="_blank"}{:rel="noopener noreferrer"}
      styles=("night" "storm" "day" "moon"){:target="_blank"}{:rel="noopener noreferrer"}
      ;;
    onedarkpro){:target="_blank"}{:rel="noopener noreferrer"}
      styles=("onedark" "onelight" "onedark_vivid" "onedark_dark"){:target="_blank"}{:rel="noopener noreferrer"}
      ;;
    catppuccin){:target="_blank"}{:rel="noopener noreferrer"}
      styles=("latte" "frappe" "macchiato" "mocha" "custom"){:target="_blank"}{:rel="noopener noreferrer"}
      ;;
    dracula){:target="_blank"}{:rel="noopener noreferrer"}
      styles=("blood" "magic" "soft" "default"){:target="_blank"}{:rel="noopener noreferrer"}
      ;;
    nightfox){:target="_blank"}{:rel="noopener noreferrer"}
      styles=("carbonfox" "dawnfox" "dayfox" "duskfox" "nightfox" "nordfox" "terafox"){:target="_blank"}{:rel="noopener noreferrer"}
      ;;
    monokai-pro){:target="_blank"}{:rel="noopener noreferrer"}
      styles=("classic" "octagon" "pro" "machine" "ristretto" "spectrum"){:target="_blank"}{:rel="noopener noreferrer"}
      ;;
    *){:target="_blank"}{:rel="noopener noreferrer"}
      styles=(){:target="_blank"}{:rel="noopener noreferrer"}
      ;;
  esac
  if [ "${have_fzf}" ]; then
    choice=$(printf "%s\n" "${styles[@]}" | fzf --prompt=" Neovim Theme Style  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
    [ "${choice}" == "${theme_style}" ] || {
      if [[ " ${styles[*]} " =~ " ${choice} " ]]; then
        set_conf_value "theme_style" "${choice}"
      fi
    }
  else
    set_haves
    while true; do
      confmenu=
      mainmenu=
      [ "$debug" ] || tput reset
      printf "\n"
      if [ "${have_rich}" ]; then
        rich "[cyan]Select Theme Style[/cyan]" -p -a rounded -c -C
      else
        [ "${have_figlet}" ] && show_figlet "Style"
      fi
      printf "\n"
      PS3="${BOLD}${PLEASE} (numeric or text, 'h' for help): ${NORM}"
      options=(){:target="_blank"}{:rel="noopener noreferrer"}
      for sty in "${styles[@]}"; do
        if [ "${theme_style}" == "$sty" ]; then
          options+=("$sty   "){:target="_blank"}{:rel="noopener noreferrer"}
        else
          options+=("$sty"){:target="_blank"}{:rel="noopener noreferrer"}
        fi
      done
      [ "${theme_style}" == "${selected_style}" ] || {
        options+=("Set style to ${theme_style}"){:target="_blank"}{:rel="noopener noreferrer"}
      }
      options+=("Configuration Menu" "Main Menu" "Quit"){:target="_blank"}{:rel="noopener noreferrer"}
      select opt in "${options[@]}"; do
        case "$opt,$REPLY" in
          "h",* | *,"h" | "H",* | *,"H" | "help",* | *,"help" | "Help",* | *,"Help"){:target="_blank"}{:rel="noopener noreferrer"}
            [ "$debug" ] || tput reset
            printf "\n"
            man lazyman
            break
            ;;
          "wave",* | *,"wave"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="wave"
            break
            ;;
          "dragon",* | *,"dragon"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="dragon"
            break
            ;;
          "lotus",* | *,"lotus"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="lotus"
            break
            ;;
          "night",* | *,"night"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="night"
            break
            ;;
          "storm",* | *,"storm"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="storm"
            break
            ;;
          "dayfox",* | *,"dayfox"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="dayfox"
            break
            ;;
          "day",* | *,"day"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="day"
            break
            ;;
          "moon",* | *,"moon"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="moon"
            break
            ;;
          "onedark",* | *,"onedark"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="onedark"
            break
            ;;
          "onelight",* | *,"onelight"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="onelight"
            break
            ;;
          "onedark_vivid",* | *,"onedark_vivid"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="onedark_vivid"
            break
            ;;
          "onedark_dark",* | *,"onedark_dark"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="onedark_dark"
            break
            ;;
          "latte",* | *,"latte"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="latte"
            break
            ;;
          "frappe",* | *,"frappe"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="frappe"
            break
            ;;
          "macchiato",* | *,"macchiato"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="macchiato"
            break
            ;;
          "mocha",* | *,"mocha"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="mocha"
            break
            ;;
          "custom",* | *,"custom"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="custom"
            break
            ;;
          "blood",* | *,"blood"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="blood"
            break
            ;;
          "magic",* | *,"magic"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="magic"
            break
            ;;
          "soft",* | *,"soft"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="soft"
            break
            ;;
          "default",* | *,"default"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="default"
            break
            ;;
          "carbonfox",* | *,"carbonfox"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="carbonfox"
            break
            ;;
          "dawnfox",* | *,"dawnfox"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="dawnfox"
            break
            ;;
          "duskfox",* | *,"duskfox"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="duskfox"
            break
            ;;
          "nightfox",* | *,"nightfox"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="nightfox"
            break
            ;;
          "nordfox",* | *,"nordfox"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="nordfox"
            break
            ;;
          "terafox",* | *,"terafox"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="terafox"
            break
            ;;
          "classic",* | *,"classic"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="classic"
            break
            ;;
          "octagon",* | *,"octagon"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="octagon"
            break
            ;;
          "pro",* | *,"pro"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="pro"
            break
            ;;
          "machine",* | *,"machine"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="machine"
            break
            ;;
          "ristretto",* | *,"ristretto"){:target="_blank"}{:rel="noopener noreferrer"}
            theme_style="ristretto"
            break
            ;;
          "Set style to"*,* | *,"Set style to"*){:target="_blank"}{:rel="noopener noreferrer"}
            set_conf_value "theme_style" "${theme_style}"
            break 2
            ;;
          "Configuration Menu"*,* | *,"Configuration Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
            confmenu=1
            break 2
            ;;
          "Main Menu"*,* | *,"Main Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
            [ "${pluginit}" ] && lazyman -N nvim-Lazyman init
            mainmenu=1
            break 2
            ;;
          "Quit"*,* | *,"Quit"* | "quit"*,* | *,"quit"*){:target="_blank"}{:rel="noopener noreferrer"}
            [ "${pluginit}" ] && lazyman -N nvim-Lazyman init
            printf "\nExiting Lazyman Configuration Menu System\n\n"
            exit 3
            ;;
        esac
        REPLY=
      done
    done
    [ "${confmenu}" ] && show_conf_menu
    [ "${mainmenu}" ] && exit 2
  fi
}

set_default_style() {
  case "$1" in
    kanagawa){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "theme_style" "dragon"
      ;;
    tokyonight){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "theme_style" "moon"
      ;;
    onedarkpro){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "theme_style" "onedark_dark"
      ;;
    catppuccin){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "theme_style" "mocha"
      ;;
    dracula){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "theme_style" "soft"
      ;;
    nightfox){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "theme_style" "carbonfox"
      ;;
    monokai-pro){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "theme_style" "pro"
      ;;
    *){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "theme_style" "none"
      ;;
  esac
}

select_theme() {
  selected_theme="$1"
  if [ "${have_fzf}" ]; then
    theme=$(printf "%s\n" "${themes[@]}" | fzf --prompt=" Neovim Theme  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
    [ "${theme}" == "${selected_theme}" ] || {
      if [[ " ${themes[*]} " =~ " ${theme} " ]]; then
        set_conf_value "theme" "${theme}"
        set_default_style "${theme}"
      fi
    }
  else
    set_haves
    while true; do
      confmenu=
      mainmenu=
      [ "$debug" ] || tput reset
      printf "\n"
      if [ "${have_rich}" ]; then
        rich "[cyan]Select Theme[/cyan]" -p -a rounded -c -C
      else
        [ "${have_figlet}" ] && show_figlet "Theme"
      fi
      printf "\n"
      PS3="${BOLD}${PLEASE} (numeric or text, 'h' for help): ${NORM}"
      options=(){:target="_blank"}{:rel="noopener noreferrer"}
      for thm in "${themes[@]}"; do
        if [ "${theme}" == "$thm" ]; then
          options+=("$thm   "){:target="_blank"}{:rel="noopener noreferrer"}
        else
          options+=("$thm"){:target="_blank"}{:rel="noopener noreferrer"}
        fi
      done
      [ "${theme}" == "${selected_theme}" ] || {
        options+=("Set theme to ${theme}"){:target="_blank"}{:rel="noopener noreferrer"}
      }
      options+=("Configuration Menu" "Main Menu" "Quit"){:target="_blank"}{:rel="noopener noreferrer"}
      select opt in "${options[@]}"; do
        case "$opt,$REPLY" in
          "h",* | *,"h" | "H",* | *,"H" | "help",* | *,"help" | "Help",* | *,"Help"){:target="_blank"}{:rel="noopener noreferrer"}
            [ "$debug" ] || tput reset
            printf "\n"
            man lazyman
            break
            ;;
          "nightfox"*,* | *,"nightfox"*){:target="_blank"}{:rel="noopener noreferrer"}
            theme="nightfox"
            break
            ;;
          "tokyonight"*,* | *,"tokyonight"*){:target="_blank"}{:rel="noopener noreferrer"}
            theme="tokyonight"
            break
            ;;
          "dracula"*,* | *,"dracula"*){:target="_blank"}{:rel="noopener noreferrer"}
            theme="dracula"
            break
            ;;
          "kanagawa"*,* | *,"kanagawa"*){:target="_blank"}{:rel="noopener noreferrer"}
            theme="kanagawa"
            break
            ;;
          "catppuccin"*,* | *,"catppuccin"*){:target="_blank"}{:rel="noopener noreferrer"}
            theme="catppuccin"
            break
            ;;
          "tundra"*,* | *,"tundra"*){:target="_blank"}{:rel="noopener noreferrer"}
            theme="tundra"
            break
            ;;
          "onedarkpro"*,* | *,"onedarkpro"*){:target="_blank"}{:rel="noopener noreferrer"}
            theme="onedarkpro"
            break
            ;;
          "everforest"*,* | *,"everforest"*){:target="_blank"}{:rel="noopener noreferrer"}
            theme="everforest"
            break
            ;;
          "monokai-pro"*,* | *,"monokai-pro"*){:target="_blank"}{:rel="noopener noreferrer"}
            theme="monokai-pro"
            break
            ;;
          "Set theme to"*,* | *,"Set theme to"*){:target="_blank"}{:rel="noopener noreferrer"}
            set_conf_value "theme" "${theme}"
            set_default_style "${theme}"
            break 2
            ;;
          "Configuration Menu"*,* | *,"Configuration Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
            confmenu=1
            break 2
            ;;
          "Main Menu"*,* | *,"Main Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
            [ "${pluginit}" ] && lazyman -N nvim-Lazyman init
            mainmenu=1
            break 2
            ;;
          "Quit",* | *,"Quit" | "quit",* | *,"quit"){:target="_blank"}{:rel="noopener noreferrer"}
            [ "${pluginit}" ] && lazyman -N nvim-Lazyman init
            printf "\nExiting Lazyman Configuration Menu System\n\n"
            exit 3
            ;;
        esac
        REPLY=
      done
    done
  fi
  [ "${confmenu}" ] && show_conf_menu
  [ "${mainmenu}" ] && exit 2
}

show_plug_help() {
  if [ "${have_rich}" ]; then
    rich "[cyan]Lazyman Plugins Menu Help[/cyan]" -p -a rounded -c -C
  else
    printf "\n\tLazyman Plugins Menu Help\n"
  fi
  printf "\nEnable and disable installed Neovim plugins and plugin configuration."
  printf "\nEnabled plugins and plugin configurations are indicated with a []"
  printf "\nDisabled plugins and plugin configurations are indicated with a [✗]\n"
  printf "\nSettings in this menu only effect the Lazyman Neovim configuration in:"
  printf "\n\t${HOME}/.config/lazyman/Lazyman\n"
  prompt_continue
}

show_plugin_menu() {
  set_haves
  while true; do
    mainmenu=
    confmenu=
    lspmenu=
    formenu=
    [ -f ${GET_CONF} ] || {
      printf "\n\nWARNING: missing ${GET_CONF}"
      printf "\nUnable to modify configuration from this menu"
      printf "\nYou may need to update or re-install Lazyman"
      prompt_continue
      mainmenu=1
      break
    }
    [ "$debug" ] || tput reset
    if [ "${have_rich}" ]; then
      rich "[b cyan]Lazyman Plugins Configuration Menu[/]" -p -a rounded -c -C
      rich "[b green]Manage the Neovim plugins enabled in[/] [b yellow]~/.config/lazyman/Lazyman[/]" -p -c
    else
      [ "${have_figlet}" ] && show_figlet "Plugins"
    fi
    printf '\n'
    namespace=$(get_conf_value namespace){:target="_blank"}{:rel="noopener noreferrer"}
    use_namespace="${namespace}"
    media_backend=$(get_conf_value media_backend){:target="_blank"}{:rel="noopener noreferrer"}
    use_media_backend="${media_backend}"
    session_manager=$(get_conf_value session_manager){:target="_blank"}{:rel="noopener noreferrer"}
    use_session_manager="${session_manager}"
    file_tree=$(get_conf_value file_tree){:target="_blank"}{:rel="noopener noreferrer"}
    use_neotree="${file_tree}"
    enable_noice=$(get_conf_value enable_noice){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_noice}" == "true" ]; then
      use_noice=""
    else
      use_noice="✗"
    fi
    enable_chatgpt=$(get_conf_value enable_chatgpt){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_chatgpt}" == "true" ]; then
      use_chatgpt=""
    else
      use_chatgpt="✗"
    fi
    enable_codeexplain=$(get_conf_value enable_codeexplain){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_codeexplain}" == "true" ]; then
      use_codeexplain=""
    else
      use_codeexplain="✗"
    fi
    enable_codeium=$(get_conf_value enable_codeium){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_codeium}" == "true" ]; then
      use_codeium=""
    else
      use_codeium="✗"
    fi
    enable_copilot=$(get_conf_value enable_copilot){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_copilot}" == "true" ]; then
      use_copilot=""
    else
      use_copilot="✗"
    fi
    enable_neoai=$(get_conf_value enable_neoai){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_neoai}" == "true" ]; then
      use_neoai=""
    else
      use_neoai="✗"
    fi
    enable_surround=$(get_conf_value enable_surround){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_surround}" == "true" ]; then
      use_surround=""
    else
      use_surround="✗"
    fi
    lualine_style=$(get_conf_value lualine_style){:target="_blank"}{:rel="noopener noreferrer"}
    use_lualine_style="${lualine_style}"
    lualine_separator=$(get_conf_value lualine_separator){:target="_blank"}{:rel="noopener noreferrer"}
    use_lualine_separator="${lualine_separator}"
    enable_fancy=$(get_conf_value enable_fancy){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_fancy}" == "true" ]; then
      use_fancy=""
    else
      use_fancy="✗"
    fi
    enable_wilder=$(get_conf_value enable_wilder){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_wilder}" == "true" ]; then
      use_wilder=""
    else
      use_wilder="✗"
    fi
    enable_lualine_lsp_progress=$(get_conf_value enable_lualine_lsp_progress){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_lualine_lsp_progress}" == "true" ]; then
      use_lualine_lsp_progress=""
    else
      use_lualine_lsp_progress="✗"
    fi
    enable_terminal=$(get_conf_value enable_terminal){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_terminal}" == "true" ]; then
      use_terminal=""
    else
      use_terminal="✗"
    fi
    enable_toggleterm=$(get_conf_value enable_toggleterm){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_toggleterm}" == "true" ]; then
      use_toggleterm=""
    else
      use_toggleterm="✗"
    fi
    enable_neotest=$(get_conf_value enable_neotest){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_neotest}" == "true" ]; then
      use_neotest=""
    else
      use_neotest="✗"
    fi
    enable_wakatime=$(get_conf_value enable_wakatime){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_wakatime}" == "true" ]; then
      use_wakatime=""
    else
      use_wakatime="✗"
    fi
    enable_asciiart=$(get_conf_value enable_asciiart){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_asciiart}" == "true" ]; then
      use_asciiart=""
    else
      use_asciiart="✗"
    fi
    enable_cheatsheet=$(get_conf_value enable_cheatsheet){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_cheatsheet}" == "true" ]; then
      use_cheatsheet=""
    else
      use_cheatsheet="✗"
    fi
    enable_motion=$(get_conf_value enable_motion){:target="_blank"}{:rel="noopener noreferrer"}
    use_motion="${enable_motion}"
    enable_notes=$(get_conf_value enable_notes){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_notes}" == "true" ]; then
      use_notes=""
    else
      use_notes="✗"
    fi
    markdown_preview=$(get_conf_value markdown_preview){:target="_blank"}{:rel="noopener noreferrer"}
    use_markdown_preview="${markdown_preview}"
    enable_obsidian=$(get_conf_value enable_obsidian){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_obsidian}" == "true" ]; then
      use_obsidian=""
    else
      use_obsidian="✗"
    fi
    obsidian_vault=$(get_conf_value obsidian_vault){:target="_blank"}{:rel="noopener noreferrer"}
    use_obsidian_vault=$(basename "${obsidian_vault}"){:target="_blank"}{:rel="noopener noreferrer"}
    get_conf_table neorg_notes
    num_neorg_notes=${#neorg_notes_table[@]}
    enable_ranger=$(get_conf_value enable_ranger_float){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_ranger}" == "true" ]; then
      use_ranger=""
    else
      use_ranger="✗"
    fi
    enable_coding=$(get_conf_value enable_coding){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_coding}" == "true" ]; then
      use_coding=""
    else
      use_coding="✗"
    fi
    enable_compile=$(get_conf_value enable_compile){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_compile}" == "true" ]; then
      use_compile=""
    else
      use_compile="✗"
    fi
    enable_bbye=$(get_conf_value enable_bbye){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_bbye}" == "true" ]; then
      use_bbye=""
    else
      use_bbye="✗"
    fi
    enable_startuptime=$(get_conf_value enable_startuptime){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_startuptime}" == "true" ]; then
      use_startuptime=""
    else
      use_startuptime="✗"
    fi
    enable_dressing=$(get_conf_value enable_dressing){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_dressing}" == "true" ]; then
      use_dressing=""
    else
      use_dressing="✗"
    fi
    enable_games=$(get_conf_value enable_games){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_games}" == "true" ]; then
      use_games=""
    else
      use_games="✗"
    fi
    enable_multi_cursor=$(get_conf_value enable_multi_cursor){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_multi_cursor}" == "true" ]; then
      use_multi_cursor=""
    else
      use_multi_cursor="✗"
    fi
    enable_renamer=$(get_conf_value enable_renamer){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_renamer}" == "true" ]; then
      use_renamer=""
    else
      use_renamer="✗"
    fi
    use_dash=$(get_conf_value dashboard){:target="_blank"}{:rel="noopener noreferrer"}
    enable_bookmarks=$(get_conf_value enable_bookmarks){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_bookmarks}" == "true" ]; then
      use_bookmarks=""
    else
      use_bookmarks="✗"
    fi
    enable_ide=$(get_conf_value enable_ide){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_ide}" == "true" ]; then
      use_ide=""
    else
      use_ide="✗"
    fi
    enable_navigator=$(get_conf_value enable_navigator){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_navigator}" == "true" ]; then
      use_navigator=""
    else
      use_navigator="✗"
    fi
    enable_project=$(get_conf_value enable_project){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_project}" == "true" ]; then
      use_project=""
    else
      use_project="✗"
    fi
    enable_picker=$(get_conf_value enable_picker){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_picker}" == "true" ]; then
      use_picker=""
    else
      use_picker="✗"
    fi
    enable_smooth_scrolling=$(get_conf_value enable_smooth_scrolling){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_smooth_scrolling}" == "true" ]; then
      use_smooth_scrolling=""
    else
      use_smooth_scrolling="✗"
    fi
    enable_securitree=$(get_conf_value enable_securitree){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_securitree}" == "true" ]; then
      use_securitree=""
    else
      use_securitree="✗"
    fi
    dashboard_recent_files=$(get_conf_value dashboard_recent_files){:target="_blank"}{:rel="noopener noreferrer"}
    use_dashboard_recent_files="${dashboard_recent_files}"
    enable_dashboard_header=$(get_conf_value enable_dashboard_header){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_dashboard_header}" == "true" ]; then
      use_dashboard_header=""
    else
      use_dashboard_header="✗"
    fi
    enable_dashboard_quick_links=$(get_conf_value enable_dashboard_quick_links){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_dashboard_quick_links}" == "true" ]; then
      use_dashboard_quick_links=""
    else
      use_dashboard_quick_links="✗"
    fi
    enable_screensaver=$(get_conf_value enable_screensaver){:target="_blank"}{:rel="noopener noreferrer"}
    use_screensaver="${enable_screensaver}"
    screensaver_timeout=$(get_conf_value screensaver_timeout){:target="_blank"}{:rel="noopener noreferrer"}
    use_timeout="${screensaver_timeout}"
    indentline_style=$(get_conf_value indentline_style){:target="_blank"}{:rel="noopener noreferrer"}
    use_indentline="${indentline_style}"
    PS3="${BOLD}${PLEASE} (numeric or text, 'h' for help): ${NORM}"
    options=(){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Ascii Art     [${use_asciiart}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Bdelete cmd   [${use_bbye}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Bookmarks     [${use_bookmarks}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("ChatGPT (AI)  [${use_chatgpt}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Codeium (AI)  [${use_codeium}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Copilot (AI)  [${use_copilot}]"){:target="_blank"}{:rel="noopener noreferrer"}
    pyver=$(check_python_version){:target="_blank"}{:rel="noopener noreferrer"}
    [ "${pyver}" == "OK" ] && {
      options+=("GPT4ALL (AI)  [${use_codeexplain}]"){:target="_blank"}{:rel="noopener noreferrer"}
    }
    [ -f "${HOME}/.codeexplain/model.bin" ] && {
      options+=(" Remove GPT model"){:target="_blank"}{:rel="noopener noreferrer"}
    }
    options+=("NeoAI   (AI)  [${use_neoai}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Cheatsheets   [${use_cheatsheet}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Enable coding [${use_coding}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Compile & Run [${use_compile}]"){:target="_blank"}{:rel="noopener noreferrer"}
    [ "${use_namespace}" == "free" ] && {
      options+=("Dashboard [${use_dash}]"){:target="_blank"}{:rel="noopener noreferrer"}
      if [ "${use_dash}" == "alpha" ]; then
        options+=(" Alpha Header [${use_dashboard_header}]"){:target="_blank"}{:rel="noopener noreferrer"}
        options+=(" Recent Files [${use_dashboard_recent_files}]"){:target="_blank"}{:rel="noopener noreferrer"}
        options+=(" Quick Links  [${use_dashboard_quick_links}]"){:target="_blank"}{:rel="noopener noreferrer"}
      fi
    }
    options+=("Dressing UI   [${use_dressing}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("File Tree [${use_neotree}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Enable Games  [${use_games}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Enable IDE    [${use_ide}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Indentline [${use_indentline}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Lualine Style [${use_lualine_style}]"){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${use_lualine_style}" == "onno" ]; then
      options+=(" Separator    [${use_lualine_separator}]"){:target="_blank"}{:rel="noopener noreferrer"}
    fi
    options+=(" Fancy Icons  [${use_fancy}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Enable Motion [${use_motion}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Enable Notes  [${use_notes}]"){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_notes}" == "true" ]; then
      options+=("Enable Obsidian [${use_obsidian}]"){:target="_blank"}{:rel="noopener noreferrer"}
      options+=(" Preview  [${use_markdown_preview}]"){:target="_blank"}{:rel="noopener noreferrer"}
      [ "${enable_obsidian}" == "true" ] && {
        options+=(" Obsidian [${use_obsidian_vault}]"){:target="_blank"}{:rel="noopener noreferrer"}
      }
      [ ${num_neorg_notes} -lt 4 ] && {
        options+=(" Neorg Notes  [add]"){:target="_blank"}{:rel="noopener noreferrer"}
      }
    fi
    options+=("Media Backend [${use_media_backend}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Multi Cursor  [${use_multi_cursor}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Navigator     [${use_navigator}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Noice UI      [${use_noice}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Picker        [${use_picker}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Project       [${use_project}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Enable Ranger [${use_ranger}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Enable Rename [${use_renamer}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Screensaver [${use_screensaver}]"){:target="_blank"}{:rel="noopener noreferrer"}
    [ "${use_screensaver}" == "none" ] || {
      options+=(" Timeout    [${use_timeout}]"){:target="_blank"}{:rel="noopener noreferrer"}
    }
    options+=("Securitree    [${use_securitree}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Session [${use_session_manager}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Smooth Scroll [${use_smooth_scrolling}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("StartupTime   [${use_startuptime}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Surround      [${use_surround}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Terminal      [${use_terminal}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Toggle Term   [${use_toggleterm}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Enable Tests  [${use_neotest}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("WakaTime      [${use_wakatime}]"){:target="_blank"}{:rel="noopener noreferrer"}
    [ "${use_namespace}" == "free" ] && {
      options+=("Wilder Menus  [${use_wilder}]"){:target="_blank"}{:rel="noopener noreferrer"}
    }
    options+=("Winbar LSP    [${use_lualine_lsp_progress}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Disable All"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Enable All"){:target="_blank"}{:rel="noopener noreferrer"}
    [ -f ${CONFBACK} ] && {
      diff ${CONFBACK} ${NVIMCONF} >/dev/null || options+=("Reset to Defaults"){:target="_blank"}{:rel="noopener noreferrer"}
    }
    [ -d "${LMANDIR}" ] && options+=("Open Lazyman"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Formatters"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("LSP Servers"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Config Menu"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Main Menu"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Quit"){:target="_blank"}{:rel="noopener noreferrer"}
    select opt in "${options[@]}"; do
      case "$opt,$REPLY" in
        "h",* | *,"h" | "H",* | *,"H" | "help",* | *,"help" | "Help",* | *,"Help"){:target="_blank"}{:rel="noopener noreferrer"}
          [ "$debug" ] || tput reset
          show_plug_help
          break
          ;;
        "Media"*,* | *,"Media"*){:target="_blank"}{:rel="noopener noreferrer"}
          choices=("none" "catimg" "chafa" "jp2a" "ueberzug" "viu"){:target="_blank"}{:rel="noopener noreferrer"}
          choice=$(printf "%s\n" "${choices[@]}" | fzf --prompt=" Telescope Media Backend  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
          if [[ " ${choices[*]} " =~ " ${choice} " ]]; then
            set_conf_value "media_backend" "${choice}"
            pluginit=1
          fi
          break
          ;;
        " Neorg Note"*,* | *," Neorg Note"*){:target="_blank"}{:rel="noopener noreferrer"}
          printf "\n\nCurrent Neorg notes location(s):"
          for notedir in "${neorg_notes_table[@]}"; do
            printf "\n\t$notedir"
          done
          printf "\nEnter the full pathname to a new Neorg notes folder."
          printf "\nPress <Enter> to continue using existing folder(s).\n"
          while true; do
            read -r -p "Neorg notes location: " notes
            case $notes in
              ""){:target="_blank"}{:rel="noopener noreferrer"}
                break
                ;;
              *){:target="_blank"}{:rel="noopener noreferrer"}
                if [ -d "${notes}" ]
                then
                  case ${num_neorg_notes} in
                    0|1){:target="_blank"}{:rel="noopener noreferrer"}
                      neorg_temp="XXXXX"
                      ;;
                    2){:target="_blank"}{:rel="noopener noreferrer"}
                      neorg_temp="YYYYY"
                      ;;
                    3){:target="_blank"}{:rel="noopener noreferrer"}
                      neorg_temp="ZZZZZ"
                      ;;
                    *){:target="_blank"}{:rel="noopener noreferrer"}
                      neorg_temp=
                      ;;
                  esac
                  [ "${neorg_temp}" ] && {
                    cat "${NVIMCONF}" \
                      | sed -e "s/${neorg_temp}/${notes}/" >/tmp/nvim$$
                    cp /tmp/nvim$$ "${NVIMCONF}"
                    rm -f /tmp/nvim$$
                    set_conf_table "NEORG_NOTES" "${notes}" "enable"
                  }
                  break
                else
                  printf "\n${notes} does not exist or is not a directory."
                  printf "\nEnter the full path to a Neorg notes folder, or"
                  printf "\npress <Enter> to retain the current setting.\n"
                fi
                ;;
            esac
          done
          break
          ;;
        " Obsidian"*,* | *," Obsidian"*){:target="_blank"}{:rel="noopener noreferrer"}
          printf "\n\nCurrent Obsidian Vault location: ${obsidian_vault}"
          printf "\nEnter the full pathname to the Obsidian vault."
          printf "\nPress <Enter> to continue using existing vault.\n"
          while true; do
            read -r -p "Obsidian vault location: " vault
            case $vault in
              ""){:target="_blank"}{:rel="noopener noreferrer"}
                break
                ;;
              *){:target="_blank"}{:rel="noopener noreferrer"}
                if [ -d "${vault}" ]
                then
                  set_conf_value "obsidian_vault" "${vault}"
                  break
                else
                  printf "\n${vault} does not exist or is not a directory."
                  printf "\nEnter the full path to an Obsidian folder, or"
                  printf "\npress <Enter> to retain the current setting.\n"
                fi
                ;;
            esac
          done
          break
          ;;
        " Preview"*,* | *," Preview"*){:target="_blank"}{:rel="noopener noreferrer"}
          choices=("Preview" "Peek" "None"){:target="_blank"}{:rel="noopener noreferrer"}
          choice=$(printf "%s\n" "${choices[@]}" | fzf --prompt=" Select Markdown Preview  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
          if [[ " ${choices[*]} " =~ " ${choice} " ]]; then
            if [ "${choice}" == "Preview" ]; then
              set_conf_value "markdown_preview" "preview"
            else
              if [ "${choice}" == "Peek" ]; then
                set_conf_value "markdown_preview" "peek"
              else
                if [ "${choice}" == "None" ]; then
                  set_conf_value "markdown_preview" "none"
                fi
              fi
            fi
            pluginit=1
          fi
          break
          ;;
        "Session"*,* | *,"Session"*){:target="_blank"}{:rel="noopener noreferrer"}
          choices=("Persistence" "Possession" "None"){:target="_blank"}{:rel="noopener noreferrer"}
          choice=$(printf "%s\n" "${choices[@]}" | fzf --prompt=" Neovim Session Manager  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
          if [[ " ${choices[*]} " =~ " ${choice} " ]]; then
            if [ "${choice}" == "Possession" ]; then
              set_conf_value "session_manager" "possession"
            else
              if [ "${choice}" == "Persistence" ]; then
                set_conf_value "session_manager" "persistence"
              else
                if [ "${choice}" == "None" ]; then
                  set_conf_value "session_manager" "none"
                fi
              fi
            fi
            pluginit=1
          fi
          break
          ;;
        "File"*,* | *,"File"*){:target="_blank"}{:rel="noopener noreferrer"}
          choices=("Neotree" "Nvimtree" "None"){:target="_blank"}{:rel="noopener noreferrer"}
          choice=$(printf "%s\n" "${choices[@]}" | fzf --prompt=" Neovim File Tree  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
          if [[ " ${choices[*]} " =~ " ${choice} " ]]; then
            if [ "${choice}" == "Neotree" ]; then
              set_conf_value "file_tree" "neo-tree"
            else
              if [ "${choice}" == "Nvimtree" ]; then
                set_conf_value "file_tree" "nvim-tree"
              else
                if [ "${choice}" == "None" ]; then
                  set_conf_value "file_tree" "none"
                fi
              fi
            fi
            pluginit=1
          fi
          break
          ;;
        "Noice"*,* | *,"Noice"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_noice}" == "true" ]; then
            set_conf_value "enable_noice" "false"
          else
            set_conf_value "enable_noice" "true"
          fi
          pluginit=1
          break
          ;;
        "ChatGPT"*,* | *,"ChatGPT"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_chatgpt}" == "true" ]; then
            set_conf_value "enable_chatgpt" "false"
            pluginit=1
          else
            if [ "$OPENAI_API_KEY" ]; then
              set_conf_value "enable_chatgpt" "true"
              pluginit=1
            else
              printf "\nThe OPENAI_API_KEY environment variable must be set"
              printf "\nbefore enabling the ChatGPT plugin."
              prompt_continue
            fi
          fi
          break
          ;;
        "Codeium"*,* | *,"Codeium"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_codeium}" == "true" ]; then
            set_conf_value "enable_codeium" "false"
          else
            set_conf_value "enable_codeium" "true"
          fi
          pluginit=1
          break
          ;;
        "Copilot"*,* | *,"Copilot"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_copilot}" == "true" ]; then
            set_conf_value "enable_copilot" "false"
          else
            set_conf_value "enable_copilot" "true"
          fi
          pluginit=1
          break
          ;;
        " Remove GPT"*,* | *," Remove GPT"*){:target="_blank"}{:rel="noopener noreferrer"}
          rm -f "${HOME}/.codeexplain/model.bin"
          for models in "${HOME}"/.codeexplain/*
          do
            [ "${models}" == "${HOME}/.codeexplain/*" ] && {
              rmdir "${HOME}/.codeexplain"
            }
          done
          set_conf_value "enable_codeexplain" "false"
          pluginit=1
          break
          ;;
        "GPT4ALL"*,* | *,"GPT4ALL"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_codeexplain}" == "true" ]; then
            set_conf_value "enable_codeexplain" "false"
          else
            if [ -f "${HOME}/.codeexplain/model.bin" ]; then
              set_conf_value "enable_codeexplain" "true"
            else
              [ -x ${LMANDIR}/scripts/gpt4all.sh ] || {
                printf "\n${LMANDIR}/scripts/gpt4all.sh not executable"
                printf "\nUnable to enable the codeexplain.nvim plugin."
                printf "\nPlease check the Lazyman installation."
                prompt_continue
              }
              printf "\nThe GPT4ALL model must be downloaded before"
              printf "\nenabling the codeexplain.nvim GPT4ALL plugin."
              printf "\nThe model is nearly 4GB in ${HOME}/.codeexplain/."
              printf "\nWould you like to download the GPT4ALL model?\n"
              while true; do
                read -r -p "Download GPT4ALL model (no API key required) ? (y/n) " yn
                case $yn in
                  [Yy]*){:target="_blank"}{:rel="noopener noreferrer"}
                    printf "\nDownloading large file, please be patient ..."
                    ${LMANDIR}/scripts/gpt4all.sh
                    if [ -f "${HOME}/.codeexplain/model.bin" ]; then
                      printf " done\n"
                      set_conf_value "enable_codeexplain" "true"
                    else
                      printf "\nDownload failed. Unable to enable plugin."
                      prompt_continue
                    fi
                    break
                    ;;
                  [Nn]*){:target="_blank"}{:rel="noopener noreferrer"}
                    break
                    ;;
                  *){:target="_blank"}{:rel="noopener noreferrer"}
                    printf "\nPlease answer yes or no.\n"
                    ;;
                esac
              done
            fi
          fi
          pluginit=1
          break
          ;;
        "NeoAI"*,* | *,"NeoAI"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_neoai}" == "true" ]; then
            set_conf_value "enable_neoai" "false"
            pluginit=1
          else
            if [ "$OPENAI_API_KEY" ]; then
              set_conf_value "enable_neoai" "true"
              pluginit=1
            else
              printf "\nThe OPENAI_API_KEY environment variable must be set"
              printf "\nbefore enabling the NeoAI plugin."
              prompt_continue
            fi
          fi
          break
          ;;
        "Surround"*,* | *,"Surround"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_surround}" == "true" ]; then
            set_conf_value "enable_surround" "false"
          else
            set_conf_value "enable_surround" "true"
          fi
          pluginit=1
          break
          ;;
        "Lualine Style"*,* | *,"Lualine Style"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${use_lualine_style}" == "free" ]; then
            set_conf_value "lualine_style" "onno"
          else
            set_conf_value "lualine_style" "free"
          fi
          pluginit=1
          break
          ;;
        " Separator"*,* | *," Separator"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${use_lualine_separator}" == "bubble" ]; then
            set_conf_value "lualine_separator" "arrow"
          else
            set_conf_value "lualine_separator" "bubble"
          fi
          pluginit=1
          break
          ;;
        " Fancy"*,* | *," Fancy"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_fancy}" == "true" ]; then
            set_conf_value "enable_fancy" "false"
          else
            set_conf_value "enable_fancy" "true"
          fi
          pluginit=1
          break
          ;;
        "Wilder"*,* | *,"Wilder"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_wilder}" == "true" ]; then
            set_conf_value "enable_wilder" "false"
          else
            set_conf_value "enable_wilder" "true"
          fi
          pluginit=1
          break
          ;;
        "Winbar LSP"*,* | *,"Winbar LSP"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_lualine_lsp_progress}" == "true" ]; then
            set_conf_value "enable_lualine_lsp_progress" "false"
          else
            set_conf_value "enable_lualine_lsp_progress" "true"
          fi
          pluginit=1
          break
          ;;
        "Terminal"*,* | *,"Terminal"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_terminal}" == "true" ]; then
            set_conf_value "enable_terminal" "false"
          else
            set_conf_value "enable_terminal" "true"
          fi
          pluginit=1
          break
          ;;
        "Toggle Term"*,* | *,"Toggle Term"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_toggleterm}" == "true" ]; then
            set_conf_value "enable_toggleterm" "false"
          else
            set_conf_value "enable_toggleterm" "true"
          fi
          pluginit=1
          break
          ;;
        "Enable Test"*,* | *,"Enable Test"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_neotest}" == "true" ]; then
            set_conf_value "enable_neotest" "false"
          else
            set_conf_value "enable_neotest" "true"
          fi
          pluginit=1
          break
          ;;
        "WakaTime"*,* | *,"WakaTime"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_wakatime}" == "true" ]; then
            set_conf_value "enable_wakatime" "false"
          else
            if [ -f "${HOME}"/.wakatime.cfg ]; then
              set_conf_value "enable_wakatime" "true"
            else
              printf "\nIt appears you do not have a configured WakaTime API key."
              printf "\nWould you like to proceed with enabling WakaTime?\n"
              while true; do
                read -r -p "Enable WakaTime (API key required) ? (y/n) " yn
                case $yn in
                  [Yy]*){:target="_blank"}{:rel="noopener noreferrer"}
                    set_conf_value "enable_wakatime" "true"
                    break
                    ;;
                  [Nn]*){:target="_blank"}{:rel="noopener noreferrer"}
                    break
                    ;;
                  *){:target="_blank"}{:rel="noopener noreferrer"}
                    printf "\nPlease answer yes or no.\n"
                    ;;
                esac
              done
            fi
          fi
          pluginit=1
          break
          ;;
        "Ascii Art"*,* | *,"Ascii Art"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_asciiart}" == "true" ]; then
            set_conf_value "enable_asciiart" "false"
          else
            set_conf_value "enable_asciiart" "true"
          fi
          pluginit=1
          break
          ;;
        "Cheatsheets"*,* | *,"Cheatsheets"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_cheatsheet}" == "true" ]; then
            set_conf_value "enable_cheatsheet" "false"
          else
            set_conf_value "enable_cheatsheet" "true"
          fi
          pluginit=1
          break
          ;;
        "Enable Motion"*,* | *,"Enable Motion"*){:target="_blank"}{:rel="noopener noreferrer"}
          choices=("Hop" "Leap" "None"){:target="_blank"}{:rel="noopener noreferrer"}
          choice=$(printf "%s\n" "${choices[@]}" | fzf --prompt=" Neovim Motion Plugin  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
          if [[ " ${choices[*]} " =~ " ${choice} " ]]; then
            if [ "${choice}" == "Hop" ]; then
              set_conf_value "enable_motion" "hop"
            else
              if [ "${choice}" == "Leap" ]; then
                set_conf_value "enable_motion" "leap"
              else
                if [ "${choice}" == "None" ]; then
                  set_conf_value "enable_motion" "none"
                fi
              fi
            fi
            pluginit=1
          fi
          break
          ;;
        "Enable Notes"*,* | *,"Enable Notes"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_notes}" == "true" ]; then
            set_conf_value "enable_notes" "false"
          else
            set_conf_value "enable_notes" "true"
          fi
          pluginit=1
          break
          ;;
        "Enable Obsidian"*,* | *,"Enable Obsidian"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_obsidian}" == "true" ]; then
            set_conf_value "enable_obsidian" "false"
          else
            set_conf_value "enable_obsidian" "true"
          fi
          pluginit=1
          break
          ;;
        "Enable Ranger"*,* | *,"Enable Ranger"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_ranger}" == "true" ]; then
            set_conf_value "enable_ranger_float" "false"
          else
            set_conf_value "enable_ranger_float" "true"
          fi
          pluginit=1
          break
          ;;
        "Securitree"*,* | *,"Securitree"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_securitree}" == "true" ]; then
            set_conf_value "enable_securitree" "false"
          else
            set_conf_value "enable_securitree" "true"
          fi
          pluginit=1
          break
          ;;
        "Enable coding"*,* | *,"Enable coding"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_coding}" == "true" ]; then
            printf "\n\nDisabling coding will disable LSP servers and several"
            printf "\nplugins providing coding and diagnostics features."
            printf "\nThis will create an editing environment for non-programmers."
            printf "\nIndividual features can be re-enabled using these menus.\n"
            while true; do
              read -r -p "Proceed with disabling coding features? (y/n) " yn
              case $yn in
                [Yy]*){:target="_blank"}{:rel="noopener noreferrer"}
                  set_conf_value "enable_coding" "false"
                  for lsp in "${all_lsp_servers[@]}"; do
                    set_conf_table "LSP_SERVERS" "${lsp}" "disable"
                  done
                  break
                  ;;
                [Nn]*){:target="_blank"}{:rel="noopener noreferrer"}
                  printf "\nSkipping disabling coding features\n"
                  break
                  ;;
                *){:target="_blank"}{:rel="noopener noreferrer"}
                  printf "\nPlease answer yes or no.\n"
                  ;;
              esac
            done
          else
            set_conf_value "enable_coding" "true"
            for lsp in "${all_lsp_servers[@]}"; do
              set_conf_table "LSP_SERVERS" "${lsp}" "enable"
            done
          fi
          pluginit=1
          break
          ;;
        "Compile"*,* | *,"Compile"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_compile}" == "true" ]; then
            set_conf_value "enable_compile" "false"
          else
            set_conf_value "enable_compile" "true"
          fi
          pluginit=1
          break
          ;;
        "Multi Cursor"*,* | *,"Multi Cursor"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_multi_cursor}" == "true" ]; then
            set_conf_value "enable_multi_cursor" "false"
          else
            set_conf_value "enable_multi_cursor" "true"
          fi
          pluginit=1
          break
          ;;
        "Enable Rename"*,* | *,"Enable Rename"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_renamer}" == "true" ]; then
            set_conf_value "enable_renamer" "false"
          else
            set_conf_value "enable_renamer" "true"
          fi
          pluginit=1
          break
          ;;
        "Bdelete"*,* | *,"Bdelete"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_bbye}" == "true" ]; then
            set_conf_value "enable_bbye" "false"
          else
            set_conf_value "enable_bbye" "true"
          fi
          pluginit=1
          break
          ;;
        "StartupTime"*,* | *,"StartupTime"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_startuptime}" == "true" ]; then
            set_conf_value "enable_startuptime" "false"
          else
            set_conf_value "enable_startuptime" "true"
          fi
          pluginit=1
          break
          ;;
        "Dressing"*,* | *,"Dressing"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_dressing}" == "true" ]; then
            set_conf_value "enable_dressing" "false"
          else
            set_conf_value "enable_dressing" "true"
          fi
          pluginit=1
          break
          ;;
        "Enable Games"*,* | *,"Enable Games"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_games}" == "true" ]; then
            set_conf_value "enable_games" "false"
          else
            set_conf_value "enable_games" "true"
          fi
          pluginit=1
          break
          ;;
        "Dashboard"*,* | *,"Dashboard"*){:target="_blank"}{:rel="noopener noreferrer"}
          choices=("alpha" "dash" "mini" "none"){:target="_blank"}{:rel="noopener noreferrer"}
          choice=$(printf "%s\n" "${choices[@]}" | fzf --prompt=" Neovim Dashboard  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
          if [[ " ${choices[*]} " =~ " ${choice} " ]]; then
            [ "${choice}" == "${use_dash}" ] || {
              set_conf_value "dashboard" "${choice}"
              pluginit=1
            }
          fi
          break
          ;;
        "Bookmarks"*,* | *,"Bookmarks"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_bookmarks}" == "true" ]; then
            set_conf_value "enable_bookmarks" "false"
          else
            set_conf_value "enable_bookmarks" "true"
          fi
          pluginit=1
          break
          ;;
        "Enable IDE"*,* | *,"Enable IDE"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_ide}" == "true" ]; then
            set_conf_value "enable_ide" "false"
          else
            set_conf_value "enable_ide" "true"
          fi
          pluginit=1
          break
          ;;
        "Navigator"*,* | *,"Navigator"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_navigator}" == "true" ]; then
            set_conf_value "enable_navigator" "false"
          else
            set_conf_value "enable_navigator" "true"
          fi
          pluginit=1
          break
          ;;
        "Project"*,* | *,"Project"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_project}" == "true" ]; then
            set_conf_value "enable_project" "false"
          else
            set_conf_value "enable_project" "true"
          fi
          pluginit=1
          break
          ;;
        "Picker"*,* | *,"Picker"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_picker}" == "true" ]; then
            set_conf_value "enable_picker" "false"
          else
            set_conf_value "enable_picker" "true"
          fi
          pluginit=1
          break
          ;;
        "Smooth Scroll"*,* | *,"Smooth Scroll"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_smooth_scrolling}" == "true" ]; then
            set_conf_value "enable_smooth_scrolling" "false"
          else
            set_conf_value "enable_smooth_scrolling" "true"
          fi
          pluginit=1
          break
          ;;
        " Recent Files"*,* | *," Recent Files"*){:target="_blank"}{:rel="noopener noreferrer"}
          choices=("0" "1" "2" "3" "4" "5" "6" "7" "8" "9"){:target="_blank"}{:rel="noopener noreferrer"}
          choice=$(printf "%s\n" "${choices[@]}" | fzf --prompt=" Number of Recent Files  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
          [ "${choice}" == "${dashboard_recent_files}" ] || {
            if [[ " ${choices[*]} " =~ " ${choice} " ]]; then
              set_conf_value "dashboard_recent_files" "${choice}"
              pluginit=1
            fi
          }
          break
          ;;
        " Alpha Header"*,* | *," Alpha Header"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_dashboard_header}" == "true" ]; then
            set_conf_value "enable_dashboard_header" "false"
          else
            set_conf_value "enable_dashboard_header" "true"
          fi
          pluginit=1
          break
          ;;
        " Quick Links"*,* | *," Quick Links"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_dashboard_quick_links}" == "true" ]; then
            set_conf_value "enable_dashboard_quick_links" "false"
          else
            set_conf_value "enable_dashboard_quick_links" "true"
          fi
          pluginit=1
          break
          ;;
        "Screensaver"*,* | *,"Screensaver"*){:target="_blank"}{:rel="noopener noreferrer"}
          choices=("epilepsy" "leaves" "snow" "spring" "stars" "summer" "treadmill" "vanish" "xmas" "drop" "zone" "random" "none"){:target="_blank"}{:rel="noopener noreferrer"}
          choice=$(printf "%s\n" "${choices[@]}" | fzf --prompt=" Select Screensaver  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
          if [[ " ${choices[*]} " =~ " ${choice} " ]]; then
            set_conf_value "enable_screensaver" "${choice}"
            pluginit=1
          fi
          break
          ;;
        " Timeout"*,* | *," Timeout"*){:target="_blank"}{:rel="noopener noreferrer"}
          choices=("1" "2" "3" "4" "5" "10" "15" "30" "45"){:target="_blank"}{:rel="noopener noreferrer"}
          choice=$(printf "%s\n" "${choices[@]}" | fzf --prompt=" Screensaver Timeout in Minutes  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
          [ "${choice}" == "${screensaver_timeout}" ] || {
            if [[ " ${choices[*]} " =~ " ${choice} " ]]; then
              set_conf_value "screensaver_timeout" "${choice}"
              pluginit=1
            fi
          }
          break
          ;;
        "Indentline"*,* | *,"Indentline"*){:target="_blank"}{:rel="noopener noreferrer"}
          choices=("background" "colored" "context" "listchars" "mini" "simple" "none"){:target="_blank"}{:rel="noopener noreferrer"}
          choice=$(printf "%s\n" "${choices[@]}" | fzf --prompt=" Select Indentline Style  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
          [ "${choice}" == "${use_indentline}" ] || {
            if [[ " ${choices[*]} " =~ " ${choice} " ]]; then
              set_conf_value "indentline_style" "${choice}"
              pluginit=1
            fi
          }
          break
          ;;
        "Disable All"*,* | *,"Disable All"*){:target="_blank"}{:rel="noopener noreferrer"}
          set_conf_value "dashboard" "none"
          set_conf_value "file_tree" "none"
          set_conf_value "media_backend" "none"
          set_conf_value "session_manager" "none"
          set_conf_value "enable_noice" "false"
          set_conf_value "enable_chatgpt" "false"
          set_conf_value "enable_codeium" "false"
          set_conf_value "enable_copilot" "false"
          set_conf_value "enable_codeexplain" "false"
          set_conf_value "enable_neoai" "false"
          set_conf_value "enable_surround" "false"
          set_conf_value "enable_fancy" "false"
          set_conf_value "enable_wilder" "false"
          set_conf_value "enable_lualine_lsp_progress" "false"
          set_conf_value "enable_terminal" "false"
          set_conf_value "enable_toggleterm" "false"
          set_conf_value "enable_neotest" "false"
          set_conf_value "enable_wakatime" "false"
          set_conf_value "enable_asciiart" "false"
          set_conf_value "enable_cheatsheet" "false"
          set_conf_value "enable_notes" "false"
          set_conf_value "markdown_preview" "none"
          set_conf_value "enable_coding" "false"
          set_conf_value "enable_compile" "false"
          set_conf_value "enable_dressing" "false"
          set_conf_value "enable_motion" "none"
          set_conf_value "enable_obsidian" "false"
          set_conf_value "enable_ranger_float" "false"
          set_conf_value "enable_renamer" "false"
          set_conf_value "enable_securitree" "false"
          set_conf_value "enable_multi_cursor" "false"
          set_conf_value "enable_bbye" "false"
          set_conf_value "enable_startuptime" "false"
          set_conf_value "enable_games" "false"
          set_conf_value "enable_bookmarks" "false"
          set_conf_value "enable_ide" "false"
          set_conf_value "enable_navigator" "false"
          set_conf_value "enable_project" "false"
          set_conf_value "enable_picker" "false"
          set_conf_value "enable_smooth_scrolling" "false"
          set_conf_value "enable_dashboard_header" "false"
          set_conf_value "enable_dashboard_quick_links" "false"
          set_conf_value "enable_screensaver" "none"
          set_conf_value "indentline_style" "none"
          pluginit=1
          break
          ;;
        "Enable All"*,* | *,"Enable All"*){:target="_blank"}{:rel="noopener noreferrer"}
          set_conf_value "dashboard" "dash"
          set_conf_value "file_tree" "neo-tree"
          set_conf_value "media_backend" "jp2a"
          set_conf_value "session_manager" "possession"
          set_conf_value "enable_noice" "true"
          set_conf_value "enable_chatgpt" "true"
          set_conf_value "enable_codeium" "true"
          set_conf_value "enable_copilot" "true"
          set_conf_value "enable_neoai" "true"
          [ -f "${HOME}/.codeexplain/model.bin" ] && {
            pyver=$(check_python_version){:target="_blank"}{:rel="noopener noreferrer"}
            [ "${pyver}" == "OK" ] && {
              set_conf_value "enable_codeexplain" "true"
            }
          }
          set_conf_value "enable_surround" "true"
          set_conf_value "enable_fancy" "true"
          set_conf_value "enable_wilder" "true"
          set_conf_value "enable_lualine_lsp_progress" "true"
          set_conf_value "enable_terminal" "true"
          set_conf_value "enable_toggleterm" "true"
          set_conf_value "enable_neotest" "true"
          [ -f "${HOME}"/.wakatime.cfg ] && set_conf_value "enable_wakatime" "true"
          set_conf_value "enable_asciiart" "true"
          set_conf_value "enable_cheatsheet" "true"
          set_conf_value "enable_notes" "true"
          set_conf_value "markdown_preview" "peek"
          set_conf_value "enable_coding" "true"
          set_conf_value "enable_compile" "true"
          set_conf_value "enable_dressing" "true"
          set_conf_value "enable_motion" "leap"
          set_conf_value "enable_obsidian" "true"
          set_conf_value "enable_ranger_float" "true"
          set_conf_value "enable_renamer" "true"
          set_conf_value "enable_securitree" "true"
          set_conf_value "enable_multi_cursor" "true"
          set_conf_value "enable_bbye" "true"
          set_conf_value "enable_startuptime" "true"
          set_conf_value "enable_games" "true"
          set_conf_value "enable_bookmarks" "true"
          set_conf_value "enable_ide" "true"
          set_conf_value "enable_navigator" "true"
          set_conf_value "enable_project" "true"
          set_conf_value "enable_picker" "true"
          set_conf_value "enable_smooth_scrolling" "true"
          set_conf_value "enable_dashboard_header" "true"
          set_conf_value "enable_dashboard_quick_links" "true"
          set_conf_value "enable_screensaver" "random"
          set_conf_value "indentline_style" "mini"
          set_conf_value "list" "true"
          pluginit=1
          break
          ;;
        "Reset"*,* | *,"Reset"*){:target="_blank"}{:rel="noopener noreferrer"}
          [ -f ${CONFBACK} ] && {
            cp ${CONFBACK} ${NVIMCONF}
            set_code_explain
            set_ranger_float
            set_waka_opt
            pluginit=1
          }
          break
          ;;
        "Open Lazyman",* | *,"Open Lazyman"){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${USEGUI}" ]; then
            NVIM_APPNAME="nvim-Lazyman" neovide
          else
            NVIM_APPNAME="nvim-Lazyman" nvim
          fi
          break
          ;;
        "Config Menu"*,* | *,"Config Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
          confmenu=1
          break 2
          ;;
        "Formatters"*,* | *,"Formatters"*){:target="_blank"}{:rel="noopener noreferrer"}
          formenu=1
          break 2
          ;;
        "LSP Servers"*,* | *,"LSP Servers"*){:target="_blank"}{:rel="noopener noreferrer"}
          lspmenu=1
          break 2
          ;;
        "Main Menu"*,* | *,"Main Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
          [ "${pluginit}" ] && lazyman -N nvim-Lazyman init
          mainmenu=1
          break 2
          ;;
        "Quit",* | *,"Quit" | "quit",* | *,"quit"){:target="_blank"}{:rel="noopener noreferrer"}
          [ "${pluginit}" ] && lazyman -N nvim-Lazyman init
          printf "\nExiting Lazyman Configuration Menu System\n\n"
          exit 3
          ;;
        *,*){:target="_blank"}{:rel="noopener noreferrer"}
          printf "\nNo matching menu item located."
          printf "\nSelection out of range or malformed."
          prompt_continue
          break
          ;;
      esac
      REPLY=
    done
  done
  [ "${confmenu}" ] && show_conf_menu
  [ "${mainmenu}" ] && exit 2
  [ "${lspmenu}" ] && show_lsp_menu
  [ "${formenu}" ] && show_formlint_menu
}

show_lsp_help() {
  if [ "${have_rich}" ]; then
    rich "[cyan]Lazyman LSP Servers Menu Help[/cyan]" -p -a rounded -c -C
  else
    printf "\n\tLazyman LSP Servers Menu Help\n"
  fi
  printf "\nEnable and disable installed Neovim language servers."
  printf "\nEnabled language servers are indicated with a []"
  printf "\nDisabled language servers are indicated with a [✗]\n"
  printf "\nThe Language Server Protocol (LSP) is an open protocol for use between"
  printf "\nsource code editors or integrated development environments (IDEs) and"
  printf "\nservers that provide programming language-specific features like code"
  printf "\ncompletion, syntax highlighting and marking of warnings and errors,"
  printf "\nas well as refactoring routines.\n"
  printf "\nSettings in this menu only effect the Lazyman Neovim configuration in:"
  printf "\n\t${HOME}/.config/lazyman/Lazyman\n"
  prompt_continue
}

show_lsp_menu() {
  set_haves
  while true; do
    mainmenu=
    confmenu=
    plugmenu=
    formmenu=
    versmenu=
    [ -f ${GET_CONF} ] || {
      printf "\n\nWARNING: missing ${GET_CONF}"
      printf "\nUnable to modify configuration from this menu"
      printf "\nYou may need to update or re-install Lazyman"
      prompt_continue
      mainmenu=1
      break
    }
    [ "$debug" ] || tput reset
    if [ "${have_rich}" ]; then
      rich "[cyan]Lazyman LSP Servers Menu[/cyan]" -p -a rounded -c -C
      rich "[b green]Enable/Disable LSP servers used by[/] [b yellow]~/.config/lazyman/Lazyman[/]" -p -c
    else
      [ "${have_figlet}" ] && show_figlet "LSP Menu"
    fi
    printf '\n'
    get_conf_table lsp_servers
    PS3="${BOLD}${PLEASE} (numeric or text, 'h' for help): ${NORM}"
    options=(){:target="_blank"}{:rel="noopener noreferrer"}
    readarray -t lsp_sorted < <(printf '%s\0' "${all_lsp_servers[@]}" | sort -z | xargs -0n1){:target="_blank"}{:rel="noopener noreferrer"}
    for lsp in "${lsp_sorted[@]}"; do
      len=${#lsp}
      numsp=$((14 - len)){:target="_blank"}{:rel="noopener noreferrer"}
      [ ${numsp} -lt 0 ] && numsp=0
      longlsp="${lsp}"
      while [ ${numsp} -gt 0 ]; do
        longlsp="${longlsp} "
        ((numsp -= 1)){:target="_blank"}{:rel="noopener noreferrer"}
      done
      if echo "${lsp_enabled_table[@]}" | grep -qw "$lsp" >/dev/null; then
        options+=("${longlsp} []"){:target="_blank"}{:rel="noopener noreferrer"}
      else
        options+=("${longlsp} [✗]"){:target="_blank"}{:rel="noopener noreferrer"}
      fi
    done
    options+=("Disable All"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Enable All"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Formatters Menu"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Plugins Menu"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Config Menu"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Main Menu"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Quit"){:target="_blank"}{:rel="noopener noreferrer"}
    select opt in "${options[@]}"; do
      case "$opt,$REPLY" in
        "h",* | *,"h" | "H",* | *,"H" | "help",* | *,"help" | "Help",* | *,"Help"){:target="_blank"}{:rel="noopener noreferrer"}
          [ "$debug" ] || tput reset
          show_lsp_help
          break
          ;;
        "Disable All"*,* | *,"Disable All"*){:target="_blank"}{:rel="noopener noreferrer"}
          for lsp in "${all_lsp_servers[@]}"; do
            set_conf_table "LSP_SERVERS" "${lsp}" "disable"
          done
          pluginit=1
          break
          ;;
        "Enable All"*,* | *,"Enable All"*){:target="_blank"}{:rel="noopener noreferrer"}
          for lsp in "${all_lsp_servers[@]}"; do
            set_conf_table "LSP_SERVERS" "${lsp}" "enable"
          done
          pluginit=1
          break
          ;;
        "Formatters Menu"*,* | *,"Formatters Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
          formmenu=1
          break 2
          ;;
        "Config Menu"*,* | *,"Config Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
          confmenu=1
          break 2
          ;;
        "Plugins Menu"*,* | *,"Plugins Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
          plugmenu=1
          break 2
          ;;
        "Main Menu"*,* | *,"Main Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
          [ "${pluginit}" ] && lazyman -N nvim-Lazyman init
          mainmenu=1
          break 2
          ;;
        "Quit",* | *,"Quit" | "quit",* | *,"quit"){:target="_blank"}{:rel="noopener noreferrer"}
          [ "${pluginit}" ] && lazyman -N nvim-Lazyman init
          printf "\nExiting Lazyman Configuration Menu System\n\n"
          exit 3
          ;;
        *,*){:target="_blank"}{:rel="noopener noreferrer"}
          enable=
          if [ "${opt}" ]; then
            lspname=$(echo "${opt}" | awk ' { print $1 } '){:target="_blank"}{:rel="noopener noreferrer"}
          else
            lspname=$(echo "${REPLY}" | awk ' { print $1 } '){:target="_blank"}{:rel="noopener noreferrer"}
          fi
          grep "LSP_SERVERS" "${NVIMCONF}" | grep "\-\- \"${lspname}" >/dev/null && enable=1
          if [ "${enable}" ]; then
            set_conf_table "LSP_SERVERS" "${lspname}" "enable"
          else
            set_conf_table "LSP_SERVERS" "${lspname}" "disable"
          fi
          pluginit=1
          break
          ;;
      esac
      REPLY=
    done
  done
  [ "${mainmenu}" ] && exit 2
  [ "${confmenu}" ] && show_conf_menu
  [ "${plugmenu}" ] && show_plugin_menu
  [ "${formmenu}" ] && show_formlint_menu
}

show_form_help() {
  if [ "${have_rich}" ]; then
    rich "[cyan]Lazyman Formatters and Linters Menu Help[/cyan]" -p -a rounded -c -C
  else
    printf "\n\tLazyman Formatters and Linters Menu Help\n"
  fi
  printf "\nEnable and disable installed Neovim formatters and linters."
  printf "\nEnabled formatters and linters are indicated with a []"
  printf "\nDisabled formatters and linters are indicated with a [✗]\n"
  printf "\nThese tools perform code formatting, static code analysis, and flag"
  printf "\nprogramming errors, bugs, stylistic errors and suspicious constructs.\n"
  printf "\nSettings in this menu only effect the Lazyman Neovim configuration in:"
  printf "\n\t${HOME}/.config/lazyman/Lazyman\n"
  prompt_continue
}

show_formlint_menu() {
  set_haves
  while true; do
    mainmenu=
    confmenu=
    plugmenu=
    lspsmenu=
    versmenu=
    [ -f ${GET_CONF} ] || {
      printf "\n\nWARNING: missing ${GET_CONF}"
      printf "\nUnable to modify configuration from this menu"
      printf "\nYou may need to update or re-install Lazyman"
      prompt_continue
      mainmenu=1
      break
    }
    [ "$debug" ] || tput reset
    if [ "${have_rich}" ]; then
      rich "[cyan]Lazyman Formatters and Linters Menu[/cyan]" -p -a rounded -c -C
      rich "[b green]Enable/Disable formatters and linters used by[/] [b yellow]~/.config/lazyman/Lazyman[/]" -p -c
    else
      [ "${have_figlet}" ] && show_figlet "Formatters"
    fi
    printf '\n'
    get_conf_table formatters_linters
    PS3="${BOLD}${PLEASE} (numeric or text, 'h' for help): ${NORM}"
    options=(){:target="_blank"}{:rel="noopener noreferrer"}
    readarray -t form_sorted < <(printf '%s\0' "${all_formatters[@]}" | sort -z | xargs -0n1){:target="_blank"}{:rel="noopener noreferrer"}
    for form in "${form_sorted[@]}"; do
      len=${#form}
      numsp=$((19 - len)){:target="_blank"}{:rel="noopener noreferrer"}
      [ ${numsp} -lt 0 ] && numsp=0
      longform="${form}"
      while [ ${numsp} -gt 0 ]; do
        longform="${longform} "
        ((numsp -= 1)){:target="_blank"}{:rel="noopener noreferrer"}
      done
      if echo "${for_enabled_table[@]}" | grep -qw "$form" >/dev/null; then
        options+=("${longform} []"){:target="_blank"}{:rel="noopener noreferrer"}
      else
        options+=("${longform} [✗]"){:target="_blank"}{:rel="noopener noreferrer"}
      fi
    done
    options+=("Disable All"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Enable All"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("LSP Servers Menu"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Plugins Menu"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Config Menu"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Main Menu"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Quit"){:target="_blank"}{:rel="noopener noreferrer"}
    select opt in "${options[@]}"; do
      case "$opt,$REPLY" in
        "h",* | *,"h" | "H",* | *,"H" | "help",* | *,"help" | "Help",* | *,"Help"){:target="_blank"}{:rel="noopener noreferrer"}
          [ "$debug" ] || tput reset
          show_form_help
          break
          ;;
        "Disable All"*,* | *,"Disable All"*){:target="_blank"}{:rel="noopener noreferrer"}
          for form in "${all_formatters[@]}"; do
            set_conf_table "FORMATTERS_LINTERS" "${form}" "disable"
          done
          pluginit=1
          break
          ;;
        "Enable All"*,* | *,"Enable All"*){:target="_blank"}{:rel="noopener noreferrer"}
          for form in "${all_formatters[@]}"; do
            set_conf_table "FORMATTERS_LINTERS" "${form}" "enable"
          done
          pluginit=1
          break
          ;;
        "LSP Servers"*,* | *,"LSP Servers"*){:target="_blank"}{:rel="noopener noreferrer"}
          lspsmenu=1
          break 2
          ;;
        "Plugins Menu"*,* | *,"Plugins Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
          plugmenu=1
          break 2
          ;;
        "Config Menu"*,* | *,"Config Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
          confmenu=1
          break 2
          ;;
        "Main Menu"*,* | *,"Main Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
          [ "${pluginit}" ] && lazyman -N nvim-Lazyman init
          mainmenu=1
          break 2
          ;;
        "Quit",* | *,"Quit" | "quit",* | *,"quit"){:target="_blank"}{:rel="noopener noreferrer"}
          [ "${pluginit}" ] && lazyman -N nvim-Lazyman init
          printf "\nExiting Lazyman Configuration Menu System\n\n"
          exit 3
          ;;
        *,*){:target="_blank"}{:rel="noopener noreferrer"}
          enable=
          if [ "${opt}" ]; then
            forname=$(echo "${opt}" | awk ' { print $1 } '){:target="_blank"}{:rel="noopener noreferrer"}
          else
            forname=$(echo "${REPLY}" | awk ' { print $1 } '){:target="_blank"}{:rel="noopener noreferrer"}
          fi
          grep "FORMATTERS_LINTERS" "${NVIMCONF}" | grep "\-\- \"${forname}" >/dev/null && enable=1
          if [ "${enable}" ]; then
            set_conf_table "FORMATTERS_LINTERS" "${forname}" "enable"
          else
            set_conf_table "FORMATTERS_LINTERS" "${forname}" "disable"
          fi
          pluginit=1
          break
          ;;
      esac
      REPLY=
    done
  done
  [ "${mainmenu}" ] && exit 2
  [ "${confmenu}" ] && show_conf_menu
  [ "${plugmenu}" ] && show_plugin_menu
  [ "${lspsmenu}" ] && show_lsp_menu
}

show_conf_menu() {
  set_haves
  while true; do
    mainmenu=
    plugmenu=
    lspmenu=
    formenu=
    lidemenu=
    wdevmenu=
    [ -f ${GET_CONF} ] || {
      printf "\n\nWARNING: missing ${GET_CONF}"
      printf "\nUnable to modify configuration from this menu"
      printf "\nYou may need to update or re-install Lazyman"
      prompt_continue
      mainmenu=1
      break
    }
    [ "$debug" ] || tput reset
    if [ "${have_rich}" ]; then
      rich "[b cyan]Lazyman Configuration Menu[/]" -p -a rounded -c -C
      rich "[b green]Manage the Neovim configuration in[/] [b yellow]~/.config/lazyman/Lazyman[/]" -p -c
    else
      [ "${have_figlet}" ] && show_figlet "Config"
    fi
    printf '\n'
    namespace=$(get_conf_value namespace){:target="_blank"}{:rel="noopener noreferrer"}
    use_namespace="${namespace}"
    theme=$(get_conf_value theme){:target="_blank"}{:rel="noopener noreferrer"}
    use_theme="${theme}"
    theme_style=$(get_conf_value theme_style){:target="_blank"}{:rel="noopener noreferrer"}
    use_theme_style="${theme_style}"
    enable_transparent=$(get_conf_value enable_transparent){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_transparent}" == "true" ]; then
      use_transparent=""
    else
      use_transparent="✗"
    fi
    mapleader=$(get_conf_value mapleader){:target="_blank"}{:rel="noopener noreferrer"}
    use_mapleader="${mapleader}"
    maplocalleader=$(get_conf_value maplocalleader){:target="_blank"}{:rel="noopener noreferrer"}
    use_maplocalleader="${maplocalleader}"
    enable_number=$(get_conf_value number){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_number}" == "true" ]; then
      use_number=""
    else
      use_number="✗"
    fi
    enable_relative_number=$(get_conf_value relative_number){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_relative_number}" == "true" ]; then
      use_relative_number=""
    else
      use_relative_number="✗"
    fi
    enable_smartcolumn=$(get_conf_value enable_smartcolumn){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_smartcolumn}" == "true" ]; then
      use_smartcolumn=""
    else
      use_smartcolumn="✗"
    fi
    enable_global_statusline=$(get_conf_value global_statusline){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_global_statusline}" == "true" ]; then
      use_global_statusline=""
    else
      use_global_statusline="✗"
    fi
    showtabline=$(get_conf_value showtabline){:target="_blank"}{:rel="noopener noreferrer"}
    use_showtabline="${showtabline}"
    enable_list=$(get_conf_value list){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_list}" == "true" ]; then
      use_list=""
    else
      use_list="✗"
    fi
    enable_statusline=$(get_conf_value enable_statusline){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_statusline}" == "true" ]; then
      use_statusline=""
    else
      use_statusline="✗"
    fi
    enable_tabline=$(get_conf_value enable_status_in_tab){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_tabline}" == "true" ]; then
      use_tabline=""
    else
      use_tabline="✗"
    fi
    enable_winbar=$(get_conf_value enable_winbar){:target="_blank"}{:rel="noopener noreferrer"}
    use_winbar="${enable_winbar}"
    show_diagnostics=$(get_conf_value show_diagnostics){:target="_blank"}{:rel="noopener noreferrer"}
    use_show_diagnostics="${show_diagnostics}"
    enable_semantic_highlighting=$(get_conf_value enable_semantic_highlighting){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_semantic_highlighting}" == "true" ]; then
      use_semantic_highlighting=""
    else
      use_semantic_highlighting="✗"
    fi
    convert_semantic_highlighting=$(get_conf_value convert_semantic_highlighting){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${convert_semantic_highlighting}" == "true" ]; then
      convert_semantic_highlighting=""
    else
      convert_semantic_highlighting="✗"
    fi
    enable_zenmode=$(get_conf_value enable_zenmode){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${enable_zenmode}" == "true" ]; then
      use_zenmode=""
    else
      use_zenmode="✗"
    fi
    PS3="${BOLD}${PLEASE} (numeric or text, 'h' for help): ${NORM}"
    options=(){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Namespace   [${use_namespace}]"){:target="_blank"}{:rel="noopener noreferrer"}
    [ "${use_namespace}" == "free" ] && {
      options+=("Diagnostics [${use_show_diagnostics}]"){:target="_blank"}{:rel="noopener noreferrer"}
    }
    options+=("Theme [${use_theme}]"){:target="_blank"}{:rel="noopener noreferrer"}
    if [[ " ${styled_themes[*]} " =~ " ${use_theme} " ]]; then
      options+=(" Style [${use_theme_style}]"){:target="_blank"}{:rel="noopener noreferrer"}
    fi
    options+=(" Transparency [${use_transparent}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Leader        [${use_mapleader}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Local Leader  [${use_maplocalleader}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Number Lines  [${use_number}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Relative Nums [${use_relative_number}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("List Chars    [${use_list}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Smart Column  [${use_smartcolumn}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Global Status [${use_global_statusline}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Status Line   [${use_statusline}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Status in Tab [${use_tabline}]"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Show Tabline  [${use_showtabline}]"){:target="_blank"}{:rel="noopener noreferrer"}
    if [ "${use_winbar}" == "none" ]
    then
      options+=("Winbar     [${use_winbar}]"){:target="_blank"}{:rel="noopener noreferrer"}
    else
      options+=("Winbar [${use_winbar}]"){:target="_blank"}{:rel="noopener noreferrer"}
    fi
    [ "${use_namespace}" == "free" ] && {
      options+=("Semantic HL   [${use_semantic_highlighting}]"){:target="_blank"}{:rel="noopener noreferrer"}
      options+=("Convert SemHL [${convert_semantic_highlighting}]"){:target="_blank"}{:rel="noopener noreferrer"}
      options+=("Zen Mode      [${use_zenmode}]"){:target="_blank"}{:rel="noopener noreferrer"}
    }
    options+=("Disable All"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Enable All"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Minimal Config"){:target="_blank"}{:rel="noopener noreferrer"}
    [ -f ${CONFBACK} ] && {
      diff ${CONFBACK} ${NVIMCONF} >/dev/null || options+=("Reset to Defaults"){:target="_blank"}{:rel="noopener noreferrer"}
    }
    [ -d "${LMANDIR}" ] && options+=("Open Lazyman"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Formatters"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("LSP Servers"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Plugins Menu"){:target="_blank"}{:rel="noopener noreferrer"}
    [ -f ${HOME}/.config/lazyman/LazyIde/lua/configuration.lua ] && {
      options+=("LazyIde Config"){:target="_blank"}{:rel="noopener noreferrer"}
    }
    [ -f ${HOME}/.config/lazyman/Webdev/lua/configuration.lua ] && {
      options+=("Webdev Config"){:target="_blank"}{:rel="noopener noreferrer"}
    }
    options+=("Main Menu"){:target="_blank"}{:rel="noopener noreferrer"}
    options+=("Quit"){:target="_blank"}{:rel="noopener noreferrer"}
    select opt in "${options[@]}"; do
      case "$opt,$REPLY" in
        "h",* | *,"h" | "H",* | *,"H" | "help",* | *,"help" | "Help",* | *,"Help"){:target="_blank"}{:rel="noopener noreferrer"}
          [ "$debug" ] || tput reset
          printf "\n"
          man lazyman
          break
          ;;
        "Smart Column"*,* | *,"Smart Column"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_smartcolumn}" == "true" ]; then
            set_conf_value "enable_smartcolumn" "false"
          else
            set_conf_value "enable_smartcolumn" "true"
          fi
          pluginit=1
          break
          ;;
        "Status Line"*,* | *,"Status Line"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_statusline}" == "true" ]; then
            set_conf_value "enable_statusline" "false"
          else
            set_conf_value "enable_statusline" "true"
          fi
          pluginit=1
          break
          ;;
        "Status in Tab"*,* | *,"Status in Tab"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_tabline}" == "true" ]; then
            set_conf_value "enable_status_in_tab" "false"
          else
            set_conf_value "enable_status_in_tab" "true"
          fi
          pluginit=1
          break
          ;;
        "Winbar"*,* | *,"Winbar"*){:target="_blank"}{:rel="noopener noreferrer"}
          choices=("Barbecue" "Standard" "None"){:target="_blank"}{:rel="noopener noreferrer"}
          choice=$(printf "%s\n" "${choices[@]}" | fzf --prompt=" Select winbar style  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
          if [[ " ${choices[*]} " =~ " ${choice} " ]]; then
            if [ "${choice}" == "Barbecue" ]; then
              set_conf_value "enable_winbar" "barbecue"
            else
              if [ "${choice}" == "Standard" ]; then
                set_conf_value "enable_winbar" "standard"
              else
                if [ "${choice}" == "None" ]; then
                  set_conf_value "enable_winbar" "none"
                fi
              fi
            fi
            pluginit=1
          fi
          break
          ;;
        " Style"*,* | *," Style"*){:target="_blank"}{:rel="noopener noreferrer"}
          select_theme_style ${theme}
          break
          ;;
        "Theme"*,* | *,"Theme"*){:target="_blank"}{:rel="noopener noreferrer"}
          select_theme ${theme}
          pluginit=1
          break
          ;;
        " Transparency"*,* | *," Transparency"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_transparent}" == "true" ]; then
            set_conf_value "enable_transparent" "false"
          else
            set_conf_value "enable_transparent" "true"
          fi
          break
          ;;
        "Namespace"*,* | *,"Namespace"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${use_namespace}" == "onno" ]; then
            set_conf_value "namespace" "free"
          else
            set_conf_value "namespace" "onno"
          fi
          pluginit=1
          break
          ;;
        "Leader"*,* | *,"Leader"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${use_mapleader}" == "," ]; then
            set_conf_value "mapleader" " "
          else
            set_conf_value "mapleader" ","
          fi
          break
          ;;
        "Local Leader"*,* | *,"Local Leader"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${use_maplocalleader}" == "," ]; then
            set_conf_value "maplocalleader" " "
          else
            set_conf_value "maplocalleader" ","
          fi
          break
          ;;
        "Number Lines"*,* | *,"Number Lines"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_number}" == "true" ]; then
            set_conf_value "number" "false"
          else
            set_conf_value "number" "true"
          fi
          break
          ;;
        "Relative Num"*,* | *,"Relative Num"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_relative_number}" == "true" ]; then
            set_conf_value "relative_number" "false"
          else
            set_conf_value "relative_number" "true"
          fi
          break
          ;;
        "List"*,* | *,"List"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_list}" == "true" ]; then
            set_conf_value "list" "false"
          else
            set_conf_value "list" "true"
          fi
          break
          ;;
        "Global Status"*,* | *,"Global Status"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_global_statusline}" == "true" ]; then
            set_conf_value "global_statusline" "false"
          else
            set_conf_value "global_statusline" "true"
          fi
          break
          ;;
        "Show Tabline"*,* | *,"Show Tabline"*){:target="_blank"}{:rel="noopener noreferrer"}
          choices=("0" "1" "2"){:target="_blank"}{:rel="noopener noreferrer"}
          choice=$(printf "%s\n" "${choices[@]}" | fzf --prompt=" Show tabline (0=never, 1=multiple tabs, 2=always)  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
          [ "${choice}" == "${showtabline}" ] || {
            if [[ " ${choices[*]} " =~ " ${choice} " ]]; then
              set_conf_value "showtabline" "${choice}"
            fi
          }
          break
          ;;
        "Diagnostic"*,* | *,"Diagnostic"*){:target="_blank"}{:rel="noopener noreferrer"}
          choices=("none" "icons" "popup"){:target="_blank"}{:rel="noopener noreferrer"}
          choice=$(printf "%s\n" "${choices[@]}" | fzf --prompt=" Neovim Diagnostics  " --layout=reverse --border --exit-0){:target="_blank"}{:rel="noopener noreferrer"}
          [ "${choice}" == "${show_diagnostics}" ] || {
            if [[ " ${choices[*]} " =~ " ${choice} " ]]; then
              set_conf_value "show_diagnostics" "${choice}"
            fi
          }
          break
          ;;
        "Semantic HL"*,* | *,"Semantic HL"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_semantic_highlighting}" == "true" ]; then
            set_conf_value "enable_semantic_highlighting" "false"
          else
            set_conf_value "enable_semantic_highlighting" "true"
          fi
          break
          ;;
        "Convert SemHL"*,* | *,"Convert SemHL"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${convert_semantic_highlighting}" == "true" ]; then
            set_conf_value "convert_semantic_highlighting" "false"
          else
            set_conf_value "convert_semantic_highlighting" "true"
          fi
          break
          ;;
        "Zen Mode"*,* | *,"Zen Mode"*){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${enable_zenmode}" == "true" ]; then
            set_conf_value "enable_zenmode" "false"
          else
            set_conf_value "enable_zenmode" "true"
          fi
          pluginit=1
          break
          ;;
        "Minimal Config"*,* | *,"Minimal Config"*){:target="_blank"}{:rel="noopener noreferrer"}
          set_conf_value "global_statusline" "false"
          set_conf_value "enable_smartcolumn" "false"
          set_conf_value "enable_statusline" "false"
          set_conf_value "enable_status_in_tab" "false"
          set_conf_value "enable_zenmode" "false"
          set_conf_value "showtabline" "0"
          set_conf_value "enable_winbar" "none"
          set_conf_value "show_diagnostics" "none"
          set_conf_value "enable_semantic_highlighting" "false"
          set_conf_value "convert_semantic_highlighting" "false"
          set_conf_value "media_backend" "none"
          set_conf_value "enable_chatgpt" "false"
          set_conf_value "enable_codeium" "false"
          set_conf_value "enable_copilot" "false"
          set_conf_value "enable_codeexplain" "false"
          set_conf_value "enable_neoai" "false"
          set_conf_value "enable_surround" "false"
          set_conf_value "enable_fancy" "false"
          set_conf_value "enable_wilder" "false"
          set_conf_value "enable_lualine_lsp_progress" "false"
          set_conf_value "enable_wakatime" "false"
          set_conf_value "enable_asciiart" "false"
          set_conf_value "enable_coding" "false"
          set_conf_value "enable_compile" "false"
          set_conf_value "enable_dressing" "false"
          set_conf_value "enable_motion" "none"
          set_conf_value "enable_obsidian" "false"
          set_conf_value "enable_ranger_float" "false"
          set_conf_value "enable_renamer" "false"
          set_conf_value "enable_securitree" "false"
          set_conf_value "enable_multi_cursor" "false"
          set_conf_value "enable_bbye" "false"
          set_conf_value "enable_startuptime" "false"
          set_conf_value "enable_games" "false"
          set_conf_value "enable_bookmarks" "false"
          set_conf_value "enable_ide" "false"
          set_conf_value "enable_navigator" "false"
          set_conf_value "enable_project" "false"
          set_conf_value "enable_picker" "false"
          set_conf_value "enable_dashboard_header" "false"
          set_conf_value "enable_screensaver" "none"
          for lsp in "${all_lsp_servers[@]}"; do
            set_conf_table "LSP_SERVERS" "${lsp}" "disable"
          done
          for form in "${all_formatters[@]}"; do
            set_conf_table "FORMATTERS_LINTERS" "${form}" "disable"
          done
          pluginit=1
          break
          ;;
        "Disable All"*,* | *,"Disable All"*){:target="_blank"}{:rel="noopener noreferrer"}
          set_conf_value "number" "false"
          set_conf_value "relative_number" "false"
          set_conf_value "enable_smartcolumn" "false"
          set_conf_value "global_statusline" "false"
          set_conf_value "enable_statusline" "false"
          set_conf_value "enable_status_in_tab" "false"
          set_conf_value "enable_zenmode" "false"
          set_conf_value "showtabline" "0"
          set_conf_value "enable_winbar" "none"
          set_conf_value "enable_transparent" "false"
          set_conf_value "show_diagnostics" "none"
          set_conf_value "enable_semantic_highlighting" "false"
          set_conf_value "convert_semantic_highlighting" "false"
          set_conf_value "list" "false"
          pluginit=1
          break
          ;;
        "Enable All"*,* | *,"Enable All"*){:target="_blank"}{:rel="noopener noreferrer"}
          set_conf_value "number" "true"
          set_conf_value "relative_number" "true"
          set_conf_value "enable_smartcolumn" "true"
          set_conf_value "global_statusline" "true"
          set_conf_value "enable_statusline" "true"
          set_conf_value "showtabline" "2"
          set_conf_value "enable_winbar" "barbecue"
          set_conf_value "enable_transparent" "true"
          set_conf_value "show_diagnostics" "popup"
          set_conf_value "enable_semantic_highlighting" "true"
          set_conf_value "convert_semantic_highlighting" "true"
          set_conf_value "list" "true"
          pluginit=1
          break
          ;;
        "Reset"*,* | *,"Reset"*){:target="_blank"}{:rel="noopener noreferrer"}
          [ -f ${CONFBACK} ] && {
            cp ${CONFBACK} ${NVIMCONF}
            set_code_explain
            set_ranger_float
            set_waka_opt
            pluginit=1
          }
          break
          ;;
        "Open Lazyman",* | *,"Open Lazyman"){:target="_blank"}{:rel="noopener noreferrer"}
          if [ "${USEGUI}" ]; then
            NVIM_APPNAME="nvim-Lazyman" neovide
          else
            NVIM_APPNAME="nvim-Lazyman" nvim
          fi
          break
          ;;
        "Formatters"*,* | *,"Formatters"*){:target="_blank"}{:rel="noopener noreferrer"}
          formenu=1
          break 2
          ;;
        "LSP Servers"*,* | *,"LSP Servers"*){:target="_blank"}{:rel="noopener noreferrer"}
          lspmenu=1
          break 2
          ;;
        "Plugins Menu"*,* | *,"Plugins Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
          plugmenu=1
          break 2
          ;;
        "LazyIde Config",* | *,"LazyIde Config"){:target="_blank"}{:rel="noopener noreferrer"}
          lidemenu=1
          break 2
          ;;
        "Webdev Config",* | *,"Webdev Config"){:target="_blank"}{:rel="noopener noreferrer"}
          wdevmenu=1
          break 2
          ;;
        "Main Menu"*,* | *,"Main Menu"*){:target="_blank"}{:rel="noopener noreferrer"}
          [ "${pluginit}" ] && lazyman -N nvim-Lazyman init
          mainmenu=1
          break 2
          ;;
        "Quit",* | *,"Quit" | "quit",* | *,"quit"){:target="_blank"}{:rel="noopener noreferrer"}
          [ "${pluginit}" ] && lazyman -N nvim-Lazyman init
          printf "\nExiting Lazyman Configuration Menu System\n\n"
          exit 3
          ;;
        *,*){:target="_blank"}{:rel="noopener noreferrer"}
          printf "\nNo matching menu item located."
          printf "\nSelection out of range or malformed."
          prompt_continue
          break
          ;;
      esac
      REPLY=
    done
  done
  [ "${mainmenu}" ] && exit 2
  [ "${plugmenu}" ] && show_plugin_menu
  [ "${lspmenu}" ] && show_lsp_menu
  [ "${formenu}" ] && show_formlint_menu
  [ "${lidemenu}" ] && {
    ${LZYIDE}
    [ $? -eq 3 ] && exit 0
  }
  [ "${wdevmenu}" ] && {
    ${WEBDEV}
    [ $? -eq 3 ] && exit 0
  }
}

debug=
confmenu=
initplugs=
menu="conf"
pluginit=
setconf=
toggle=
while getopts "dim:stu" flag; do
  case $flag in
    d){:target="_blank"}{:rel="noopener noreferrer"}
      debug=1
      ;;
    i){:target="_blank"}{:rel="noopener noreferrer"}
      initplugs=1
      ;;
    m){:target="_blank"}{:rel="noopener noreferrer"}
      menu="${OPTARG}"
      if [ "${menu}" ]
      then
        case "${menu}" in
          conf*|Conf*){:target="_blank"}{:rel="noopener noreferrer"}
            menu="confmenu"
            ;;
          plug*|Plug*){:target="_blank"}{:rel="noopener noreferrer"}
            menu="plugmenu"
            ;;
          lsp*|Lsp*|LSP*){:target="_blank"}{:rel="noopener noreferrer"}
            menu="lspmenu"
            ;;
          for*|For*|lint*|Lint*){:target="_blank"}{:rel="noopener noreferrer"}
            menu="formenu"
            ;;
          *){:target="_blank"}{:rel="noopener noreferrer"}
            menu="main"
            ;;
        esac
      else
        menu="confmenu"
      fi
      ;;
    s){:target="_blank"}{:rel="noopener noreferrer"}
      setconf=1
      ;;
    t){:target="_blank"}{:rel="noopener noreferrer"}
      toggle=1
      ;;
    u){:target="_blank"}{:rel="noopener noreferrer"}
      usage
      ;;
    *){:target="_blank"}{:rel="noopener noreferrer"}
      printf "\nUnrecognized option. Exiting.\n"
      usage
      ;;
  esac
done
shift $((OPTIND - 1)){:target="_blank"}{:rel="noopener noreferrer"}

set_haves

[ "${toggle}" ] && {
  [ "$1" ] || {
    printf "\nThe -t option requires a configuration name argument."
    usage
  }
  curval=$(get_conf_value "$1"){:target="_blank"}{:rel="noopener noreferrer"}
  case ${curval} in
    true){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "$1" "false"
      ;;
    false){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "$1" "true"
      ;;
    onno){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "$1" "free"
      ;;
    free){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "$1" "onno"
      ;;
    neo-tree){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "$1" "nvim-tree"
      ;;
    nvim-tree){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "$1" "neo-tree"
      ;;
    hop){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "$1" "leap"
      ;;
    leap){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "$1" "hop"
      ;;
    persistence){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "$1" "possession"
      ;;
    possession){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "$1" "persistence"
      ;;
    preview){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "$1" "peek"
      ;;
    peek){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "$1" "preview"
      ;;
    bubble){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "$1" "arrow"
      ;;
    arrow){:target="_blank"}{:rel="noopener noreferrer"}
      set_conf_value "$1" "bubble"
      ;;
    *){:target="_blank"}{:rel="noopener noreferrer"}
      printf "\nUnrecognized configuration toggle: $1\n"
      usage
      ;;
  esac
  [ "${initplugs}" ] || exit 0
}

[ "${setconf}" ] && {
  [ "$1" ] || {
    printf "\nThe -s option requires configuration name and value arguments."
    usage
  }
  [ "$2" ] || {
    printf "\nThe -s option requires configuration name and value arguments."
    usage
  }
  if [ "$1" == "get" ]
  then
    get_conf_value "$2"
    exit 0
  else
    set_conf_value "$1" "$2"
  fi
  [ "${initplugs}" ] || exit 0
}

[ "${initplugs}" ] && {
  set_code_explain
  set_ranger_float
  set_waka_opt
  exit 0
}

# Source the Lazyman shell initialization for aliases and nvims selector
# shellcheck source=~/.config/lazyman/Lazyman/.lazymanrc
[ -f ~/.config/lazyman/Lazyman/.lazymanrc ] && source ~/.config/nvim-Lazyman/.lazymanrc

if [ "$menu" ]; then
  if [ "$menu" == "confmenu" ]; then
    show_conf_menu
  else
    if [ "$menu" == "plugmenu" ]; then
      show_plugin_menu
    else
      if [ "$menu" == "lspmenu" ]; then
        show_lsp_menu
      else
        if [ "$menu" == "formenu" ]; then
          show_formlint_menu
        else
          show_conf_menu
        fi
      fi
    fi
  fi
else
  show_conf_menu
fi

exit 0
```

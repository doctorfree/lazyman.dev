---
title: Lazyman Features
author: doctorfree
date: 2023-08-22 15:25:00 +0800
tags: [nvims, neovim, fuzzy, config, features, lazyman]
pin: true
img_path: "/posts/20230822"
---

## Lazyman Command Features

- `lazyman` command to easily install, initialize, manage, and explore multiple Neovim configurations
- support for `Lazy`, `Packer`, and `vim-plug` plugin managers (`dein` for `SpaceVim` only)
- open, install, remove, get info, search plugins, all from the command line or main menu
- automated installation of dependencies, tools, language servers, and Neovim 0.9+
- install and manage the `Bob` neovim version manager via a menu interface
- richly configured `Lazyman` Neovim configuration
- interactive menu interface for ease of management
  - manage the `Lazyman`, `LazyIde`, and `Webdev` configs via menus
  - perform health checks and generate a status report via menus
- convenience shell functions and aliases with fuzzy search and selection
  - `nvims` and `neovides` shell functions to fuzzy search, select, and open Neovim configs
  - enhanced `less` command alias
  - enhanced `ls` command alias
  - `tree` alias to display a tree view of files and folders
  - `tldrf` alias to fuzzy search, select, and preview cheat sheets
- vimdoc help for `Lazyman` with `:h Lazyman` or `,hl`
- vimdoc help for `nvims` with `:h Nvims` or `,hn`
- vimdoc help for `Lazyman` keymaps with `:h Lazyman-Keymaps` or `,hk`
- over 100 supported Neovim configurations out of the box, additional custom configs

See the [Usage](https://lazyman.dev/usage) section for details on `lazyman` command usage.

## The nvims fuzzy selector

The `lazyman` installation and configuration automatically configures
convenience aliases and shell functions for Lazyman installed Neovim
configurations. One of these is the `nvims` shell function which dynamically
creates a fuzzy searchable menu of installed Neovim configurations and launches
Neovim with the selected Lazyman Neovim configuration.

See `~/.config/nvim-Lazyman/.lazymanrc`.

Similarly, a `neovides` shell function can be used to select a Neovim
configuration for use with the Neovim GUI `neovide`.

The fuzzy searchable/selectable menu of Neovim configurations can also
be shown with the command `lazyman -S`. Note also that both the `nvims`
shell function and the `lazyman -S` command can accept additional filename
arguments which are then passed to Neovim. For example, to edit
`/tmp/foo.lua` with a Neovim configuration selected from the `nvims` menu:

```bash
nvims /tmp/foo.lua
```

See [Neovim Configuration Fuzzy Selector](https://lazyman.dev/posts/Nvims) for
additional details on use of the `nvims` and `neovides` shell functions.

## Menu Configuration Management

Lazyman provides a character-based menu system which includes menu management
of several Neovim configurations. Menu configuration management is supported
for the following Lazyman Neovim configurations:

- [Lazyman Neovim configuration](https://lazyman.dev/info/Lazyman.html)
- [LazyIde Neovim configuration](https://lazyman.dev/info/LazyIde.html)
- [Webdev Neovim configuration](https://lazyman.dev/info/Webdev.html)

To view the Lazyman Configuration Menu, select the `Lazyman Config` option
from the main menu or execute the command:

```shell
lazyman -F
```

If the `LazyIde` or `Webdev` Neovim configurations have been installed
then menu entries will be presented for `LazyIde Config` and `Webdev Config`.

Command line arguments can be used to open Lazyman menus directly. For example,
to open the Lazyman plugins configuration menu directly from the command line,
execute the command `lazyman -F plugins`.

The following command line menu entry points are supported:

- `lazyman -F config`
  - Lazyman Neovim configuration menu
- `lazyman -F plugins`
  - Lazyman plugins configuration menu
- `lazyman -F lsp`
  - Lazyman language server configuration menu
- `lazyman -F format`
  - Lazyman formatters and linters configuration menu
- `lazyman -F lazyide`
  - LazyIde Neovim configuration menu
- `lazyman -F webdev`
  - Webdev Neovim configuration menu

Neovim configuration options, settings, formatters, linters, language servers,
and plugins can be managed via these menus.

## [Get configuration script](https://lazyman.dev/info/get_conf.html)

Neovim 0.9 introduced a new feature which allows execution of Lua scripts
in Neovim from the shell command line. The `lazyman` configuration menu
interface uses this new feature to get the current Lazyman Neovim
configuration with shell commands like:

```bash
GET_CONF="${HOME}/.config/nvim-Lazyman/scripts/get_conf.lua"
confval=$(NVIM_APPNAME="nvim-Lazyman" nvim -l ${GET_CONF} ${confname} 2>&1)
```

The [get_conf.lua](https://lazyman.dev/info/get_conf.html) script can also
be used to retrieve option or variable settings in any Neovim configuration.
For example, to retrieve the value of the 'mouse' option in the `Webdev`
Neovim configuration:

```bash
GET_CONF="${HOME}/.config/nvim-Lazyman/scripts/get_conf.lua"
NVIM_APPNAME="nvim-Webdev" nvim -l ${GET_CONF} mouse
```

## Lazyman source code

The convenience script to install and initialize `Lazyman` is provided by
[lazyman.sh](https://lazyman.dev/info/lazyman_command.html).

## Install neovim and tools

The `lazyman` command checks for a current version of Neovim and, if not found
or if the existing version is less than 0.9, invokes the `install_neovim.sh`
script to install Neovim, dependencies, language servers, and tools.

Not all language servers and tools are installed. If additional language
support is desired, it can usually be provided by Mason or native package
installation. For example, to provide support for `composer`, `php`, `julia`,
and `luarocks` run `lazyman -I`.

The automated install and initialization is performed by `lazyman` and
[install_neovim.sh](https://lazyman.dev/info/install_neovim).

## Lazyman Neovim Configuration Features

<div align="center"><p>
    <a href="https://dotfyle.com/doctorfree/nvim-lazyman"><img src="https://dotfyle.com/doctorfree/nvim-lazyman/badges/plugins?style=flat" alt="Plugins"/></a>
    <a href="https://dotfyle.com/doctorfree/nvim-lazyman"><img src="https://dotfyle.com/doctorfree/nvim-lazyman/badges/leaderkey?style=flat" alt="Leader"/></a>
    <a href="https://dotfyle.com/doctorfree/nvim-lazyman"><img src="https://dotfyle.com/doctorfree/nvim-lazyman/badges/plugin-manager?style=flat" alt="Manager"/></a>
</p><p>
  <img src="https://raw.githubusercontent.com/wiki/doctorfree/nvim-lazyman/screenshots/lazyman-plugins.png" alt="Plugins" style="width:850px;height:531px;">
</p></div>

### General

The Lazyman Neovim configuration can be managed via the `lazyman` menu
system. When managing the Lazyman Neovim configuration, the `lazyman`
command invokes
[scripts/lazyman_config.sh](https://lazyman.dev/info/lazyman_config.html).

In addition to the menu configuration management, the following features
are supported:

- Package management and plugin configuration via [lazy.nvim](https://github.com/folke/lazy.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
- Easily configure namespace, theme, active plugins, and their configuration via `configuration.lua`
- [Multiple namespaces](#multiple-namespace-support), it is really 3 configurations in one. Switch between namespaces with the `conf.namespace` setting in `lua/configuration.lua` or via the Lazyman menu system (`lazyman -F`).
- Preconfigured themes: [catppuccin](https://github.com/catppuccin/nvim){:target="\_blank"}{:rel="noopener noreferrer"}, [tokyonight](https://github.com/folke/tokyonight.nvim){:target="\_blank"}{:rel="noopener noreferrer"}, [nightfox](https://github.com/EdenEast/nightfox.nvim){:target="\_blank"}{:rel="noopener noreferrer"}, [tundra](https://github.com/sam4llis/nvim-tundra){:target="\_blank"}{:rel="noopener noreferrer"}, [dracula](https://github.com/Mofiqul/dracula.nvim){:target="\_blank"}{:rel="noopener noreferrer"}, [kanagawa](https://github.com/rebelot/kanagawa.nvim){:target="\_blank"}{:rel="noopener noreferrer"}, [onedarkpro](https://github.com/olimorris/onedarkpro.nvim){:target="\_blank"}{:rel="noopener noreferrer"}, [everforest](https://github.com/neanias/everforest-nvim){:target="\_blank"}{:rel="noopener noreferrer"}, [monokai-pro](https://github.com/loctvl842/monokai-pro.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
  - Keymap to toggle transparency for several color schemes (`,ut`)
- AI developer assistants:
  - Support for [Github Copilot](https://github.com/features/copilot){:target="\_blank"}{:rel="noopener noreferrer"} with completions
  - Support for ChatGPT using [ChatGPT.nvim](https://github.com/jackMort/ChatGPT.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
    - Uses ChatGPT prompts from [Awesome ChatGPT Prompts](https://github.com/f/awesome-chatgpt-prompts){:target="\_blank"}{:rel="noopener noreferrer"}
  - Support for [Neoai](https://github.com/Bryley/neoai.nvim){:target="\_blank"}{:rel="noopener noreferrer"} plugin for OpenAI's GPT-4
- Auto-configure [codeexplain.nvim](https://github.com/mthbernardes/codeexplain.nvim){:target="\_blank"}{:rel="noopener noreferrer"} (GPT4ALL) if the GPT model is found
  - Lazyman menu provides auto-download and setup (requires Python 3.9 or greater)
  - This plugin is new and experimental. Unlike ChatGPT, it uses a self-hosted model and requires no API key or money
- Custom Lazyman Cheat Sheets using [cheatsheet.nvim](https://github.com/sudormrfbin/cheatsheet.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
  - `:Cheatsheet` command, fuzzy search `lazyman` for custom Lazyman keymaps
- Mnemonic keyboard mappings inspired by [Spacemacs](https://www.spacemacs.org/){:target="\_blank"}{:rel="noopener noreferrer"} via [which-key.nvim](https://github.com/folke/which-key.nvim){:target="\_blank"}{:rel="noopener noreferrer"}; no more than three keystrokes for each keybinding
- Replace the UI for messages, cmdline and popup menu via [noice.nvim](https://github.com/folke/noice.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
- Fully featured status line via [lualine](https://github.com/nvim-lualine/lualine.nvim){:target="\_blank"}{:rel="noopener noreferrer"} and [tabline](https://github.com/kdheepak/tabline.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
- Terminal integration via [nvim-toggleterm.lua](https://github.com/akinsho/nvim-toggleterm.lua){:target="\_blank"}{:rel="noopener noreferrer"}
- [Terminal management](#lazyman-neovim-terminal) via [terminal.nvim](https://github.com/rebelot/terminal.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
  - Preconfigured Neovim terminal execution of `lazyman` command (`<leader>lm`)
  - Preconfigured Neovim terminal execution of `asciiville` command (`<leader>A`)
  - Preconfigured Neovim terminal execution of `htop` command (`<leader>H`)
- Fancy notifications via [nvim-notify](https://github.com/rcarriga/nvim-notify){:target="\_blank"}{:rel="noopener noreferrer"}
- Code diagnostics via [LSP](https://github.com/neovim/nvim-lspconfig){:target="\_blank"}{:rel="noopener noreferrer"}
- Choice of preconfigured dashboard: [alpha](https://github.com/goolord/alpha-nvim){:target="\_blank"}{:rel="noopener noreferrer"} (default), [dashboard-nvim](https://github.com/nvimdev/dashboard-nvim){:target="\_blank"}{:rel="noopener noreferrer"}, or [mini.starter](https://github.com/echasnovski/mini.nvim/blob/main/readmes/mini-starter.md){:target="\_blank"}{:rel="noopener noreferrer"}
- Git management with [Lazygit](https://github.com/jesseduffield/lazygit){:target="_blank"}{:rel="noopener noreferrer"}, custom telescope commits view with [git-delta](https://github.com/dandavison/delta){:target="_blank"}{:rel="noopener noreferrer"}, [gitsigns](https://github.com/lewis6991/gitsigns.nvim){:target="_blank"}{:rel="noopener noreferrer"} & [diffview](https://github.com/sindrets/diffview.nvim){:target="_blank"}{:rel="noopener noreferrer"}, custom git blame
- Neovim games for fun and learning ([Sudoku](https://github.com/jim-fx/sudoku.nvim){:target="\_blank"}{:rel="noopener noreferrer"}, [Blackjack](https://github.com/alanfortlink/blackjack.nvim){:target="\_blank"}{:rel="noopener noreferrer"}, [vim-be-good](https://github.com/ThePrimeagen/vim-be-good){:target="\_blank"}{:rel="noopener noreferrer"} practice basic movements, and more).
  - Key map `<leader>G` (e.g. `,G`) displays the available games and amusements.
- Github actions to publish docker image on Docker Hub, check spelling/syntax, and auto-generate vim help doc (see `.github/workflows/*.yml`)
- Over 100 plugins with custom configuration and management via menu system

### Namespace `candy` features

In addition to the above general features, the `candy` namespace of the Lazyman
Neovim configuration includes the following features:

- Beautiful and functional custom statusline built with [galaxyline.nvim](https://github.com/glepnir/galaxyline.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- Configured for TypeScript Development (React.js, Next.js, Vue.js, Angular, Node.js etc.)
- Support for [TailwindCSS](https://tailwindcss.com/){:target="_blank"}{:rel="noopener noreferrer"} with highlighted colors
- JSON autocompletion for most popular Frontend configs
- NPM packages autocompletion in _package.json_
- Internal [Jest](https://github.com/facebook/jest){:target="_blank"}{:rel="noopener noreferrer"} testing and [Coverage](https://github.com/andythigpen/nvim-coverage){:target="_blank"}{:rel="noopener noreferrer"} support
- Debugging with [nvim-dap](https://github.com/mfussenegger/nvim-dap){:target="_blank"}{:rel="noopener noreferrer"} (works with React.js & React Native)
- Automatic Treesitter-based folding with imports folded by default
- Current code context via [nvim-navic](https://github.com/SmiteshP/nvim-navic){:target="_blank"}{:rel="noopener noreferrer"}

### Lazyman configuration plugins list and language server support

See [Lazyman Configuration Plugins and Servers](https://lazyman.dev/posts/Lazyman-Plugins-Servers)
for listings and descriptions of plugins and language servers used by the Lazyman
Neovim configuration.

### Navigation

<div><p>
  <img
  src="https://raw.githubusercontent.com/wiki/doctorfree/nvim-lazyman/screenshots/alpha.png"
  alt="alpha"
  style="width:680px;height:610px;">
</p></div>

- [Telescope.nvim](https://github.com/nvim-telescope/telescope.nvim){:target="\_blank"}{:rel="noopener noreferrer"} for all your search needs
- Project management with [Project.nvim](https://github.com/ahmedkhalf/project.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
- File tree navigation/manipulation via [neo-tree](https://github.com/nvim-neo-tree/neo-tree.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
- Better Tmux navigation with your home row via [Navigator.nvim](https://github.com/numToStr/Navigator.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
- Convenient jumping through windows with [nvim-window-picker](https://gitlab.com/s1n7ax/nvim-window-picker){:target="\_blank"}{:rel="noopener noreferrer"}

### Coding

<div><p>
  <img src="https://raw.githubusercontent.com/wiki/doctorfree/nvim-lazyman/screenshots/diagnostics.png" style="width:800px;height:600px;">
</p></div>

- Auto completion powered by [nvim-cmp](https://github.com/hrsh7th/nvim-cmp){:target="\_blank"}{:rel="noopener noreferrer"}
- Built-in LSP configured via [nvim-lspconfig](https://github.com/neovim/nvim-lspconfig){:target="\_blank"}{:rel="noopener noreferrer"}, [mason](https://github.com/williamboman/mason.nvim){:target="\_blank"}{:rel="noopener noreferrer"}, and [mason-lspconfig](https://github.com/williamboman/mason-lspconfig.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
- Debugging for Go and Python via [nvim-dap](https://github.com/mfussenegger/nvim-dap){:target="\_blank"}{:rel="noopener noreferrer"} and friends
- [Treesitter](https://github.com/nvim-treesitter/nvim-treesitter){:target="\_blank"}{:rel="noopener noreferrer"} and [Tresitter-textobjects](https://github.com/nvim-treesitter/nvim-treesitter-textobjects){:target="\_blank"}{:rel="noopener noreferrer"} for your syntax needs
- Auto formatting via [null-ls.nvim](https://github.com/jose-elias-alvarez/null-ls.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
- Excellent Go support via LSP and [go.nvim](https://github.com/ray-x/go.nvim){:target="\_blank"}{:rel="noopener noreferrer"} including sensible keybindings
- Always know where you are in your code via [nvim-navic](https://github.com/SmiteshP/nvim-navic){:target="\_blank"}{:rel="noopener noreferrer"}
- Git integration via [Neogit](https://github.com/TimUntersberger/neogit){:target="\_blank"}{:rel="noopener noreferrer"} and [gitsigns](https://github.com/lewis6991/gitsigns.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
- Outlining symbols with [symbols-outline.nvim](https://github.com/simrat39/symbols-outline.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
- Snippets provided by [Luasnip](https://github.com/L3MON4D3/LuaSnip){:target="\_blank"}{:rel="noopener noreferrer"} and [friendly snippets](https://github.com/rafamadriz/friendly-snippets){:target="\_blank"}{:rel="noopener noreferrer"} with autocompletion
- Auto-install and setup of dozens of language servers including: `ansiblels`, `astro`, `awk_ls`, `bashls`, `clangd`, `ccls`, `cmake`, `cssmodules_ls`, `denols`, `dockerls`, `eslint`, `gopls`, `graphql`, `html`, `jdtls`, `jsonls`, `julials`, `lua_ls`, `ltex`, `marksman`, `pylsp`, `pyright`, `rust_analyzer`, `sqlls`, `svelte`, `tailwindcss`, `taplo`, `texlab`, `tflint`, `tsserver`, `vimls`, `yamlls`

#### Go development

<div align="center"><p>
<img src="https://raw.githubusercontent.com/wiki/doctorfree/nvim-lazyman/screenshots/go-dev.png" style="width:1152px;height:635px;">
</p>
</div>

#### Debugging via DAP

<div align="center"><p>
<img src="https://raw.githubusercontent.com/wiki/doctorfree/nvim-lazyman/screenshots/dap.png" style="width:1152px;height:635px;">
</p>
</div>

### Lazyman Neovim Terminal

The `Lazyman` Neovim configuration includes Neovim Terminal management via
[terminal.nvim](https://github.com/rebelot/terminal.nvim){:target="\_blank"}{:rel="noopener noreferrer"}. This Neovim terminal
is preconfigured for execution of the `lazyman` command. A shortcut key
binding to execute `lazyman` in a Neovim terminal has also been provided:
(`<leader>lm`). While in Neovim with the default `nvim-Lazyman` configuration,
pressing `,lm` will execute the `lazyman` command in a Neovim floating terminal
window. Alternately, executing the Neovim command `:Lazyman` will also
bring up the `lazyman` command in a Neovim terminal.

If [Asciiville](https://github.com/doctorfree/Asciiville){:target="\_blank"}{:rel="noopener noreferrer"} is installed,
pressing `,A` or executing the `:Asciiville` Neovim command will execute
the `asciiville` command in a Neovim floating terminal window.

If the `htop` command is available, `:Htop` will execute the `htop` system
monitor in a floating Neovim terminal window.

This preconfigured Neovim terminal capability is only available in the
`Lazyman` Neovim configuration and not in the other configs.

### Multiple namespace support

The Lazyman Neovim configuration supports multiple namespaces, each of which
has its own separate and distinct configuration, options, plugins, and style.

Use the Lazyman configuration menu to select a namespace (`lazyman -F`).

The default namespace is `free`. This was the traditional namespace used by
all previous versions of Lazyman:

<div align="center"><p>
<img src="https://raw.githubusercontent.com/wiki/doctorfree/nvim-lazyman/screenshots/free.png" style="width:1040px;height:643px;">
</p>
</div>

The `onno` namespace is based on the `ONNO` Lazyman Neovim configuration:

<div align="center"><p>
<img src="https://raw.githubusercontent.com/wiki/doctorfree/nvim-lazyman/screenshots/onno.png" style="width:1040px;height:643px;">
</p>
</div>

The `candy` namespace is based on the `Ecovim` Lazyman Neovim configuration:

<div align="center"><p>
<img src="https://raw.githubusercontent.com/wiki/doctorfree/nvim-lazyman/screenshots/candy.png" style="width:1040px;height:643px;">
</p>
</div>

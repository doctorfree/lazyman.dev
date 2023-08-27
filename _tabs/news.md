---
layout: post
icon: fas fa-plus-circle
order: 4
toc: true
post_style: page
---

# Lazyman Neovim Configuration Manager News

## Installation location

Beginning with Lazyman version 4 the Lazyman installation location has moved
from `~/.config/nvim-Lazyman` to `~/.config/lazyman/Lazyman`. In addition,
all Neovim configurations installed with `lazyman` are located in
`~/.config/lazyman/`. This change was motivated by the clutter of over 100
Neovim configurations all located in `~/.config/`.

Note that the `NVIM_APPNAME` environment variable must now contain the
`lazyman/...` prefix. For example, to reference the Neovim configuration
located in `~/.config/lazyman/Abstract` set `NVIM_APPNAME="lazyman/Abstract"`.

### Migration support

Users updating Lazyman from version 3 or earlier to version 4 via `lazyman -U`
can perform a migration of any previously installed Neovim configurations.
The first time `lazyman` is run after updating it will prompt for migration
if any previously installed Neovim configurations are found.

If migration is initially skipped it can be performed later with `lazyman migrate`.

## Supported configurations information documents

Each Lazyman supported Neovim configuration now has an
information document providing configuration details at
[https://lazyman.dev/info](https://lazyman.dev/info).

## Lazyman configuration category websites

Lazyman supported configurations using popular Neovim configuration
frameworks are now detailed in newly available websites. These include:

- [AstroNvim configurations](https://astronvim.lazyman.dev)
- [LazyVim configurations](https://lazyvim.lazyman.dev)
- [LunarVim configurations](https://lunarvim.lazyman.dev)
- [NvChad configurations](https://nvchad.lazyman.dev)

## New features, fixes, and improvements

Recent releases of `lazyman` include several new features, fixes, and improvements:

- Information documents for each supported Neovim configuration which include:
  - Installation command, install location, brief description
  - Links to relevant websites including the Github repo, website, YouTube, etc
  - List of plugins included in each configuration
  - Table of keymaps defined in each configuration
- New configuration categories: `LazyVim`, `AstroNvim`, `NvChad`, `LunarVim`
  - Easily install all supported configurations using one of these frameworks
- Easy menu navigation and command line usage with keywords
  - `lazyman` command line now supports `open`, `install`, `info` arguments
    - `lazyman open` to fuzzy select a config to open
    - `lazyman install` to fuzzy select a config to install
    - `lazyman info` to fuzzy select a config to display info
  - Menu interface also supports keywords to fuzzy select a config for an action
  - Additional keywords supported: `health`, `init`, `remove`, `search`, `status`
- Auto-install of [Bob](https://github.com/MordechaiHadad/bob){:target="_blank"}{:rel="noopener noreferrer"} Neovim version manager (optional)
- Multiple namespace support in `Lazyman` default `lazyman` Neovim configuration
  - Select which namespace to use in `lua/configuration.lua` or via the menu interface
  - Both namespaces can be configured vi the Lazyman configuration menus (`lazyman -F`)
- `LazyIde` and `Webdev` configurations now configurable via a menu interface
- Fuzzy select a configuration for a health check
- Improved [get_conf.lua](#get-configuration-script) can return option or variable value
- Search for plugins and get a list of supported configurations using that plugin

## Improved nvims shell function

The `nvims` shell function is sourced at login and when `lazyman` is executed.
It provides a fuzzy search and select facility to easily open, remove, or get
info on a Lazyman installed Neovim configuration. Several new features have
recently been added to `nvims` and its companion shell function `neovides`.

In addition to the command line arguments and usage described below, when a
Neovim configuration is selected for opening with `nvims` that selection is
"sticky". That is, an alias for `vi` is created which will use the previously
selected `nvims` configuration for subsequent invocations of `vi`.

Here is the current usage message for `nvims`:

```
Usage: nvims [-c cmd] [-C fltr] [-I] [-R] [-S file] [-U] [file1 [file2] ...]
 '-c cmd' : 'Ex' command to be executed after first file read
 '-C fltr' : filter to use when generating the list to select from
 '-I' : display the selected configuration information document
 '-R' : indicates removal of the selected Neovim configuration
 '-S file' : Executes 'Vimscript' or 'Lua' in 'file' after file read
  '~/.config/lazyman/Lazyman/overrides.lua' is used if not empty
 '-U' : displays a usage message and exits

Examples:
 nvims
  Opens Neovim using the selected configuration
 nvims main.cpp
  Opens 'main.cpp' with Neovim using the selected configuration
 nvims -C lazy
  Opens Neovim using the configuration selected from those
  with names containing the case insensitive string 'lazy'
 nvims -I
  Displays information for the selected Neovim configuration
 nvims -R
  Removes the selected Neovim configuration
```

More info and source code listing for `nvims` can be found in the
[Lazyman Wiki](https://github.com/doctorfree/nvim-lazyman/wiki/Nvims){:target="_blank"}{:rel="noopener noreferrer"}.

## Get configuration script

Neovim 0.9 introduced a new feature which allows execution of Lua scripts
in Neovim from the shell command line. The `lazyman` configuration menu
interface uses this new feature to get the current Lazyman Neovim
configuration with shell commands like:

```bash
GET_CONF="${HOME}/.config/lazyman/Lazyman/scripts/get_conf.lua"
confval=$(NVIM_APPNAME="lazyman/Lazyman" nvim -l ${GET_CONF} ${confname} 2>&1)
```

The `get_conf.lua` script can also be used to retrieve option or variable
settings in any Neovim configuration. For example, to retrieve the value of
the 'mouse' option in the `Webdev` Neovim configuration:

```bash
GET_CONF="${HOME}/.config/lazyman/Lazyman/scripts/get_conf.lua"
NVIM_APPNAME="lazyman/Webdev" nvim -l ${GET_CONF} mouse
```

The Lazyman `get_conf.lua` script:

```lua
-- Invoke with 'nvim -l get_conf.lua conf_name'
-- Where 'conf_name' is:
--   - one of the entries in lua/configuration.lua
--   - the keyword 'config_home' to get configuration location info
--   - an option/variable name to retrieve its value
--
-- For example, to retrieve the Lazyman configuration 'namespace' setting:
--
-- #!/bin/bash
-- NVIM_APPNAME="lazyman/Lazyman" \
--   nvim -l ~/.config/lazyman/Lazyman/scripts/get_conf.lua namespace
--
-- or, to retrieve the value of the 'mouse' option in the Webdev config:
--
-- #!/bin/bash
-- NVIM_APPNAME="lazyman/Webdev" \
--   nvim -l ~/.config/lazyman/Lazyman/scripts/get_conf.lua mouse

local config = vim.inspect(_G.arg[1])
local arg = string.gsub(config, '"', "")
local app_name = os.getenv("NVIM_APPNAME") or ""

local function get_var(var_name, default_value)
  local s, v = pcall(function()
    return vim.api.nvim_get_option(var_name)
  end)
  if s then
    return v
  else
    s, v = pcall(function()
      return vim.api.nvim_get_var(var_name)
    end)
    if s then
      return v
    else
      return default_value
    end
  end
end

local function print_var(entry)
  if type(entry) == "string" then
    io.write(entry .. "\n")
  elseif type(entry) == "table" then
    table.sort(entry)
    for _, val in ipairs(entry) do
      io.write(val .. "\n")
    end
  else
    io.write(tostring(entry) .. "\n")
  end
end

if arg == "config_home" then
  local config_home = vim.fn.stdpath("config")
  io.write("Neovim configuration location = " .. vim.fn.expand(config_home) .. "\n")
  io.write("NVIM_APPNAME = " .. app_name .. "\n")
else
  local var_val = ""
  if app_name == "lazyman/Lazyman" then
    local settings = require("configuration")
    local entry = settings[arg]
    if entry ~= nil then
      print_var(entry)
    else
      var_val = get_var(arg, "")
      print_var(var_val)
    end
  else
    var_val = get_var(arg, "")
    print_var(var_val)
  end
end
```

Pretty simple, huh? Thanks Neovim!

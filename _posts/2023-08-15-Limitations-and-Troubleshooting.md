---
title: Known Limitations and Troubleshooting
author: doctorfree
date: 2023-08-15 16:20:00 +0800
tags: [limits, debug, trouble, lazyman, nvims, neovim, config]
pin: true
img_path: "/posts/20230815"
---

## Known limitations

### Interactive Neovim Configuration Initialization

Lazyman does not support automatic initialization of interactive configurations.
If the initialization process is interactive, the auto initialization will hang.
Some effort is made to detect an interactive initialization and avoid a hung
process. For example, if the configuration includes the
[WakaTime metrics plugin](https://github.com/wakatime/vim-wakatime) and no
WakaTime configuration is detected then the user is prompted before continuing.
Other configurations that prompt for an example config are handled by Lazyman
but some custom configurations not yet supported by Lazyman may hang during
initialization if they prompt for input.

If the initialization process takes more than a few minutes it can be terminated
with `Ctrl-c`. After termination the configuration can be manually initialized:

```bash
NVIM_APPNAME="<nvim dir>" nvim
```

### External Configuration Dependencies

Neovim configurations often rely on external commands, utilities, language
servers, formatters, linters, and tools. The `Lazyman` initialization process
installs much of what might be required but not all. Some configurations
may initialize cleanly but subsequent use might provoke an error when an
external dependency is not available. For example, the `Shuvro` Neovim
configuration relies upon an externally installed `luacheck` facility. If this
is not available then `Shuvro` will emit an error message when opening
`lua` files. Most commonly used external dependencies are installed by
`lazyman` but missing dependencies sometimes occur.

### Lazyman Neovim Configuration

The installation of some programming languages is left to the system
administrator. In particular, `lazyman` does not install Go, Java, the
Java Development Kit (JDK), Composer, PHP, or Julia. These may show
up as warnings when performing a `:checkhealth` and can be installed
manually if needed. Some additional tools can be installed with `lazyman -I`.

SSH users may need to install
[lemonade](https://github.com/lemonade-command/lemonade)
to support the clipboard over SSH.

If `go` is not installed or incorrectly configured then the Mason installs
of `goimports`, `gopls`, and `gofumpt` will fail.

The `dashboard-nvim` dashboard may display the tabline after performing some
dashboard actions.

Changing the configured dashboard from within Neovim via the Terminal display
of the `lazyman` menu system will not take effect until a restart of Neovim.

### Updating lazyman

An update of the Lazyman configuration and `lazyman` command can be performed
with the command `lazyman -U`. However, early releases of Lazyman always
preserve any existing `~/.config/nvim-Lazyman/lua/configuration.lua`. Later
releases of Lazyman include a different format for this file. When updating
from an older Lazyman release it may be necessary to run the update twice.

### Homebrew

Homebrew can be used to install Neovim dependencies and tools by using the
`-h` switch to `lazyman` or by selecting Homebrew when prompted. Using
Homebrew on some Linux systems has the advantage of providing more recent
versions of some packages. However, the Homebrew python package will be
installed as a dependency and will appear first in your PATH. This results
in a system which no longer recognizes previously installed python modules
in the system python. This issue has been reported to the Homebrew team
but is unlikely to be addressed.

If you wish to use Homebrew and want to retain your existing python modules
then the following manual process may suffice:

- Locate the module paths the Homebrew python is using. For example:
  - `/home/linuxbrew/.linuxbrew/bin/python3 -c 'import site; print(site.getsitepackages())' | tr -d '[],'`
- Locate the module paths the system python is using. For example:
  - `/usr/bin/python3 -c 'import site; print(site.getsitepackages())' | tr -d '[],'`
- Append the system python module paths to `PYTHONPATH` with Homebrew's first
- Export the constructed `PYTHONPATH` environment variable in your shell init, e.g.
  - `export PYTHONPATH="<colon separated list of paths>"`

This Homebrew python module path issue is not a problem when using the
native package manager to install dependencies and tools. This is the default.

#### Ubuntu 20.04

The version of `luarocks` in the Ubuntu 20.04 default repositories is
no longer supported. If `luarocks` is required then it can be installed
manually by following the instructions in the
[Luarocks documentation](https://luarocks.org/#quick-start). This is not
an issue when using Homebrew to install dependencies.

The binary distribution of the `tree-sitter-cli` npm package depends on GLIBC
2.32 but this is unavailable in this release of Ubuntu Linux. The `tree-sitter`
command is not functional, disabling the `:TSInstallFromGrammar` command.

### Alpine, SUSE, and Void Linux

Due to limited resources, very little testing has been performed on Alpine
Linux, SUSE Linux, or Void Linux. Support for these platforms
was recently introduced and issues are expected. If you encounter a problem
on these platforms please
[open an issue](https://github.com/doctorfree/nvim-lazyman/issues).

### Semantic token highlighting for types containing hyphens

Neovim 0.9 introduced semantic token highlighting but placed some restrictions
on the format of semantic tokens. For example, if a filetype contains a hyphen
then language servers may return semantic tokens that contain a hyphen and this
will generate an error. This issue may cause some configurations to hang or
display errors.

### LaTeX configuration hangs on macOS

The `LaTeX` configuration is hanging on my Mac. It appears to work fine
on Linux platforms. This is currently under investigation.

## Troubleshooting

The most frequent type of issue encountered using `lazyman` to install and
initialize Neovim configurations is incompatibility between the existing
configuration and Neovim supported configuration parameters. Lazyman
uses Neovim 0.9 which includes revised support for several Neovim features.
Many existing Neovim configurations rely on features or configuration
parameters no longer supported in Neovim 0.9.

For example, one of the most frequent issues initializing a Neovim
configuration is the initialization error:

```
Parser not available for language "help"
```

The Treesitter `help` parser was renamed to `vimdoc` and `help` is no longer
supported as a Treesitter parser. These types of changes are called
"breaking changes" and will occur more frequently when using a recent
Neovim build. To correct a `Parser not available for language "help"`
initialization error, locate where in the configuration the Treesitter
`help` parser is set (usually in the `ensure_installed` section of the
Treesitter plugin configuration) and change `help` to `vimdoc`.

See the [Neovim 0.9 release notes](https://github.com/neovim/neovim/releases/tag/v0.9.0)
for an overview of changes. In particular, many of these types of issues
are detailed in the [news.txt for Neovim 0.9](https://github.com/neovim/neovim/blob/040f1459849ab05b04f6bb1e77b3def16b4c2f2b/runtime/doc/news.txt) (`:help news` within nvim).

This is life on the bleeding edge. However, all of the supported Lazyman
Neovim configurations and most of the Personal Neovim configurations supported
by `lazyman` do not have Neovim version incompatibilities.

### Lazyman installation

The installation process requires Neovim 0.9 or later. If not present the
install script will attempt to compile current Neovim from source. This step
can fail for a variety of reasons. Most typically, the Neovim build failure
is due to missing libraries, header files, or development environment
components. To debug a failed Lazyman installation, first run the install
script in debug mode to try and determine the cause of the failure:

```bash
lazyman -d
```

The `lazyman -d` command should run the `install_neovim` script in debug mode
and any errors will be displayed. Alternatively, execute the Neovim install
script directly with `$HOME/.config/nvim-Lazyman/scripts/install_neovim.sh -d`
and view the output for errors.

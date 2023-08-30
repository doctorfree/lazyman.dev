---
layout: post
icon: fas fa-arrow-circle-down
order: 1
toc: true
post_style: page
---

```bash
# Install lazyman with the following two commands:
git clone https://github.com/doctorfree/nvim-lazyman $HOME/.config/nvim-Lazyman
$HOME/.config/nvim-Lazyman/lazyman.sh
```

## Requirements

The [lazyman](https://lazyman.dev/usage) Neovim configuration manager requires
Neovim 0.9. The `lazyman` installation and initialization process checks for
Neovim 0.9 and, if not found, installs it and required dependencies and tools.

Lazyman requires Linux or macOS, git, and the Bash shell version 4 or later.

- Unix/Linux/macOS
- Neovim 0.9 (automatically installed if not found)
- Bash version 4 or later (automatically installed if not found)
- Git

### macOS users

Even the latest versions of macOS ship with Bash 3.2 which dates from 2007.
The Lazyman initialization process will update your system to use a modern
Bash with Homebrew:

```bash
brew install bash
```

The initialization process also makes sure it is found first in your PATH.
For example, `export PATH="/usr/local/bin:${PATH}"` or `export PATH="/opt/homebrew/bin:${PATH}"`.

## Installation

The Lazyman installation process consists of two steps.

Step 1, clone the Lazyman repository:

```bash
git clone https://github.com/doctorfree/nvim-lazyman $HOME/.config/nvim-Lazyman
```

Step 2, initialize the Lazyman Neovim configuration:

```bash
$HOME/.config/nvim-Lazyman/lazyman.sh
```

These 2 steps perform the following:

1. Download the Lazyman Neovim configuration
1. Initialize the Lazyman Neovim configuration which:
   1. Installs language servers and tools for coding diagnostics
   1. Installs the latest version of Neovim if not already installed
   1. Installs and initializes configured Neovim plugins

After the download and initialization are complete, execute the `lazyman`
command found in `~/.local/bin/lazyman`.

By default, Lazyman uses the native package manager to install Neovim
dependencies and tools. Supported native package managers include:

- `apt` or `apt-get` on Debian based platforms (e.g. Ubuntu)
- `dnf` or `yum` on RPM based platforms (Fedora, CentOS, Red Hat)
- `pacman` on Arch Linux and Arch-Like platforms
- `apk` on Alpine Linux
- `xbps-install` on Void Linux
- `zypper` on SUSE Linux

Alternately, command line options exist to direct `lazyman` to install Neovim,
dependencies and tools using
[Homebrew](https://brew.sh){:target="_blank"}{:rel="noopener noreferrer"}
or to skip the Neovim installation altogether. If no supported native package
manager is found then Homebrew is used. Homebrew is always used on macOS.

To install Neovim, dependencies, and tools using Homebrew rather than the
native package manger, invoke `lazyman` with the `-h` option when initializing:

```bash
git clone https://github.com/doctorfree/nvim-lazyman $HOME/.config/nvim-Lazyman
$HOME/.config/nvim-Lazyman/lazyman.sh -h
```

To compile and install the nightly build of Neovim, use the `-H` option:

```bash
git clone https://github.com/doctorfree/nvim-lazyman $HOME/.config/nvim-Lazyman
$HOME/.config/nvim-Lazyman/lazyman.sh -H
```

The installation of Neovim 0.9, language servers, and tools ensures a proper
runtime environment. To avoid the installation of Homebrew, Neovim, language
servers, and tools altogether, execute `lazyman -Z`:

```bash
git clone https://github.com/doctorfree/nvim-lazyman $HOME/.config/nvim-Lazyman
$HOME/.config/nvim-Lazyman/lazyman.sh -Z
```

Note that circumventing the Neovim installation means that Neovim 0.9 must
be installed in some other manner. Also, language servers and tools
required by some Neovim configurations may not be present. However, some
may prefer to handle the installation of Neovim 0.9, language servers,
and tools on their own.

If, after initializing Lazyman with `lazyman -Z`, you wish to let Lazyman
install Neovim 0.9, language servers and tools, then issue the command
`lazyman -I` or choose the `Install Tools` lazyman menu option.

The `lazyman -I` command can also be used to install additional tools, often
resolving some `:checkhealth` warnings.

### Bootstrap

To bootstrap the Lazyman Neovim configuration manager, the
[lazyman.sh](https://lazyman.dev/info/lazyman_command.html) script
must be downloaded and executed. The download can be performed with `git`,
`curl`, `wget`, or a copy/paste.

The recommended bootstrap procedure is with `git`:

Clone the repository with `git` and execute `lazyman.sh`:

```bash
git clone https://github.com/doctorfree/nvim-lazyman $HOME/.config/nvim-Lazyman
$HOME/.config/nvim-Lazyman/lazyman.sh
```

Once the `lazyman.sh` script has been downloaded and executed, subsequent
Lazyman operations can be performed with the `lazyman` command found in
`~/.local/bin/lazyman`. The manual page can be viewed with `man lazyman`.

Neovim 0.9 and later users can use the `NVIM_APPNAME` environment variable
to control where Neovim looks for its configuration.

### Manual installation

If you do not wish to use the automated installation and initialization
provided by the `lazyman.sh` script, manual installation and initialization
can be performed. See the Lazyman Wiki article on
[Manual Installation](https://github.com/doctorfree/nvim-lazyman/wiki/Manual_Installation){:target="_blank"}{:rel="noopener noreferrer"}
to manually install rather than use the automated installation feature of
the `lazyman` command.

## Removal

The `lazyman` command can be used to remove previously installed
Neovim configurations with the `-r` or `-R` command line option.
For example, to remove a previously installed `LazyVim` configuration,
its initialized plugins, state, and cache, execute the following command:

```bash
lazyman -l -r
```

A Neovim configuration managed by `lazyman` can be removed by name:

```bash
lazyman -R -N MagicVim
```

To remove the `Lazyman` configuration and associated plugins, state,
backups, and cache:

```bash
lazyman -R -N Lazyman
```

**WARNING:** removing the `Lazyman` configuration disables `lazyman`
features. Remove `Lazyman` only if you no longer wish to use the Lazyman
Neovim configuration manager.

All `lazyman.sh` operations can be performed as a dry run with `-n`. For
example, to see which `LazyVim` folders would be removed without removing any:

```bash
lazyman -n -l -r
```

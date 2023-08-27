---
layout: post
toc: true
post_style: page
---

<h1 align="center">Lazyman Neovim Configuration Manager</h1>

The Lazyman project can be used to install, initialize, and manage multiple
Neovim configurations. Over 100 popular Neovim configurations are supported.
Lazyman provides a character-based menu interface as well as a weath of
command line options. The Lazyman main menu looks like this:

<div align="center">
  <img
    src="https://github.com/doctorfree/nvim-lazyman/wiki/screenshots/lazymenu.png"
    alt="Lazyman"
    style="width: 965px; height: 528px"
  />
</div>

[See what's new](https://lazyman.dev/news/)

## Overview

Follow the [Installation instructions](https://lazyman.dev/install)
to bootstrap Lazyman. Once Lazyman is installed, execute the
`lazyman` command to manage Neovim configurations. The
`lazyman` command is located in <b>$HOME/.local/bin/lazyman</b>.

The two primary features of the Lazyman project are the
[`lazyman` command](https://lazyman.dev/usage) and the
[`nvims` shell function](https://lazyman.dev/posts/Nvims).
The `lazyman` command provides a menu interface and command line
options to install, initialize, and manage multiple Neovim configurations. The
`nvims` shell function dynamically generates a fuzzy searchable
menu of Neovim configurations from which to select. The selected
configurations can be opened in Neovim, removed, or a configuration
information document can be viewed.

The nvims Neovim configuration fuzzy selector:

<div align="left">
  <img
    src="https://raw.githubusercontent.com/wiki/doctorfree/nvim-lazyman/screenshots/nvims.png"
    alt="nvims"
    style="width: 263px; height: 352px"
  />
  <img
    src="https://raw.githubusercontent.com/wiki/doctorfree/nvim-lazyman/screenshots/nvims2.png"
    alt="nvims"
    style="width: 305px; height: 320px"
  />
</div>

More info on the `nvims` and `neovides` shell functions
can be found in the
[nvims fuzzy selector article](https://lazyman.dev/posts/Nvims) , in
the <b>nvims</b> man page with <b>man nvims</b>, with the command
<b>nvims -U</b>, or in Neovim using the <b>Lazyman</b> configuration with
<b>:h Nvims</b>.

The `lazyman` command separates Neovim configurations into 5 categories:
`Base` `Language` `Personal` `Starter` and `Custom`. The `Base` category
consists of well tested Neovim configurations and distributions, all of which
provide significant value. The `Language` category includes Neovim
configurations tailored for a specific programming or document format
language. The `Personal` category includes personal Neovim
configurations that provide significant value or demonstrate some cool
features. Configurations in the `Personal` category are not
necessarily intended for public use, these repositories are maintained for the
personal use of the authors but are included here for their value. The
`Starter` category includes Neovim configurations tailored to serve
as a starting point for developing your own Neovim configuration. These
include the popular Neovim `Kickstart` configuration, a
`Modern` Neovim config, the `PDE` personal development
environment config, and the Neovim configurations provided by the
<a href="https://github.com/VonHeikemen/nvim-starter" target="_blank" rel="noopener">
nvim-starter project</a>. The `Custom` category includes any additional Neovim
configurations installed and initialized with `lazyman` by the
end-user using the `C url` and `N nvimdir` options.

In addition, Lazyman installs and initializes the Lazyman Neovim
configuration, a richly configured Neovim environment using Lua, Lazy, and
Mason to support highlighting, completion, diagnostics, and more for many
programming languages.

The installation and initialization of Neovim configurations are placed in
separate directories and managed using the
`NVIM_APPNAME` environment variable.

Note that a full installation and initialization of all supported
Neovim configurations, plugins, language servers, formatters, linters,
and tools will consume over 20GB of disk space.

The `lazyman` command is installed as
`local/bin/lazyman` and can be used to install, initialize,
remove, and manage multiple Neovim configurations.

## Requirements and Installation

See the [Install section](https://lazyman.dev/install) for details
on both **Requirements** and **Installation**.

## Supported configurations

See the [Configurations section](https://lazyman.dev/configurations)
for details on **Supported Configurations**.

## Features

See the [Features section](https://lazyman.dev/features)
for details on **Lazyman Features**.

## Usage

See the [Usage section](https://lazyman.dev/usage)
for details on **Lazyman Usage**.

## Motivation

I’m a lazy man. I wanted to try out a bunch of nifty looking Neovim
configurations but I didn’t want to spend a lot of time setting each of them
up and managing them. Instead, I spent a lot of time writing an
install/initialize/manage tool I could use: `lazyman`

Although the primary motivation for creating this project was to provide an
easy way to try out various Neovim configurations, `lazyman` can be
used to setup and manage Neovim configurations tailored for specific purposes.
A Neovim configuration for work, one for school, one for Python development,
another for git repository maintenance and markdown editing, one with language
servers and debugging tools, one for your mom.

It’s also pretty interesting and educational to see how some of these
***Neovim Wizards*** setup their configurations.

### Inspiration

Lazyman was inspired by several Neovim distributions and configurations including:

<ul>
<li><a href="https://github.com/Allaman/nvim.git" target="_blank" rel="noopener">Michael Peter</a></li>
<li><a href="https://github.com/loctvl842/nvim.git" target="_blank" rel="noopener">loctvl</a></li>
<li><a href="https://github.com/mrcjkb/nvim-config.git" target="_blank" rel="noopener">Marc Jakobi</a></li>
<li><a href="https://github.com/LazyVim/LazyVim" target="_blank" rel="noopener">LazyVim</a></li>
<li><a href="https://github.com/LunarVim/LunarVim" target="_blank" rel="noopener">LunarVim</a></li>
<li><a href="https://nvchad.github.io/" target="_blank" rel="noopener">NvChad</a></li>
<li><a href="https://github.com/ray-x/nvim.git" target="_blank" rel="noopener">rayx</a></li>
</ul>

Some of these distributions, like the work of Michael Peter, are released
under an MIT license and I was able to copy directly configuration or
initialization code. Others, like the work of Marc Jakobi, are released under
a more restrictive license and I was only able to use these as reference but
still a valuable aid. I copied my own previous work liberally.

Thanks everybody!

## Info

See the [Info section](https://lazyman.dev/info)
for detailed information on **Lazyman supported configurations**.

## Notes

See the [Notes article](https://lazyman.dev/posts/Notes)
for details on **Lazyman Notes**.

## Removal

See the [Removal section of Install](https://lazyman.dev/install#removal)
for details on **Lazyman Configuration Removal**.

## Known limitations and troubleshooting

See the article
[Known Limitations and Troubleshooting](https://lazyman.dev/posts/Limitations-and-Troubleshooting)
for details on **limitations and debugging**.

<div align="center">
  <h2 id="connect">Connect</h2>
  <p align="center">
    <a href="https://ronrecord.com" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="domain"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/domain.png"
    /></a>
    <a href="https://www.reddit.com/user/No-Blackberry-3160" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="reddit"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/reddit.png"
    /></a>
    <a href="https://github.com/doctorfree" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="github"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/github.png"
    /></a>
    <a href="https://gitlab.com/doctorfree" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="gitlab"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/gitlab.png"
    /></a>
    <a href="https://twitter.com/ronrecord" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="twitter"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/twitter.png"
    /></a>
    <a href="https://youtube.com/c/doctorfree" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="youtube"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/youtube.png"
    /></a>
    <a href="https://linkedin.com/in/ronrecord" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="linkedin"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/linkedin.png"
    /></a>
    <a href="https://instagram.com/doctorfree" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="instagram"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/instagram.png"
    /></a>
    <a href="https://noc.social/@doctorwhen" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="mastodon"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/mastodon.png"
    /></a>
    <a href="https://en.wikipedia.org/wiki/User:Doctorfree" target="_blank" rel="noopener">
      <img align="center"
      style="width:40px;height:40px"
      alt="wikipedia"
      src="https://raw.githubusercontent.com/doctorfree/doctorfree/master/icons/wikipedia.png"
    /></a>
  </p>
</div>

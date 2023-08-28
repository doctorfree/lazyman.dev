---
title: Neovim Configuration Distributions
author: doctorfree
date: 2023-07-20 12:45:00 +0800
tags: [neovim, config, configuration, preconfigured, distribution]
pin: true
img_path: "/posts/20230720"
---

## Introduction

[Neovim](https://neovim.io/) refers to itself as "hyperextensible". Much if not
most of the ability to extend `Neovim` derives from its plugin architecture.
There are hundreds of Neovim plugins, each with its own unique initialization
and configuration, some with duplicate functionality. It can be difficult for
a Neovim user to decide which plugins to use and how to configure each.

Fortunately, there exist many excellent pre-configured and user-extensible
Neovim configuration distributions. However, there are so many good Neovim
configuration distributions that it becomes difficult for a Neovim user to
decide which distribution to use and how to tailor it for their use case.

[Lazyman](https://github.com/doctorfree/nvim-lazyman) attempts to address this
issue by providing several example configurations of many of the Neovim
configuration distributions in an easy-to-install and easy-to-use manner.
Try each distribution out, see how you like it, play with them, extend each
to your liking, settle on one you like and adopt it for your use case(s).

## Top Neovim configuration distributions

By far, the top 5 Neovim configuration distributions are
[AstroNvim](https://github.com/AstroNvim/AstroNvim),
[kickstart](https://github.com/nvim-lua/kickstart.nvim),
[LazyVim](https://github.com/LazyVim/LazyVim),
[LunarVim](https://github.com/LunarVim/LunarVim), and
[NvChad](https://github.com/NvChad/NvChad). That is not to say these are the
"best" configuration distributions, simply that they are the most popular.

Each of these configuration distributions has value. They all provide
excellent starting points for crafting your own custom configuration,
they are all extensible and fairly easy to learn, and they all provide
an out-of-the-box setup that can be used effectively without modification.

Distinguishing features of the top Neovim configuration distributions:

### AstroNvim

- An excellent [community repository](https://github.com/AstroNvim/astrocommunity)
- Fully featured out-of-the-box
- Good documentation

### kickstart

- Minimal out-of-the-box setup
- Easy to extend and widely used as a starting point
- A good choice if your goal is hand-crafting your own config

### LazyVim

- Very well maintained by the author of `lazy.nvim`
- Nice architecture, it's a plugin with which you can `import` preconfigured plugins
- Good documentation

### LunarVim

- Well maintained and mature
- Custom installation processs installs LunarVim in an isolated location
- Been around a while, large community, widespread presence on the web

### NvChad

- Really great `base46` plugin enables easy theme/colorscheme management
- Includes an impressive mappings `cheatsheet`
- `ui` plugin and `nvim-colorizer`

## Distributions included in Lazyman

| **Lazyman**                                             |                    **Included**                     |                    **Neovim**                    |                   **Configuration**                    |                                     **Distributions** |
| :------------------------------------------------------ | :-------------------------------------------------: | :----------------------------------------------: | :----------------------------------------------------: | ----------------------------------------------------: |
| [Abstract](https://github.com/Abstract-IDE/Abstract)    | [AstroNvim](https://github.com/AstroNvim/AstroNvim) | [CodeArt](https://github.com/artart222/CodeArt)  | [CosmicNvim](https://github.com/CosmicNvim/CosmicNvim) |             [Ecovim](https://github.com/ecosse3/nvim) |
| [kickstart](https://github.com/nvim-lua/kickstart.nvim) |    [LazyVim](https://github.com/LazyVim/LazyVim)    | [LunarVim](https://github.com/LunarVim/LunarVim) |      [LvimIde](https://github.com/lvim-tech/lvim)      | [mini.nvim](https://github.com/echasnovski/mini.nvim) |
| [NormalNvim](https://github.com/NormalNvim/NormalNvim)  |     [NvChad](https://github.com/NvChad/NvChad)      |  [NvPak](https://github.com/EvolveBeyond/NvPak)  |            [SpaceVim](https://spacevim.org)            |                                                       |

## Distributions not yet included in Lazyman

| **Excluded**                                                  |                       **Neovim**                        |                      **Configuration**                       |                                            **Distributions** |
| :------------------------------------------------------------ | :-----------------------------------------------------: | :----------------------------------------------------------: | -----------------------------------------------------------: |
| [doom.nvim](https://github.com/doom-neovim/doom-nvim)         |   [dusk.nvim](https://github.com/imbacraft/dusk.nvim)   |     [lin.nvim](https://github.com/linrongbin16/lin.nvim)     |             [ModuleVim](https://github.com/JryChn/ModuleVim) |
| [mood-nvim](https://github.com/otavioschwanck/mood-nvim)      | [neovitality](https://github.com/zachcoyle/neovitality) | [nii-nvim](https://github.com/Theory-of-Everything/nii-nvim) |                  [nv-ide](https://github.com/crivotz/nv-ide) |
| [nvim](https://github.com/askfiy/nvim)                        |         [nvim](https://github.com/cunderw/nvim)         |       [nvim-ide](https://github.com/ldelossa/nvim-ide)       |                  [nvoid](https://github.com/nvoid-lua/nvoid) |
| [nyoom.nvim](https://github.com/nyoom-engineering/nyoom.nvim) |   [.sea.nvim](https://github.com/cstsunfu/.sea.nvim)    |    [VapourNvim](https://github.com/VapourNvim/VapourNvim)    | [web-dev.nvim](https://github.com/jonathandion/web-dev.nvim) |

## Lazyman included Neovim configuration distribution details

- [Abstract](https://github.com/Abstract-IDE/Abstract)
  - [Neovimcraft description](https://neovimcraft.com/plugin/Abstract-IDE/Abstract/index.html)
  - Lazyman Abstract configuration
    - `~/.config/lazyman/Abstract` install with `lazyman -g`
- [AstroNvim](https://github.com/AstroNvim/AstroNvim)
  - [Neovimcraft description](https://neovimcraft.com/plugin/AstroNvim/AstroNvim/index.html)
  - Install all Lazyman AstroNvim configurations with `lazyman -i astronvim -y`
  - Lazyman AstroNvim configurations
    - `~/.config/lazyman/AstroNvimPlus` install with `lazyman -a`
    - `~/.config/lazyman/AstroNvimStart` install with `lazyman -x AstroNvimStart`
    - `~/.config/lazyman/Kabin` install with `lazyman -x Kabin`
    - `~/.config/lazyman/Lamia` install with `lazyman -x Lamia`
    - `~/.config/lazyman/Micah` install with `lazyman -x Micah`
    - `~/.config/lazyman/Normal` install with `lazyman -x Normal`
    - `~/.config/lazyman/Orhun` install with `lazyman -w Orhun`
    - `~/.config/lazyman/Spider` install with `lazyman -w Spider`
- [CodeArt](https://github.com/artart222/CodeArt)
  - [Neovimcraft description](https://neovimcraft.com/plugin/artart222/CodeArt/index.html)
  - Lazyman CodeArt configuration
    - `~/.config/lazyman/CodeArt` install with `lazyman -x CodeArt`
- [CosmicNvim](https://github.com/CosmicNvim/CosmicNvim)
  - [Neovimcraft description](https://neovimcraft.com/plugin/CosmicNvim/CosmicNvim/index.html)
  - Lazyman CosmicNvim configuration
    - `~/.config/lazyman/Cosmic` install with `lazyman -x Cosmic`
- [Ecovim](https://github.com/ecosse3/nvim)
  - [Neovimcraft description](https://neovimcraft.com/plugin/ecosse3/nvim/index.html)
  - Lazyman Ecovim configuration
    - `~/.config/lazyman/Ecovim` install with `lazyman -e`
- [kickstart](https://github.com/nvim-lua/kickstart.nvim)
  - [Neovimcraft description](https://neovimcraft.com/plugin/nvim-lua/kickstart.nvim/index.html)
  - Lazyman kickstart configuration
    - `~/.config/lazyman/Kickstart` install with `lazyman -k`
- [LazyVim](https://github.com/LazyVim/LazyVim)
  - [Neovimcraft description](https://neovimcraft.com/plugin/LazyVim/LazyVim/index.html)
  - Install all Lazyman LazyVim configurations with `lazyman -i lazyvim -y`
  - Lazyman LazyVim configurations
    - `~/.config/lazyman/LazyVim` install with `lazyman -l`
    - `~/.config/lazyman/Penguin` install with `lazyman -o`
    - `~/.config/lazyman/CatNvim` install with `lazyman -L CatNvim`
    - `~/.config/lazyman/Elijah` install with `lazyman -w Elijah`
    - `~/.config/lazyman/JustinNvim` install with `lazyman -w JustinNvim`
    - `~/.config/lazyman/JustinOhMy` install with `lazyman -x JustinOhMy`
    - `~/.config/lazyman/LazyIde` install with `lazyman -L LazyIde`
    - `~/.config/lazyman/Nv` install with `lazyman -L Nv`
    - `~/.config/lazyman/Traap` install with `lazyman -w Traap`
    - `~/.config/lazyman/Webdev` install with `lazyman -L Webdev`
- [LunarVim](https://github.com/LunarVim/LunarVim)
  - [Neovimcraft description](https://neovimcraft.com/plugin/LunarVim/LunarVim/index.html)
  - Install all Lazyman LunarVim configurations with `lazyman -i lunarvim -y`
  - Lazyman LunarVim configurations
    - `~/.config/lazyman/LunarVim` install with `lazyman -v`
    - `~/.config/lazyman/Daniel` install with `lazyman -w Daniel`
    - `~/.config/lazyman/JustinLvim` install with `lazyman -w JustinLvim`
    - `~/.config/lazyman/LunarIde` install with `lazyman -L LunarIde`
    - `~/.config/lazyman/LvimAdib` install with `lazyman -w LvimAdib`
    - `~/.config/lazyman/Shuvro` install with `lazyman -L Shuvro`
- [LvimIde](https://github.com/lvim-tech/lvim)
  - [Neovimcraft description](https://neovimcraft.com/plugin/lvim-tech/lvim/index.html) (needs help)
  - Lazyman LvimIde configuration
    - `~/.config/lazyman/LvimIde` install with `lazyman -L LvimIde`
- [mini.nvim](https://github.com/echasnovski/mini.nvim)
  - [Neovimcraft description](https://neovimcraft.com/plugin/echasnovski/mini.nvim/index.html)
  - Lazyman mini.nvim configuration
    - `~/.config/lazyman/Mini` install with `lazyman -M`
- [NormalNvim](https://github.com/NormalNvim/NormalNvim)
  - [Neovimcraft description](https://neovimcraft.com/plugin/NormalNvim/NormalNvim/index.html)
  - NormalNvim is an enhanced fork of AstroNvim and serves as a sort of meta-distribution
  - Lazyman NormalNvim configuration
    - `~/.config/lazyman/Normal` install with `lazyman -x Normal`
- [NvChad](https://github.com/NvChad/NvChad)
  - [Neovimcraft description](https://neovimcraft.com/plugin/siduck76/NvChad/index.html)
  - Install all Lazyman NvChad configurations with `lazyman -i nvchad -y`
  - Lazyman NvChad configurations
    - `~/.config/lazyman/NvChad` install with `lazyman -c`
    - `~/.config/lazyman/Cpp` install with `lazyman -L Cpp`
    - `~/.config/lazyman/Go` install with `lazyman -L Go`
    - `~/.config/lazyman/Python` install with `lazyman -L Python`
    - `~/.config/lazyman/Rust` install with `lazyman -L Rust`
- [NvPak](https://github.com/EvolveBeyond/NvPak)
  - [Neovimcraft description](https://neovimcraft.com/plugin/Pakrohk-DotFiles/NvPak/index.html)
  - Lazyman NvPak configuration
    - `~/.config/lazyman/NvPak` install with `lazyman -x NvPak`
- [SpaceVim](https://spacevim.org)
  - Lazyman SpaceVim configuration
    - `~/.config/lazyman/SpaceVim` install with `lazyman -s`

## See also

- [Preconfigured Configuration](https://github.com/rockerBOO/awesome-neovim#preconfigured-configuration) at [Awesome Neovim](https://github.com/rockerBOO/awesome-neovim)
- [Preconfigured Configuration](https://neovimcraft.com/?search=tag:preconfigured-configuration) at [Neovimcraft](https://neovimcraft.com)
- [Medium article exploring the top Neovim distributions](https://medium.com/@adaml.poniatowski/exploring-the-top-neovim-distributions-lazyvim-lunarvim-astrovim-and-nvchad-which-one-reigns-3adcdbfa478d)

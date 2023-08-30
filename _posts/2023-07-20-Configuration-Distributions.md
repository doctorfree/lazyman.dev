---
title: Neovim Configuration Distributions
author: doctorfree
date: 2023-07-20 12:45:00 +0800
tags: [neovim, config, configuration, preconfigured, distribution]
pin: true
img_path: "/posts/20230720"
---

## Introduction

[Neovim](https://neovim.io/){:target="\_blank"}{:rel="noopener noreferrer"} refers to itself as "hyperextensible". Much if not
most of the ability to extend `Neovim` derives from its plugin architecture.
There are hundreds of Neovim plugins, each with its own unique initialization
and configuration, some with duplicate functionality. It can be difficult for
a Neovim user to decide which plugins to use and how to configure each.

Fortunately, there exist many excellent pre-configured and user-extensible
Neovim configuration distributions. However, there are so many good Neovim
configuration distributions that it becomes difficult for a Neovim user to
decide which distribution to use and how to tailor it for their use case.

[Lazyman](https://github.com/doctorfree/nvim-lazyman){:target="\_blank"}{:rel="noopener noreferrer"}
attempts to address this issue by providing several example configurations of many of the Neovim
configuration distributions in an easy-to-install and easy-to-use manner.
Try each distribution out, see how you like it, play with them, extend each
to your liking, settle on one you like and adopt it for your use case(s).

## Top Neovim configuration distributions

By far, the top 5 Neovim configuration distributions are
[AstroNvim](https://github.com/AstroNvim/AstroNvim){:target="\_blank"}{:rel="noopener noreferrer"},
[kickstart](https://github.com/nvim-lua/kickstart.nvim){:target="\_blank"}{:rel="noopener noreferrer"},
[LazyVim](https://github.com/LazyVim/LazyVim){:target="\_blank"}{:rel="noopener noreferrer"},
[LunarVim](https://github.com/LunarVim/LunarVim){:target="\_blank"}{:rel="noopener noreferrer"},
and
[NvChad](https://github.com/NvChad/NvChad){:target="\_blank"}{:rel="noopener noreferrer"}.
That is not to say these are the "best" configuration distributions, simply that they are the most popular.

Each of these configuration distributions has value. They all provide
excellent starting points for crafting your own custom configuration,
they are all extensible and fairly easy to learn, and they all provide
an out-of-the-box setup that can be used effectively without modification.

Distinguishing features of the top Neovim configuration distributions:

### AstroNvim

- An excellent [community repository](https://github.com/AstroNvim/astrocommunity){:target="\_blank"}{:rel="noopener noreferrer"}
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
| [Abstract](https://github.com/Abstract-IDE/Abstract){:target="\_blank"}{:rel="noopener noreferrer"}    | [AstroNvim](https://github.com/AstroNvim/AstroNvim){:target="\_blank"}{:rel="noopener noreferrer"} | [CodeArt](https://github.com/artart222/CodeArt){:target="\_blank"}{:rel="noopener noreferrer"}  | [CosmicNvim](https://github.com/CosmicNvim/CosmicNvim){:target="\_blank"}{:rel="noopener noreferrer"} |             [Ecovim](https://github.com/ecosse3/nvim){:target="\_blank"}{:rel="noopener noreferrer"} |
| [kickstart](https://github.com/nvim-lua/kickstart.nvim){:target="\_blank"}{:rel="noopener noreferrer"} |    [LazyVim](https://github.com/LazyVim/LazyVim){:target="\_blank"}{:rel="noopener noreferrer"}    | [LunarVim](https://github.com/LunarVim/LunarVim){:target="\_blank"}{:rel="noopener noreferrer"} |      [LvimIde](https://github.com/lvim-tech/lvim){:target="\_blank"}{:rel="noopener noreferrer"}      | [mini.nvim](https://github.com/echasnovski/mini.nvim){:target="\_blank"}{:rel="noopener noreferrer"} |
| [NormalNvim](https://github.com/NormalNvim/NormalNvim){:target="\_blank"}{:rel="noopener noreferrer"}  |     [NvChad](https://github.com/NvChad/NvChad){:target="\_blank"}{:rel="noopener noreferrer"}      |  [NvPak](https://github.com/EvolveBeyond/NvPak){:target="\_blank"}{:rel="noopener noreferrer"}  |            [SpaceVim](https://spacevim.org){:target="\_blank"}{:rel="noopener noreferrer"}            |                                                       |

## Distributions not yet included in Lazyman

| **Excluded**                                                  |                       **Neovim**                        |                      **Configuration**                       |                                            **Distributions** |
| :------------------------------------------------------------ | :-----------------------------------------------------: | :----------------------------------------------------------: | -----------------------------------------------------------: |
| [doom.nvim](https://github.com/doom-neovim/doom-nvim){:target="\_blank"}{:rel="noopener noreferrer"}         |   [dusk.nvim](https://github.com/imbacraft/dusk.nvim){:target="\_blank"}{:rel="noopener noreferrer"}   |     [lin.nvim](https://github.com/linrongbin16/lin.nvim){:target="\_blank"}{:rel="noopener noreferrer"}     |             [ModuleVim](https://github.com/JryChn/ModuleVim){:target="\_blank"}{:rel="noopener noreferrer"} |
| [mood-nvim](https://github.com/otavioschwanck/mood-nvim){:target="\_blank"}{:rel="noopener noreferrer"}      | [neovitality](https://github.com/zachcoyle/neovitality){:target="\_blank"}{:rel="noopener noreferrer"} | [nii-nvim](https://github.com/Theory-of-Everything/nii-nvim){:target="\_blank"}{:rel="noopener noreferrer"} |                  [nv-ide](https://github.com/crivotz/nv-ide){:target="\_blank"}{:rel="noopener noreferrer"} |
| [nvim](https://github.com/askfiy/nvim){:target="\_blank"}{:rel="noopener noreferrer"}                        |         [nvim](https://github.com/cunderw/nvim){:target="\_blank"}{:rel="noopener noreferrer"}         |       [nvim-ide](https://github.com/ldelossa/nvim-ide){:target="\_blank"}{:rel="noopener noreferrer"}       |                  [nvoid](https://github.com/nvoid-lua/nvoid){:target="\_blank"}{:rel="noopener noreferrer"} |
| [nyoom.nvim](https://github.com/nyoom-engineering/nyoom.nvim){:target="\_blank"}{:rel="noopener noreferrer"} |   [.sea.nvim](https://github.com/cstsunfu/.sea.nvim){:target="\_blank"}{:rel="noopener noreferrer"}    |    [VapourNvim](https://github.com/VapourNvim/VapourNvim){:target="\_blank"}{:rel="noopener noreferrer"}    | [web-dev.nvim](https://github.com/jonathandion/web-dev.nvim){:target="\_blank"}{:rel="noopener noreferrer"} |

## Lazyman included Neovim configuration distribution details

- [Abstract](https://github.com/Abstract-IDE/Abstract){:target="\_blank"}{:rel="noopener noreferrer"}
  - [Neovimcraft description](https://neovimcraft.com/plugin/Abstract-IDE/Abstract/index.html){:target="\_blank"}{:rel="noopener noreferrer"}
  - Lazyman Abstract configuration
    - `~/.config/nvim-Abstract` install with `lazyman -g`
- [AstroNvim](https://github.com/AstroNvim/AstroNvim){:target="\_blank"}{:rel="noopener noreferrer"}
  - [Neovimcraft description](https://neovimcraft.com/plugin/AstroNvim/AstroNvim/index.html){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install all Lazyman AstroNvim configurations with `lazyman -i astronvim -y`
  - Lazyman AstroNvim configurations
    - `~/.config/nvim-AstroNvimPlus` install with `lazyman -a`
    - `~/.config/nvim-AstroNvimStart` install with `lazyman -x AstroNvimStart`
    - `~/.config/nvim-Kabin` install with `lazyman -x Kabin`
    - `~/.config/nvim-Lamia` install with `lazyman -x Lamia`
    - `~/.config/nvim-Micah` install with `lazyman -x Micah`
    - `~/.config/nvim-Normal` install with `lazyman -x Normal`
    - `~/.config/nvim-Orhun` install with `lazyman -w Orhun`
    - `~/.config/nvim-Spider` install with `lazyman -w Spider`
- [CodeArt](https://github.com/artart222/CodeArt){:target="\_blank"}{:rel="noopener noreferrer"}
  - [Neovimcraft description](https://neovimcraft.com/plugin/artart222/CodeArt/index.html){:target="\_blank"}{:rel="noopener noreferrer"}
  - Lazyman CodeArt configuration
    - `~/.config/nvim-CodeArt` install with `lazyman -x CodeArt`
- [CosmicNvim](https://github.com/CosmicNvim/CosmicNvim){:target="\_blank"}{:rel="noopener noreferrer"}
  - [Neovimcraft description](https://neovimcraft.com/plugin/CosmicNvim/CosmicNvim/index.html){:target="\_blank"}{:rel="noopener noreferrer"}
  - Lazyman CosmicNvim configuration
    - `~/.config/nvim-Cosmic` install with `lazyman -x Cosmic`
- [Ecovim](https://github.com/ecosse3/nvim){:target="\_blank"}{:rel="noopener noreferrer"}
  - [Neovimcraft description](https://neovimcraft.com/plugin/ecosse3/nvim/index.html){:target="\_blank"}{:rel="noopener noreferrer"}
  - Lazyman Ecovim configuration
    - `~/.config/nvim-Ecovim` install with `lazyman -e`
- [kickstart](https://github.com/nvim-lua/kickstart.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
  - [Neovimcraft description](https://neovimcraft.com/plugin/nvim-lua/kickstart.nvim/index.html){:target="\_blank"}{:rel="noopener noreferrer"}
  - Lazyman kickstart configuration
    - `~/.config/nvim-Kickstart` install with `lazyman -k`
- [LazyVim](https://github.com/LazyVim/LazyVim){:target="\_blank"}{:rel="noopener noreferrer"}
  - [Neovimcraft description](https://neovimcraft.com/plugin/LazyVim/LazyVim/index.html){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install all Lazyman LazyVim configurations with `lazyman -i lazyvim -y`
  - Lazyman LazyVim configurations
    - `~/.config/nvim-LazyVim` install with `lazyman -l`
    - `~/.config/nvim-Penguin` install with `lazyman -o`
    - `~/.config/nvim-CatNvim` install with `lazyman -L CatNvim`
    - `~/.config/nvim-Elijah` install with `lazyman -w Elijah`
    - `~/.config/nvim-JustinNvim` install with `lazyman -w JustinNvim`
    - `~/.config/nvim-JustinOhMy` install with `lazyman -x JustinOhMy`
    - `~/.config/nvim-LazyIde` install with `lazyman -L LazyIde`
    - `~/.config/nvim-Nv` install with `lazyman -L Nv`
    - `~/.config/nvim-Traap` install with `lazyman -w Traap`
    - `~/.config/nvim-Webdev` install with `lazyman -L Webdev`
- [LunarVim](https://github.com/LunarVim/LunarVim){:target="\_blank"}{:rel="noopener noreferrer"}
  - [Neovimcraft description](https://neovimcraft.com/plugin/LunarVim/LunarVim/index.html){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install all Lazyman LunarVim configurations with `lazyman -i lunarvim -y`
  - Lazyman LunarVim configurations
    - `~/.config/nvim-LunarVim` install with `lazyman -v`
    - `~/.config/nvim-Daniel` install with `lazyman -w Daniel`
    - `~/.config/nvim-JustinLvim` install with `lazyman -w JustinLvim`
    - `~/.config/nvim-LunarIde` install with `lazyman -L LunarIde`
    - `~/.config/nvim-LvimAdib` install with `lazyman -w LvimAdib`
    - `~/.config/nvim-Shuvro` install with `lazyman -L Shuvro`
- [LvimIde](https://github.com/lvim-tech/lvim){:target="\_blank"}{:rel="noopener noreferrer"}
  - [Neovimcraft description](https://neovimcraft.com/plugin/lvim-tech/lvim/index.html){:target="\_blank"}{:rel="noopener noreferrer"} (needs help)
  - Lazyman LvimIde configuration
    - `~/.config/nvim-LvimIde` install with `lazyman -L LvimIde`
- [mini.nvim](https://github.com/echasnovski/mini.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
  - [Neovimcraft description](https://neovimcraft.com/plugin/echasnovski/mini.nvim/index.html){:target="\_blank"}{:rel="noopener noreferrer"}
  - Lazyman mini.nvim configuration
    - `~/.config/nvim-Mini` install with `lazyman -M`
- [NormalNvim](https://github.com/NormalNvim/NormalNvim){:target="\_blank"}{:rel="noopener noreferrer"}
  - [Neovimcraft description](https://neovimcraft.com/plugin/NormalNvim/NormalNvim/index.html){:target="\_blank"}{:rel="noopener noreferrer"}
  - NormalNvim is an enhanced fork of AstroNvim and serves as a sort of meta-distribution
  - Lazyman NormalNvim configuration
    - `~/.config/nvim-Normal` install with `lazyman -x Normal`
- [NvChad](https://github.com/NvChad/NvChad){:target="\_blank"}{:rel="noopener noreferrer"}
  - [Neovimcraft description](https://neovimcraft.com/plugin/siduck76/NvChad/index.html){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install all Lazyman NvChad configurations with `lazyman -i nvchad -y`
  - Lazyman NvChad configurations
    - `~/.config/nvim-NvChad` install with `lazyman -c`
    - `~/.config/nvim-Cpp` install with `lazyman -L Cpp`
    - `~/.config/nvim-Go` install with `lazyman -L Go`
    - `~/.config/nvim-Python` install with `lazyman -L Python`
    - `~/.config/nvim-Rust` install with `lazyman -L Rust`
- [NvPak](https://github.com/EvolveBeyond/NvPak){:target="\_blank"}{:rel="noopener noreferrer"}
  - [Neovimcraft description](https://neovimcraft.com/plugin/Pakrohk-DotFiles/NvPak/index.html){:target="\_blank"}{:rel="noopener noreferrer"}
  - Lazyman NvPak configuration
    - `~/.config/nvim-NvPak` install with `lazyman -x NvPak`
- [SpaceVim](https://spacevim.org){:target="\_blank"}{:rel="noopener noreferrer"}
  - Lazyman SpaceVim configuration
    - `~/.config/nvim-SpaceVim` install with `lazyman -s`

## See also

- [Preconfigured Configuration](https://github.com/rockerBOO/awesome-neovim#preconfigured-configuration){:target="\_blank"}{:rel="noopener noreferrer"} at [Awesome Neovim](https://github.com/rockerBOO/awesome-neovim){:target="\_blank"}{:rel="noopener noreferrer"}
- [Preconfigured Configuration](https://neovimcraft.com/?search=tag:preconfigured-configuration){:target="\_blank"}{:rel="noopener noreferrer"} at [Neovimcraft](https://neovimcraft.com){:target="\_blank"}{:rel="noopener noreferrer"}
- [Medium article exploring the top Neovim distributions](https://medium.com/@adaml.poniatowski/exploring-the-top-neovim-distributions-lazyvim-lunarvim-astrovim-and-nvchad-which-one-reigns-3adcdbfa478d){:target="\_blank"}{:rel="noopener noreferrer"}

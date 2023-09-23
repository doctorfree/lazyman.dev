---
title: Lazyman Supported Neovim Configurations
author: doctorfree
date: 2023-08-23 16:20:00 +0800
tags: [neovim, config, lazyman, configurations, supported]
pin: true
img_path: "/posts/20230823"
---

See the [Configurations section](https://lazyman.dev/configurations) for
links to info documents describing each of the Lazyman supported Neovim
configurations and additional Lazyman supported Neovim configuration details.

## Lazyman Configuration Categories

After [installing and initializing Lazyman](https://lazyman.dev/install),
additional Neovim configurations can be installed and initialized using
the `lazyman` command.

All of the supported Lazyman Neovim configurations can be managed using
the `lazyman` command interactive menu interface. The `lazyman` menu is
presented by invoking `lazyman` without arguments after the initial
bootstrap process is complete. Lazyman Neovim configurations can
also be managed with `lazyman` command line operations.

Currently over 100 popular Neovim configurations are supported in the
following configuration categories:

| **Lazyman** | **Supported** | **Configuration** | **Frameworks** |
| :---------- | :-----------: | :---------------: | -------------: |
| [AstroNvim configurations](https://astronvim.lazyman.dev) | [LazyVim configurations](https://lazyvim.lazyman.dev) | [LunarVim configurations](https://lunarvim.lazyman.dev) | [NvChad configurations](https://nvchad.lazyman.dev) |

| **Lazyman** | **Supported** | **Configuration** | **Categories** |
| :---------- | :-----------: | :---------------: | -------------: |
| [Base configurations](#base-configurations) | [Language configurations](#language-configurations) | [Personal configurations](#personal-configurations) | [Starter configurations](#starter-configurations) |

In addition to the supported configuration categories,
[Custom configurations](#custom-configurations) can be installed
and initialized using [lazyman command line arguments](https://lazyman.dev/usage).

### Base configurations

The Lazyman "Base" Neovim configurations are well tested, full featured Neovim
configurations that provide an excellent base starting point for exploring
the features of `lazyman` and the wealth of Neovim configuration possibilities.

All "Base" Neovim configurations can be installed and initialized with `lazyman -B`.

#### Lazyman "Base" Neovim configurations

- [Lazyman](https://lazyman.dev/info/Lazyman.html)
  - See the [Installation section](https://lazyman.dev/install)
  - Installed and initialized by default
- [Abstract](https://lazyman.dev/info/Abstract.html)
  - Preconfigured Neovim as IDE (see the [Abstract website](https://abstract-ide.github.io/site/){:target="\_blank"}{:rel="noopener noreferrer"})
  - Install and initialize with `lazyman -g`
- [AstroNvimPlus](https://lazyman.dev/info/AstroNvimPlus.html)
  - Install and initialize with `lazyman -a`
  - An example [AstroNvim community](https://github.com/AstroNvim/astrocommunity){:target="\_blank"}{:rel="noopener noreferrer"} plugins configuration is added
- [Basic IDE](https://lazyman.dev/info/BasicIde.html)
  - Maintained by LunarVim, this is a descendent of "Neovim from Scratch"
  - All plugins are pinned to known working versions
  - Install and initialize with `lazyman -j`
- [Ecovim](https://lazyman.dev/info/Ecovim.html)
  - Install and initialize with `lazyman -e`
  - Tailored for frontend development with React and Vue.js
- [LazyVim](https://lazyman.dev/info/LazyVim.html)
  - The [LazyVim starter](https://github.com/LazyVim/starter){:target="\_blank"}{:rel="noopener noreferrer"} configuration
  - Install and initialize with `lazyman -l`
- [LunarVim](https://lazyman.dev/info/LunarVim.html)
  - Installs LunarVim plus the [IfCodingWereNatural custom user config](https://youtu.be/Qf9gfx7gWEY){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -v`
- [MagicVim](https://lazyman.dev/info/MagicVim.html)
  - Custom Neovim configuration designed to be light and fast
  - LSP, Treesitter & Code Completion all work out of the box
  - Auto install when you open a file type that doesn't have code completion for it yet
  - Uses Packer plugin manager, installs in `~/.config/nvim-MagicVim`
  - Install and initialize with `lazyman -m`
- [NvChad](https://lazyman.dev/info/NvChad.html)
  - Advanced [customization of NvChad](https://github.com/doctorfree/NvChad-custom){:target="\_blank"}{:rel="noopener noreferrer"}
  - Good [introductory video](https://youtu.be/Mtgo-nP_r8Y){:target="\_blank"}{:rel="noopener noreferrer"} to NvChad
  - Install and initialize with `lazyman -c`
- [SpaceVim](https://lazyman.dev/info/SpaceVim.html)
  - SpaceVim started in December 2016, mature and well supported
  - Standard SpaceVim install uses `curl`:
 - `curl -sLf https://spacevim.org/install.sh | bash`
  - Lazyman custom SpaceVim configuration installed in `~/.SpaceVim.d/`
  - Install and initialize using Lazyman with `lazyman -s`

### Language configurations

In addition to the base Neovim configurations listed above, `lazyman` can
install and initialize several "Language" Neovim configurations. These can
be used as programming or document format specific Neovim configurations.
The `Language` category configurations either employ a specific language
or target specific language(s).

[Note:] The `Language` category does not include all supported Lazyman Neovim
configurations with programming language support. In fact, most Neovim
configurations support several programming languages. The `Language` category
simply serves as a convenience to get started exploring language support.

All of the "Language" configurations can be installed and initialized with
the command `lazyman -L all`. Individual "Language" configurations can be
installed with the `-L lang` option.

#### Lazyman "Language" Neovim configurations

- [AlanVim](https://lazyman.dev/info/AlanVim.html)
  - Oriented toward Python development
  - Install and initialize with `lazyman -L AlanVim`
- [Allaman](https://lazyman.dev/info/Allaman.html)
  - One of the inspirations for `Lazyman`
  - Excellent support for Python, Golang, Rust, YAML, and more
  - Install and initialize with `lazyman -L Allaman`
- [CatNvim](https://lazyman.dev/info/CatNvim.html)
  - Included in the `Language` category as the configuration is written in `C`
  - Yes, this is a Neovim configuration written in the [C programming language](https://en.wikipedia.org/wiki/C_(programming_language)){:target="\_blank"}{:rel="noopener noreferrer"}
  - `CatNvim` is a `LazyVim` based configuration
  - Install and initialize with `lazyman -L CatNvim`
- [Cpp](https://lazyman.dev/info/Cpp.html)
  - `NvChad` based Neovim config with C++ formatting, debugging, and diagnostics
  - Dreams of Code [video tutorial](https://youtu.be/lsFoZIg-oDs){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -L Cpp`
- [Go](https://lazyman.dev/info/Go.html)
  - `NvChad` based Neovim config with Go formatting, debugging, and diagnostics
  - Dreams of Code [video tutorial](https://youtu.be/i04sSQjd-qo){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -L Go`
- [Go2one](https://lazyman.dev/info/Go2one.html)
  - Neovim Go development environment that does not touch standard Neovim configuration folders
  - The `lazyman` install does not use the `go2one` script
  - Install and initialize with `lazyman -L Go2one`
- [Insis](https://lazyman.dev/info/Insis.html)
  - Out-of-the-box Neovim IDE solution with simple development environment setup
  - Install and initialize with `lazyman -L Insis`
- [Knvim](https://lazyman.dev/info/Knvim.html)
  - Targets Python, Bash, LaTeX, Markdown, and C/C++
  - See the [Knvim Config Cheat Sheet](https://github.com/knmac/knvim/blob/main/res/cheatsheet.md){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -L Knvim`
- [LaTeX](https://lazyman.dev/info/LaTeX.html)
  - Neovim configuration optimized for writing in LaTeX
  - Personal Neovim configuration of [Benjamin Brast-McKie](http://www.benbrastmckie.com){:target="\_blank"}{:rel="noopener noreferrer"}
  - Keymaps and more described in the configuration [Cheatsheet](https://github.com/benbrastmckie/.config/blob/master/CheatSheet.md){:target="\_blank"}{:rel="noopener noreferrer"}
  - Blog article by the author detailing [tools used by his configuration](http://www.benbrastmckie.com/tools#access){:target="\_blank"}{:rel="noopener noreferrer"}
  - [Video playlist](https://www.youtube.com/watch?v=_Ct2S65kpjQ&list=PLBYZ1xfnKeDRhCoaM4bTFrjCl3NKDBvqk){:target="\_blank"}{:rel="noopener noreferrer"} of tutorials on using this config for writing LaTeX in Neovim
  - Install and initialize with `lazyman -L LaTeX`
- [LazyIde](https://lazyman.dev/info/LazyIde.html)
  - LazyVim IDE config for Neovim
  - Install and initialize with `lazyman -L LazyIde`
- [LunarIde](https://lazyman.dev/info/LunarIde.html)
  - LunarVim config based on [Christian Chiarulli's](https://github.com/ChristianChiarulli/lvim){:target="\_blank"}{:rel="noopener noreferrer"}
  - Java, Python, Lua, Go, JavaScript, Typescript, React, and Rust IDE
  - Install and initialize with `lazyman -L LunarIde`
- [LvimIde](https://lazyman.dev/info/LvimIde.html)
  - Not to be confused with `LunarVim`, this is a standalone Neovim configuration
  - Modular configuration with LSP support for 60+ languages
  - Debug support for c, cpp, dart, elixir, go, haskell, java, javascript/typescript, lua, php, python, ruby, rust
  - Install and initialize with `lazyman -L LvimIde`
- [Magidc](https://lazyman.dev/info/Magidc.html)
  - Java, Python, Lua, and Rust IDE
  - Install and initialize with `lazyman -L Magidc`
- [Nv](https://lazyman.dev/info/Nv.html)
  - `LazyVim` based Neovim configuration
  - Andreas Gerlach develops smart farming tech and maintains the `Sway` edition of `Manjaro-arm`
  - Install and initialize with `lazyman -L Nv`
- [NV-IDE](https://lazyman.dev/info/NV-IDE.html)
  - Configuration oriented for web developers (rails, ruby, php, html, css, SCSS, javascript)
  - Install and initialize with `lazyman -L NV-IDE`
- [Orange](https://lazyman.dev/info/Orange.html)
  - Modern Neovim configuration for coding React and TypeScript
  - Install and initialize with `lazyman -L Orange`
- [Python](https://lazyman.dev/info/Python.html)
  - `NvChad` based Neovim config with Python formatting, debugging, and diagnostics
  - Dreams of Code [video tutorial](https://youtu.be/4BnVeOUeZxc){:target="\_blank"}{:rel="noopener noreferrer"}
  - These features are included in the Base `NvChad` custom add-on (`lazyman -c`)
  - Install and initialize `lazyman -L Python`
- [Rust](https://lazyman.dev/info/Rust.html)
  - `NvChad` based Neovim config with Rust formatting, debugging, and diagnostics
  - Dreams of Code [video tutorial](https://youtu.be/mh_EJhH49Ms){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -L Rust`
- [SaleVim](https://lazyman.dev/info/SaleVim.html)
  - `Salesforce` optimized IDE with custom features for editing `Apex`, `Visualforce`, and `Lightning` code
  - Install and initialize with `lazyman -L SaleVim`
- [Shuvro](https://lazyman.dev/info/Shuvro.html)
  - Significantly improved fork of [Abouzar Parvan's](https://github.com/abzcoding/lvim){:target="\_blank"}{:rel="noopener noreferrer"} advanced `LunarVim` config
  - Install and initialize with `lazyman -L Shuvro`
- [Webdev](https://lazyman.dev/info/Webdev.html)
  - LazyVim based config for web developers
  - JavaScript, Typescript, React, and Tailwind CSS support
  - Install and initialize with `lazyman -L Webdev`

### Personal configurations

In addition to the base and language Neovim configurations listed above,
`lazyman` can install and initialize several "Personal" Neovim configurations.
These are used as personal Neovim configurations, so there are no guarantees
made about stability or compatibility. Each supported personal configuration
uses some interesting approach and provides significant value making them worthy
of study, exploration, and possible use in tailoring your own configuration.

All of the 'Personal' configurations can be installed and initialized with
the command `lazyman -W`. Individual 'Personal' configurations can be
installed with the `-w conf` option.

#### Lazyman "Personal" Neovim configurations

- [Adib](https://lazyman.dev/info/Adib.html)
  - Personal Neovim configuration of Adib Hanna
  - Tips, distros, and configuration [demo video](https://youtu.be/8SVPOKZVaMU){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -w Adib`
- [Ahsan](https://lazyman.dev/info/Ahsan.html)
  - Personal Neovim configuration of Ahsan Habib
  - Install and initialize with `lazyman -w Ahsan`
- [Artur](https://lazyman.dev/info/Artur.html)
  - Personal Neovim configuration of Artur Gomes
  - Install and initialize with `lazyman -w Artur`
- [Beethoven](https://lazyman.dev/info/Beethoven.html)
  - Personal Neovim configuration of mechanical engineering student Alexander Vazquez
  - `lazyman -w Beethoven`
- [Brain](https://lazyman.dev/info/Brain.html)
  - Well structured personal config based on the [KISS](https://en.wikipedia.org/wiki/KISS_principle){:target="\_blank"}{:rel="noopener noreferrer"} principle
  - `lazyman -w Brain`
- [Charles](https://lazyman.dev/info/Charles.html)
  - Well structured lazy config with several setup scripts and a Wiki
  - Install and initialize with `lazyman -w Charles`
- [Chokerman](https://lazyman.dev/info/Chokerman.html)
  - Personal Neovim configuration of Github user `justchokingaround`
  - Install and initialize with `lazyman -w Chokerman`
- [Craftzdog](https://lazyman.dev/info/Craftzdog.html)
  - Takuya Matsuyama's Neovim configuration
  - Install and initialize with `lazyman -w Craftzdog`
- [Daniel](https://lazyman.dev/info/Daniel.html)
  - `LunarVim` based config of Daniel Vera Gilliard
  - Install and initialize with `lazyman -w Daniel`
- [Dillon](https://lazyman.dev/info/Dillon.html)
  - Author of [tsc.nvim](https://github.com/dmmulroy/tsc.nvim){:target="\_blank"}{:rel="noopener noreferrer"}, asynchronous TypeScript type-checking
  - Install and initialize with `lazyman -w Dillon`
- [Elianiva](https://lazyman.dev/info/Elianiva.html)
  - Personal Neovim configuration of Dicha Zelianivan Arkana
  - `lazyman -w Elianiva`
- [Elijah](https://lazyman.dev/info/Elijah.html)
  - Personal Neovim configuration of Elijah Manor
  - `lazyman -w Elijah`
- [Enrique](https://lazyman.dev/info/Enrique.html)
  - Personal Neovim configuration of Enrique Mejidas
  - `lazyman -w Enrique`
- [Jdhao](https://lazyman.dev/info/Jdhao.html)
  - A modern Neovim configuration with full support for Python, Lua, C++, Markdown, LaTeX, and more
  - `lazyman -w Jdhao`
- [Kristijan](https://lazyman.dev/info/Kristijan.html)
  - Personal Neovim configuration of Kristijan Husak, author of several Neovim plugins including `orgmode` and `vim-dadbod-ui`
  - `lazyman -w Kristijan`
- [Heiker](https://lazyman.dev/info/Heiker.html)
  - Neovim config of Heiker Curiel, author of [lsp-zero](https://github.com/VonHeikemen/lsp-zero.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -w Heiker`
- [J4de](https://lazyman.dev/info/J4de.html)
  - Personal Neovim configuration of Jade Fox
  - `lazyman -w J4de`
- [Josean](https://lazyman.dev/info/Josean.html)
  - Josean Martinez [video tutorial](https://youtu.be/vdn_pKJUda8){:target="\_blank"}{:rel="noopener noreferrer"}
  - `lazyman -w Josean`
- [JustinLvim](https://lazyman.dev/info/JustinLvim.html)
  - LunarVim based Neovim configuration by Justin Angeles
  - Install and initialize with `lazyman -w JustinLvim`
- [JustinNvim](https://lazyman.dev/info/JustinNvim.html)
  - LazyVim based Neovim configuration by Justin Angeles
  - Justin has created a series of YouTube videos on configuring LazyVim
 - [Part 1 - Colorschemne](https://youtu.be/LznwxUSZz_8){:target="\_blank"}{:rel="noopener noreferrer"}
 - [Part 2 - Options](https://youtu.be/I4flypojhUk){:target="\_blank"}{:rel="noopener noreferrer"}
 - [Part 3 - Keymaps](https://youtu.be/Vc_5feJ9F5k){:target="\_blank"}{:rel="noopener noreferrer"}
 - [Part 4 - Final Thoughts](https://youtu.be/eRQHWeJ3D7I){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -w JustinNvim`
- [Kodo](https://lazyman.dev/info/Kodo.html)
  - Personal Neovim configuration of chadcat, a high school student with no life
  - `Kodo` is a Neovim configuration that looks good and is fast (startuptime < 0.035s)
  - Install and initialize with `lazyman -w Kodo`
- [LamarVim](https://lazyman.dev/info/LamarVim.html)
  - Personal Neovim configuration of Cassio Lamarck
  - Install and initialize with `lazyman -w LamarVim`
- [Lukas](https://lazyman.dev/info/Lukas.html)
  - Packer based personal Neovim configuration of Lukas Reineke, author of many excellent Neovim plugins
  - Requires an externally installed `lua-language-server` and `efm-langserver`
  - Install and initialize with `lazyman -w Lukas`
- [Maddison](https://lazyman.dev/info/Maddison.html)
  - Personal Neovim configuration of Maddison Hellstrom
  - Author of `incline.nvim` floating statuslines, `SchemaStore.nvim` JSON schemas, `mapx.nvim` better keymaps
  - Install and initialize with `lazyman -w Maddison`
- [Metis](https://lazyman.dev/info/Metis.html)
  - Neovim config by the creator of `MetisLinux` and `Ewm`
  - Install and initialize with `lazyman -w Metis`
- [Mini](https://lazyman.dev/info/Mini.html)
  - Uses the [mini.nvim](https://github.com/echasnovski/mini.nvim){:target="\_blank"}{:rel="noopener noreferrer"} library
  - Personal configuration of the `mini.nvim` author
  - Install and initialize with `lazyman -M`
- [ONNO](https://lazyman.dev/info/ONNO.html)
  - One of the primary inspirations for Lazyman
  - Install and initialize with `lazyman -w ONNO`
- [OnMyWay](https://lazyman.dev/info/OnMyWay.html)
  - The personal Neovim configuration of Richard Ariza
  - Install and initialize with `lazyman -w OnMyWay`
- [Optixal](https://lazyman.dev/info/Optixal.html)
  - Hybrid Neovim config for developers with a functional yet aesthetic experience
  - Uses a combination of vimscript and lua with the `vim-plug` plugin manager
  - Install and initialize with `lazyman -w Optixal`
- [Orhun](https://lazyman.dev/info/Orhun.html)
  - Personal AstroNvim based Neovim configuration of open source developer Orhun Parmaksiz
  - Install and initialize with `lazyman -w Orhun`
- [Primeagen](https://lazyman.dev/info/Primeagen.html)
  - Packer based [config from scratch](https://youtu.be/w7i4amO_zaE){:target="\_blank"}{:rel="noopener noreferrer"} by ThePrimeagen"
  - Install and initialize with `lazyman -w Primeagen`
- [Rafi](https://lazyman.dev/info/Rafi.html)
  - [Extensible](https://github.com/rafi/vim-config#extending){:target="\_blank"}{:rel="noopener noreferrer"} Neovim configuration
  - Install and initialize with `lazyman -w Rafi`
- [RNvim](https://lazyman.dev/info/RNvim.html)
  - Personal Neovim configuration of Github user `RoryNesbitt`
  - Install and initialize with `lazyman -w RNvim`
- [Roiz](https://lazyman.dev/info/Roiz.html)
  - Just a random Neovim config found on Github, works well
  - Install and initialize with `lazyman -w Roiz`
- [Simple](https://lazyman.dev/info/Simple.html)
  - A remarkably effective Neovim configuration in only one small file
  - The author's [video description of this config](https://youtu.be/AzhSnM0uHvM){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -w Simple`
- [Slydragonn](https://lazyman.dev/info/Slydragonn.html)
  - [Introductory video](https://youtu.be/vkCnPdaRBE0){:target="\_blank"}{:rel="noopener noreferrer"}
  - `lazyman -w Slydragonn`
- [Spider](https://lazyman.dev/info/Spider.html)
  - AstroNvim based configuration with animated status bar and smooth scroll
  - [Introductory video](https://youtu.be/Lj6MZsKl9MU){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -w Spider`
- [Traap](https://lazyman.dev/info/Traap.html)
  - [Introductory video](https://youtu.be/aD9j6d9pgtc){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -w Traap`
- [Wuelner](https://lazyman.dev/info/Wuelner.html)
  - Wuelner's Neovim setup follows a well-defined philosophy governed by coherence and minimalism
  - Install and initialize with `lazyman -w Wuelner`
- [xero](https://lazyman.dev/info/xero.html)
  - personal neovim configuration of [xero harrison](https://x-e.ro/){:target="\_blank"}{:rel="noopener noreferrer"}
  - xero is a fine example, as are many here, of the unix greybeard
  - install and initialize with `lazyman -w xero`
- [Xiao](https://lazyman.dev/info/Xiao.html)
  - Personal Neovim configuration of XiaoZhang
  - Install and initialize with `lazyman -w Xiao`

### Starter configurations

The "Starter" Neovim configurations include `Basic`, `Kickstart`, `NvPak`,
`Modern`, `PDE`, and those provided by [VonHeikemen](https://github.com/VonHeikemen){:target="\_blank"}{:rel="noopener noreferrer"},
the author of [LSP Zero](https://github.com/VonHeikemen/lsp-zero.nvim){:target="\_blank"}{:rel="noopener noreferrer"}.

All of the "Starter" configurations can be installed and initialized with
the command `lazyman -X`. Individual "Starter" configurations can be
installed with the `-x conf` option.

#### Lazyman "Starter" Neovim configurations

- [AstroNvimStart](https://lazyman.dev/info/AstroNvimStart.html)
  - Default AstroNvim example configuration
  - Install and initialize with `lazyman -x AstroNvimStart`
- [Barebones](https://lazyman.dev/info/Barebones.html)
  - Starter bare bones LazyVim config by Traap with [video introduction](https://youtu.be/xpBoiTIiepc){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -x Barebones`
- [Basic](https://lazyman.dev/info/Basic.html)
  - Starter config by the author of NvChad with [video tutorial](https://youtube.com/playlist?list=PLYVQrj2EVSUL1NqYn3jsIVXG3U9eWaMcq){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -x Basic`
- [CodeArt](https://lazyman.dev/info/CodeArt.html)
  - Use Neovim as general purpose IDE
  - Install and initialize with `lazyman -x CodeArt`
- [CosmicNvim](https://lazyman.dev/info/Cosmic.html)
  - Install `Node.js`, `prettierd`, and `eslint_d`
  - Install and initialize with `lazyman -x Cosmic`
- [Ember](https://lazyman.dev/info/Ember.html)
  - Dan is a computer science student at Arizona State University
  - Install and initialize with `lazyman -x Ember`
- [Fennel](https://lazyman.dev/info/Fennel.html)
  - An opinionated configuration reminiscent of Doom-Emacs, written in Fennel
  - Install and initialize with `lazyman -x Fennel`
- [Kickstart](https://lazyman.dev/info/Kickstart.html)
  - Popular starting point, small, single file, well documented, modular
  - Install and initialize with `lazyman -k`
- [KickstartPython](https://lazyman.dev/info/KickstartPython.html)
  - Kickstart configuration tailored for use with Python
  - Install and initialize with `lazyman -x KickstartPython`
- [nvim2k](https://lazyman.dev/info/2k.html)
  - [Video walkthrough](https://youtu.be/WfhylGI_F-o){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -x 2k`
- [NvPak](https://lazyman.dev/info/NvPak.html)
  - PaK in Farsi means pure, something that is in its purest form
  - Install and initialize with `lazyman -x NvPak`
- [HardHacker](https://lazyman.dev/info/HardHacker.html)
  - A theme-driven modern Neovim configuration
  - Install and initialize with `lazyman -x HardHacker`
- [JustinOhMy](https://lazyman.dev/info/JustinOhMy.html)
  - Full featured starter LazyVim based Neovim configuration by Justin Angeles
  - Justin has created a [YouTube video](https://youtu.be/mpSuIfBKP-s){:target="\_blank"}{:rel="noopener noreferrer"} describing this config
  - Install and initialize with `lazyman -x JustinOhMy`
- [Modern](https://lazyman.dev/info/Modern.html)
  - Configure Neovim as a modernized development environment
  - Details described in [an excellent Medium article](https://alpha2phi.medium.com/modern-neovim-configuration-recipes-d68b16537698){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -x Modern`
- [PDE](https://lazyman.dev/info/pde.html)
  - Configure Neovim as a Personalized Development Environment (PDE)
  - Install and initialize with `lazyman -x pde`
- [Kabin](https://lazyman.dev/info/Kabin.html)
  - One of the AstroNvim "Black Belt" example advanced configurations
  - `lazyman -x Kabin`
- [Micah](https://lazyman.dev/info/Micah.html)
  - One of the AstroNvim "Black Belt" example advanced configurations
  - `lazyman -x Micah`
- [Normal](https://lazyman.dev/info/Normal.html)
  - Based on AstroNvim with additional features
  - Install and initialize with `lazyman -x Normal`
- [Rohit](https://lazyman.dev/info/Rohit.html)
  - Good example use of [mason-tool-installer](https://github.com/WhoIsSethDaniel/mason-tool-installer.nvim){:target="\_blank"}{:rel="noopener noreferrer"}
  - Install and initialize with `lazyman -x Rohit`
- [Scratch](https://lazyman.dev/info/Scratch.html)
  - Jumping-off point for new Neovim users or those who have declared config bankruptcy
  - Install and initialize with `lazyman -x Scratch`
- [SingleFile](https://lazyman.dev/info/SingleFile.html)
  - A clean, organized pre-configured Neovim configuration guide in a single `init.lua`
  - Install and initialize with `lazyman -x SingleFile`

#### VonHeikemen Starter configurations

- [BasicLsp](https://lazyman.dev/info/BasicLsp.html)
  - Example lua configuration showing one way to setup LSP servers without plugins
  - Install and initialize with `lazyman -x BasicLsp`
- [BasicMason](https://lazyman.dev/info/BasicMason.html)
  - Minimal setup with `mason.nvim`
  - Install and initialize with `lazyman -x BasicMason`
- [LspCmp](https://lazyman.dev/info/LspCmp.html)
  - Minimal setup with `nvim-lspconfig` and `nvim-cmp`
  - Install and initialize with `lazyman -x LspCmp`
- [Extralight](https://lazyman.dev/info/Extralight.html)
  - Single file lightweight configuration focused on providing basic features
  - Install and initialize with `lazyman -x Extralight`
- [Minimal](https://lazyman.dev/info/Minimal.html)
  - Small configuration without third party plugins
  - Install and initialize with `lazyman -x Minimal`
- [Modular](https://lazyman.dev/info/Modular.html)
  - Same as `StartMason` but everything is split in modules
  - Install and initialize with `lazyman -x Modular`
- [StartBase](https://lazyman.dev/info/StartBase.html)
  - Small configuration that includes a plugin manager
  - Install and initialize with `lazyman -x StartBase`
- [Opinionated](https://lazyman.dev/info/Opinion.html)
  - Includes a combination of popular plugins
  - Install and initialize with `lazyman -x Opinion`
- [StartLsp](https://lazyman.dev/info/StartLsp.html)
  - Configures the built-in LSP client with autocompletion, based on `Opinionated`
  - Install and initialize with `lazyman -x StartLsp`
- [StartMason](https://lazyman.dev/info/StartMason.html)
  - Same as `StartLsp` but uses [mason.nvim](https://github.com/williamboman/mason.nvim){:target="\_blank"}{:rel="noopener noreferrer"} to install language servers
  - Install and initialize with `lazyman -x StartMason`

### Custom configurations

Lazyman includes support for `Custom` Neovim configurations. To install and initialize
a Neovim configuration not supported out-of-the-box by Lazyman, use the `-C url` and
`-N nvimdir` options to `lazyman`. After the installation and initialization completes,
set the `NVIM_APPNAME` environment variable to use the newly created Neovim configuration:

```bash
export NVIM_APPNAME="<nvimdir>"
```

Where `<nvimdir>` is the argument provided to `-N` above.

For example, to install and initialize the Packer based Neovim configuration
hosted at
[https://github.com/VapourNvim/VapourNvim](https://github.com/VapourNvim/VapourNvim){:target="\_blank"}{:rel="noopener noreferrer"}
and place it in
`~/.config/nvim-VapourNvim`, execute the command:

```bash
lazyman -C https://github.com/VapourNvim/VapourNvim -N VapourNvim -P
export NVIM_APPNAME="nvim-VapourNvim"
nvim
```

Sometimes people place their Neovim configuration in a repository subdirectory
along with other configurations in a `dotfiles` repo. To retrieve only the
Neovim configuration subdirectory in such a repository, use the `-b branch`
and `-D subdir` arguments to `lazyman` along with `-C url` and `-N nvimdir`.
If no `-b branch` is provided then the default git branch is assumed to be
`master`. For example, to install and initialize the Neovim configuration
hosted at
[https://github.com/alanRizzo/dot-files](https://github.com/alanRizzo/dot-files){:target="\_blank"}{:rel="noopener noreferrer"}
in the subdirectory `nvim`
with default branch `main`, place it in `~/.config/nvim-AlanVim`, and
initialize it with Packer:

```bash
lazyman -b main -C https://github.com/alanRizzo/dot-files -D nvim -N AlanVim -P
```

Note the `-b main` argument in this Lazyman command. When specifying a
subdirectory of a repository with `-D <subdir>` it is necessary to also
provide the default branch of the repository if not `master`.

Custom Neovim configurations may require additional setup work. Often
a custom Lazyman configuration will appear to work without issue but
contain references to `~/.config/nvim/` in its configuration files. For
example, a configuration's dashboard may contain a reference to
`~/.config/nvim/init.lua`. References like this can be fixed so the
configuration is relocatable by doing something like the following in Lua:

```lua
local config_path = vim.fn.stdpath("config") .. "/init.lua"
```

Custom Neovim configurations will be displayed and available in subsequent
runs of `lazyman` in the Lazyman Menu System.

An excellent list of preconfigured Neovim configurations is available at the
[Awesome Neovim Repository](https://github.com/rockerBOO/awesome-neovim#preconfigured-configuration){:target="\_blank"}{:rel="noopener noreferrer"}. Many of these can be easily installed and initialized using
`lazyman -b <branch> -C <url> -N <nvimdir> ...`.

Feel free to open an issue at
[https://github.com/doctorfree/nvim-lazyman/issues](https://github.com/doctorfree/nvim-lazyman/issues){:target="\_blank"}{:rel="noopener noreferrer"}
to help tackle any problems
installing or initializing Neovim configurations with Lazyman.

#### Custom configuration patches

If you encounter a Neovim configuration that does not cleanly initialize
with `lazyman` it is often possible to make a few minor changes to the
configuration to get it working. Lazyman supports custom configuration
patches that are applied during initialization of a configuration.

The `~/.config/nvim-Lazyman/scripts/patches/` directory contains patches
to Neovim configurations applied after cloning the repo with `lazyman`.

The patch file for a configuration must be named `<Name>.patch` where
`<Name>` is the name of the configuration folder in `~/.config/`.

Some Neovim configurations do not initialize cleanly using `lazyman`
and modifications to the configuration files may be necessary. In this
case it is possible to generate a patch file for the config, place it
here, and re-run `lazyman` to install and initialize that configuration.

The patch should be created from the top of the configuration directory
after making the necessary changes and backing up the original file(s).

For example, the Neovim configuration by [3rd](https://github.com/3rd/config){:target="\_blank"}{:rel="noopener noreferrer"}
contains references to a custom tree-sitter grammar and does not initialize
cleanly with `lazyman`. After commenting out these references a patch can be
created for this config with:

```bash
diff -Naur lua/modules/language-support/tree-sitter.lua.orig \
  lua/modules/language-support/tree-sitter.lua \
  > ~/.config/nvim-Lazyman/scripts/patches/3rd.patch
```

Subsequently, running:

```bash
lazyman -C https://github.com/3rd/config -D home/dotfiles/nvim -N 3rd
```

will produce a cleanly initialized Neovim configuration.

---
layout: post
title: Rust Configuration Info
toc: true
post_style: page
---

## Rust Neovim Configuration Information

'NvChad' based Neovim config with Rust formatting, debugging, and diagnostics. Dreams of Code [video tutorial](https://youtu.be/mh_EJhH49Ms){:target="_blank"}{:rel="noopener noreferrer"}

- Install and initialize: **`lazyman -L Rust`**
- Configuration category: [Language](https://lazyman.dev/configurations/#language-configurations)
- Base configuration:     [NvChad](https://nvchad.com){:target="_blank"}{:rel="noopener noreferrer"}
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- Installation location:  **`~/.config/nvim-Rust`**


### Git repository

[https://github.com/dreamsofcode-io/neovim-rust](https://github.com/dreamsofcode-io/neovim-rust){:target="_blank"}{:rel="noopener noreferrer"}

### Website

[https://nvchad.com](https://nvchad.com){:target="_blank"}{:rel="noopener noreferrer"}

### YouTube channel

[https://www.youtube.com/@dreamsofcode](https://www.youtube.com/@dreamsofcode){:target="_blank"}{:rel="noopener noreferrer"}

### Lazy managed plugins

- [numToStr/Comment.nvim](https://github.com/numToStr/Comment.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip){:target="_blank"}{:rel="noopener noreferrer"}
- [NvChad/base46](https://github.com/NvChad/base46.git){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-buffer](https://github.com/hrsh7th/cmp-buffer){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-nvim-lua](https://github.com/hrsh7th/cmp-nvim-lua){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-path](https://github.com/hrsh7th/cmp-path){:target="_blank"}{:rel="noopener noreferrer"}
- [saadparwaiz1/cmp_luasnip](https://github.com/saadparwaiz1/cmp_luasnip){:target="_blank"}{:rel="noopener noreferrer"}
- [saecki/crates.nvim](https://github.com/saecki/crates.nvim.git){:target="_blank"}{:rel="noopener noreferrer"}
- [NvChad/extensions](https://github.com/NvChad/extensions.git){:target="_blank"}{:rel="noopener noreferrer"}
- [rafamadriz/friendly-snippets](https://github.com/rafamadriz/friendly-snippets){:target="_blank"}{:rel="noopener noreferrer"}
- [lewis6991/gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [lukas-reineke/indent-blankline.nvim](https://github.com/lukas-reineke/indent-blankline.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/lazy.nvim](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [windwp/nvim-autopairs](https://github.com/windwp/nvim-autopairs){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp){:target="_blank"}{:rel="noopener noreferrer"}
- [norcalli/nvim-colorizer.lua](https://github.com/norcalli/nvim-colorizer.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [theHamsta/nvim-dap-virtual-text](https://github.com/theHamsta/nvim-dap-virtual-text){:target="_blank"}{:rel="noopener noreferrer"}
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-tree.lua](https://github.com/kyazdani42/nvim-tree.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons){:target="_blank"}{:rel="noopener noreferrer"}
- [NvChad/nvterm](https://github.com/NvChad/nvterm){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [simrat39/rust-tools.nvim](https://github.com/simrat39/rust-tools.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [rust-lang/rust.vim](https://github.com/rust-lang/rust.vim.git){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [bluz71/vim-nightfly-guicolors](https://github.com/bluz71/vim-nightfly-guicolors){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/which-key.nvim](https://github.com/folke/which-key.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### Rust Keymaps

#### normal mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  |   |  |
|  | " |  |
| Nvim builtin | & | :&&<CR> |
|  | ' |  |
| Nvim builtin | Y | y$ |
|  | ` |  |
|  | c |  |
| Comment toggle current block | gbc |  |
| Comment toggle blockwise | gb |  |
| Comment toggle linewise | gc |  |
| Comment toggle current line | gcc |  |
|  | g |  |
|  | v |  |
| Nvim builtin | <C-L> | <Cmd>nohlsearch|diffupdate|normal! <C-L><CR> |

#### visual mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
| Nvim builtin | # | y?\V<C-R>"<CR> |
| Nvim builtin | * | y/\V<C-R>"<CR> |
| Comment toggle blockwise (visual) | gb |  |
| Comment toggle linewise (visual) | gc |  |

#### operator mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
| Comment toggle linewise | gc |  |
| Comment toggle blockwise | gb |  |

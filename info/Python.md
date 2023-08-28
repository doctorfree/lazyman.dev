---
layout: post
title: Python Configuration Info
toc: true
post_style: page
---

## Python Neovim Configuration Information

'NvChad' based Neovim config with Python formatting, debugging, and diagnostics. Dreams of Code [video tutorial](https://youtu.be/4BnVeOUeZxc). These features are included in the Base 'NvChad' custom add-on (lazyman -c){:target="_blank"}{:rel="noopener noreferrer"}

- Install and initialize: **`-L Python`**
- Configuration category: [Language](https://lazyman.dev/configurations/#language-configurations)
- Base configuration:     [NvChad](https://nvchad.com){:target="_blank"}{:rel="noopener noreferrer"}
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- Installation location:  **`~/.config/lazyman/Python`**


### Git repository

[https://github.com/dreamsofcode-io/neovim-python](https://github.com/dreamsofcode-io/neovim-python){:target="_blank"}{:rel="noopener noreferrer"}

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
- [NvChad/extensions](https://github.com/NvChad/extensions.git){:target="_blank"}{:rel="noopener noreferrer"}
- [rafamadriz/friendly-snippets](https://github.com/rafamadriz/friendly-snippets){:target="_blank"}{:rel="noopener noreferrer"}
- [lewis6991/gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [lukas-reineke/indent-blankline.nvim](https://github.com/lukas-reineke/indent-blankline.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/lazy.nvim](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [jayp0521/mason-null-ls.nvim](https://github.com/jayp0521/mason-null-ls.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [windwp/nvim-autopairs](https://github.com/windwp/nvim-autopairs){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp){:target="_blank"}{:rel="noopener noreferrer"}
- [norcalli/nvim-colorizer.lua](https://github.com/norcalli/nvim-colorizer.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [mfussenegger/nvim-dap-python](https://github.com/mfussenegger/nvim-dap-python.git){:target="_blank"}{:rel="noopener noreferrer"}
- [rcarriga/nvim-dap-ui](https://github.com/rcarriga/nvim-dap-ui){:target="_blank"}{:rel="noopener noreferrer"}
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-tree.lua](https://github.com/kyazdani42/nvim-tree.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons){:target="_blank"}{:rel="noopener noreferrer"}
- [NvChad/nvterm](https://github.com/NvChad/nvterm){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [bluz71/vim-nightfly-guicolors](https://github.com/bluz71/vim-nightfly-guicolors){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/which-key.nvim](https://github.com/folke/which-key.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### Python Keymaps

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
|  | g |  |
| Comment toggle blockwise | gb |  |
| Comment toggle linewise | gc |  |
| Comment toggle current block | gbc |  |
| Comment toggle current line | gcc |  |
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
| Comment toggle blockwise | gb |  |
| Comment toggle linewise | gc |  |

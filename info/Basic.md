---
layout: post
title: Basic Configuration Info
toc: true
post_style: page
---

## Basic Neovim Configuration Information

Starter config by the author of NvChad with [video tutorial](https://youtube.com/playlist?list=PLYVQrj2EVSUL1NqYn3jsIVXG3U9eWaMcq){:target="_blank"}{:rel="noopener noreferrer"}

- Install and initialize: **`lazyman -x Basic`**
- Configuration category: [Starter](https://lazyman.dev/configurations/#starter-configurations)
- Base configuration:     Custom
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- Installation location:  **`~/.config/nvim-Basic`**


### Git repository

[https://github.com/NvChad/basic-config](https://github.com/NvChad/basic-config){:target="_blank"}{:rel="noopener noreferrer"}

### YouTube channel

[https://www.youtube.com/@siduck_og](https://www.youtube.com/@siduck_og){:target="_blank"}{:rel="noopener noreferrer"}

### Lazy managed plugins

- [numToStr/Comment.nvim](https://github.com/numToStr/Comment.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip){:target="_blank"}{:rel="noopener noreferrer"}
- [akinsho/bufferline.nvim](https://github.com/akinsho/bufferline.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-buffer](https://github.com/hrsh7th/cmp-buffer){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-nvim-lua](https://github.com/hrsh7th/cmp-nvim-lua){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-path](https://github.com/hrsh7th/cmp-path){:target="_blank"}{:rel="noopener noreferrer"}
- [saadparwaiz1/cmp_luasnip](https://github.com/saadparwaiz1/cmp_luasnip){:target="_blank"}{:rel="noopener noreferrer"}
- [rafamadriz/friendly-snippets](https://github.com/rafamadriz/friendly-snippets){:target="_blank"}{:rel="noopener noreferrer"}
- [lewis6991/gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [lukas-reineke/indent-blankline.nvim](https://github.com/lukas-reineke/indent-blankline.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/lazy.nvim](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [echasnovski/mini.statusline](https://github.com/echasnovski/mini.statusline.git){:target="_blank"}{:rel="noopener noreferrer"}
- [jayp0521/mason-null-ls.nvim](https://github.com/jayp0521/mason-null-ls.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [windwp/nvim-autopairs](https://github.com/windwp/nvim-autopairs){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp){:target="_blank"}{:rel="noopener noreferrer"}
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-tree.lua](https://github.com/kyazdani42/nvim-tree.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons){:target="_blank"}{:rel="noopener noreferrer"}
- [navarasu/onedark.nvim](https://github.com/navarasu/onedark.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### Basic Keymaps

#### normal mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  | <Tab> | <Cmd> BufferLineCycleNext <CR> |
|  |  / |  |
|  |  gt | <Cmd> Telescope git_status <CR> |
|  |  fw | <Cmd> Telescope live_grep <CR> |
|  |  fo | <Cmd> Telescope oldfiles <CR> |
|  |  ff | <Cmd> Telescope find_files <CR> |
| Nvim builtin | & | :&&<CR> |
| Nvim builtin | Y | y$ |
|  | <C-Q> | <Cmd> bd <CR> |
|  | <S-Tab> | <Cmd> BufferLineCyclePrev <CR> |
|  | <C-H> | <Cmd> NvimTreeFocus <CR> |
|  | <C-N> | <Cmd> NvimTreeToggle <CR> |
|  | <C-S> | <Cmd> w <CR> |
| Nvim builtin | <C-L> | <Cmd>nohlsearch|diffupdate|normal! <C-L><CR> |

#### visual mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  |  / | <Esc><Cmd>lua require('Comment.api').toggle.linewise(vim.fn.visualmode())<CR> |
| Nvim builtin | # | y?\V<C-R>"<CR> |
| Nvim builtin | * | y/\V<C-R>"<CR> |

#### operator mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |

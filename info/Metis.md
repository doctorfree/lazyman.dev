---
layout: post
title: Metis Configuration Info
toc: true
post_style: page
---

## Metis Neovim Configuration Information

Neovim config by the creator of 'MetisLinux' and 'Ewm'

- Install and initialize: **`lazyman -w Metis`**
- Configuration category: [Personal](https://lazyman.dev/configurations/#personal-configurations)
- Base configuration:     Custom
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- Installation location:  **`~/.config/lazyman/Metis`**


### Git repository

[https://github.com/metis-os/pwnvim](https://github.com/metis-os/pwnvim){:target="_blank"}{:rel="noopener noreferrer"}

### Lazy managed plugins

- [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip){:target="_blank"}{:rel="noopener noreferrer"}
- [utilyre/barbecue.nvim](https://github.com/utilyre/barbecue.nvim.git){:target="_blank"}{:rel="noopener noreferrer"}
- [j-morano/buffer_manager.nvim](https://github.com/j-morano/buffer_manager.nvim.git){:target="_blank"}{:rel="noopener noreferrer"}
- [catppuccin/nvim](https://github.com/catppuccin/nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-buffer](https://github.com/hrsh7th/cmp-buffer){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/lazy.nvim](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig){:target="_blank"}{:rel="noopener noreferrer"}
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [echasnovski/mini.comment](https://github.com/echasnovski/mini.comment){:target="_blank"}{:rel="noopener noreferrer"}
- [jayp0521/mason-null-ls.nvim](https://github.com/jayp0521/mason-null-ls.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp){:target="_blank"}{:rel="noopener noreferrer"}
- [SmiteshP/nvim-navic](https://github.com/SmiteshP/nvim-navic){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-tree.lua](https://github.com/kyazdani42/nvim-tree.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons){:target="_blank"}{:rel="noopener noreferrer"}
- [NvChad/nvterm](https://github.com/NvChad/nvterm){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [utilyre/sentiment.nvim](https://github.com/utilyre/sentiment.nvim.git){:target="_blank"}{:rel="noopener noreferrer"}
- [artart222/telescope_find_directories](https://github.com/artart222/telescope_find_directories){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter){:target="_blank"}{:rel="noopener noreferrer"}

### Metis Keymaps

#### normal mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  | <Tab> |  |
|  |  ls | :LspStart<CR> |
|  |  lr | :LspRestart<CR> |
|  |  lp | :LspInfo<CR> |
|  |  x | <C-W>c |
|  |  h | :nohlsearch<CR> |
|  |  pd |  |
|  |  pp |  |
|  |  pr |  |
|  |  pl |  |
|  |  pc |  |
|  |  px |  |
|  |  ps |  |
|  |  pu |  |
|  |  pi |  |
|  |  ph |  |
|  |  d |  |
|  |  ff |  |
|  |  ft |  |
|  |  fr |  |
|  |  fw |  |
|  |  e |  |
|  |  b |  |
| Nvim builtin | & | :&&<CR> |
|  | J | jzz |
|  | K | kzz |
| Nvim builtin | Y | y$ |
|  | [d |  |
|  | ]d |  |
|  | <C-Q> | :bd!<CR> |
|  | <C-S> | :w <CR> |
|  | <C-K> | <C-W>k |
|  | <C-J> | <C-W>j |
|  | <C-H> | <C-W>h |
|  | <M-h> |  |
|  | <M-t> |  |
|  | <M-H> |  |
|  | <S-Tab> |  |
|  | <C-L> | <C-W>l |

#### visual mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
| Nvim builtin | # | y?\V<C-R>"<CR> |
| Nvim builtin | * | y/\V<C-R>"<CR> |
|  | J | :m '>+1<CR>gv=gv |
|  | K | :m '<lt>-2<CR>gv=gv |
|  | p | _dP |

#### operator mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |

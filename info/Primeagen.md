---
layout: post
title: Primeagen Configuration Info
toc: true
post_style: page
---

## Primeagen Neovim Configuration Information

[Config from scratch](https://youtu.be/w7i4amO_zaE) by ThePrimeagen

- Install and initialize: **`lazyman -w Primeagen`**
- Configuration category: [Personal](https://lazyman.dev/configurations/#personal-configurations)
- Base configuration:     Custom
- Plugin manager:         [Packer](https://github.com/wbthomason/packer.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- Installation location:  **`~/.config/nvim-Primeagen`**


### Git repository

[https://github.com/ThePrimeagen/init.lua](https://github.com/ThePrimeagen/init.lua){:target="_blank"}{:rel="noopener noreferrer"}

### YouTube channel

[https://www.youtube.com/@ThePrimeagen](https://www.youtube.com/@ThePrimeagen){:target="_blank"}{:rel="noopener noreferrer"}

### Packer managed plugins

- [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip){:target="_blank"}{:rel="noopener noreferrer"}
- [eandrju/cellular-automaton.nvim](https://github.com/eandrju/cellular-automaton.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [laytan/cloak.nvim](https://github.com/laytan/cloak.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-buffer](https://github.com/hrsh7th/cmp-buffer){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-nvim-lua](https://github.com/hrsh7th/cmp-nvim-lua){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-path](https://github.com/hrsh7th/cmp-path){:target="_blank"}{:rel="noopener noreferrer"}
- [saadparwaiz1/cmp_luasnip](https://github.com/saadparwaiz1/cmp_luasnip){:target="_blank"}{:rel="noopener noreferrer"}
- [github/copilot.vim](https://github.com/github/copilot.vim){:target="_blank"}{:rel="noopener noreferrer"}
- [rafamadriz/friendly-snippets](https://github.com/rafamadriz/friendly-snippets){:target="_blank"}{:rel="noopener noreferrer"}
- [theprimeagen/harpoon](https://github.com/theprimeagen/harpoon){:target="_blank"}{:rel="noopener noreferrer"}
- [VonHeikemen/lsp-zero.nvim](https://github.com/VonHeikemen/lsp-zero.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [williamboman/mason-lspconfig.nvim](https://github.com/williamboman/mason-lspconfig.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [williamboman/mason.nvim](https://github.com/williamboman/mason.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp){:target="_blank"}{:rel="noopener noreferrer"}
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter-context](https://github.com/nvim-treesitter/nvim-treesitter-context){:target="_blank"}{:rel="noopener noreferrer"}
- [wbthomason/packer.nvim](https://github.com/wbthomason/packer.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/playground](https://github.com/nvim-treesitter/playground){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [theprimeagen/refactoring.nvim](https://github.com/theprimeagen/refactoring.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [rose-pine/neovim](https://github.com/rose-pine/neovim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/trouble.nvim](https://github.com/folke/trouble.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [mbbill/undotree](https://github.com/mbbill/undotree){:target="_blank"}{:rel="noopener noreferrer"}
- [tpope/vim-fugitive](https://github.com/tpope/vim-fugitive){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/zen-mode.nvim](https://github.com/folke/zen-mode.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### Primeagen Keymaps

#### normal mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  |  zZ |  |
|  |  zz |  |
|  |  u |  |
|  |  xq | <Cmd>TroubleToggle quickfix<CR> |
|  |  vh |  |
|  |  ps |  |
|  |  pf |  |
|  |  a |  |
|  |  gs |  |
|  |    |  |
|  |  mr | <Cmd>CellularAutomaton make_it_rain<CR> |
|  |  vpp | <Cmd>e ~/.config/nvim-Primeagen/lua/theprimeagen/packer.lua<CR> |
|  |  x | <Cmd>!chmod +x %<CR> |
|  |  s | :%s/\<lt><C-R><C-W>\>/<C-R><C-W>/gI<Left><Left><Left> |
|  |  j | <Cmd>lprev<CR>zz |
|  |  k | <Cmd>lnext<CR>zz |
|  |  f |  |
|  |  d | "_d |
|  |  Y | "+Y |
|  |  y | "+y |
|  |  svwm |  |
|  |  vwm |  |
|  |  pv |  |
|  | % | <Plug>(MatchitNormalForward) |
| Nvim builtin | & | :&&<CR> |
|  | J | mzJ`z |
|  | N | Nzzzv |
|  | Q |  |
| Nvim builtin | Y | y$ |
|  | [% | <Plug>(MatchitNormalMultiBackward) |
|  | ]% | <Plug>(MatchitNormalMultiForward) |
|  | gx | <Plug>NetrwBrowseX |
|  | g% | <Plug>(MatchitNormalBackward) |
|  | n | nzzzv |
|  | y<C-G> | :<C-U>call setreg(v:register, fugitive#Object(@%))<CR> |
|  | <C-P> |  |
|  | <C-S> |  |
|  | <C-N> |  |
|  | <C-T> |  |
|  | <C-H> |  |
|  | <C-E> |  |
|  | <Plug>fugitive: |  |
|  | <Plug>fugitive:y<C-G> | :<C-U>call setreg(v:register, fugitive#Object(@%))<CR> |
|  | <Plug>PlenaryTestFile | :lua require('plenary.test_harness').test_directory(vim.fn.expand("%:p"))<CR> |
|  | <Plug>luasnip-expand-repeat |  |
|  | <Plug>luasnip-delete-check |  |
|  | <Plug>NetrwBrowseX | :call netrw#BrowseX(netrw#GX(),netrw#CheckIfRemote(netrw#GX()))<CR> |
|  | <Plug>(MatchitNormalMultiForward) | :<C-U>call matchit#MultiMatch("W",  "n")<CR> |
|  | <Plug>(MatchitNormalMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "n")<CR> |
|  | <Plug>(MatchitNormalBackward) | :<C-U>call matchit#Match_wrapper('',0,'n')<CR> |
|  | <Plug>(MatchitNormalForward) | :<C-U>call matchit#Match_wrapper('',1,'n')<CR> |
|  | <C-J> | <Cmd>cprev<CR>zz |
|  | <C-K> | <Cmd>cnext<CR>zz |
|  | <C-F> | <Cmd>silent !tmux neww tmux-sessionizer<CR> |
|  | <C-U> | <C-U>zz |
|  | <C-D> | <C-D>zz |
| Nvim builtin | <C-L> | <Cmd>nohlsearch|diffupdate|normal! <C-L><CR> |

#### visual mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  |  ri |  <Esc><Cmd>lua require('refactoring').refactor('Inline Variable')<CR> |
|  |  d | "_d |
|  |  y | "+y |
|  |  p | "_dP |
| Nvim builtin | # | y?\V<C-R>"<CR> |
|  | % | <Plug>(MatchitVisualForward) |
| Nvim builtin | * | y/\V<C-R>"<CR> |
|  | J | :m '>+1<CR>gv=gv |
|  | K | :m '<lt>-2<CR>gv=gv |
|  | [% | <Plug>(MatchitVisualMultiBackward) |
|  | ]% | <Plug>(MatchitVisualMultiForward) |
|  | a% | <Plug>(MatchitVisualTextObject) |
|  | gx | <Plug>NetrwBrowseXVis |
|  | g% | <Plug>(MatchitVisualBackward) |
|  | <Plug>luasnip-expand-repeat |  |
|  | <Plug>NetrwBrowseXVis | :<C-U>call netrw#BrowseXVis()<CR> |
|  | <Plug>(MatchitVisualTextObject) | <Plug>(MatchitVisualMultiBackward)o<Plug>(MatchitVisualMultiForward) |
|  | <Plug>(MatchitVisualMultiForward) | :<C-U>call matchit#MultiMatch("W",  "n")<CR>m'gv`` |
|  | <Plug>(MatchitVisualMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "n")<CR>m'gv`` |
|  | <Plug>(MatchitVisualBackward) | :<C-U>call matchit#Match_wrapper('',0,'v')<CR>m'gv`` |
|  | <Plug>(MatchitVisualForward) | :<C-U>call matchit#Match_wrapper('',1,'v')<CR>:if col("''") != col("$") | exe ":normal! m'" | endif<CR>gv`` |

#### operator mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  | % | <Plug>(MatchitOperationForward) |
|  | [% | <Plug>(MatchitOperationMultiBackward) |
|  | ]% | <Plug>(MatchitOperationMultiForward) |
|  | g% | <Plug>(MatchitOperationBackward) |
|  | <Plug>luasnip-expand-repeat |  |
|  | <Plug>(MatchitOperationMultiForward) | :<C-U>call matchit#MultiMatch("W",  "o")<CR> |
|  | <Plug>(MatchitOperationMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "o")<CR> |
|  | <Plug>(MatchitOperationBackward) | :<C-U>call matchit#Match_wrapper('',0,'o')<CR> |
|  | <Plug>(MatchitOperationForward) | :<C-U>call matchit#Match_wrapper('',1,'o')<CR> |

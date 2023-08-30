---
layout: post
title: Brain Configuration Info
toc: true
post_style: page
---

## Brain Neovim Configuration Information

Well structured personal config based on the [KISS](https://en.wikipedia.org/wiki/KISS_principle) principle

- Install and initialize: **`lazyman -w Brain`**
- Configuration category: [Personal](https://lazyman.dev/configurations/#personal-configurations)
- Base configuration:     Custom
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- Installation location:  **`~/.config/nvim-Brain`**


### Git repository

[https://github.com/brainfucksec/neovim-lua](https://github.com/brainfucksec/neovim-lua){:target="_blank"}{:rel="noopener noreferrer"}

### Neovimcraft entry

[http://neovimcraft.com/plugin/brainfucksec/neovim-lua](http://neovimcraft.com/plugin/brainfucksec/neovim-lua){:target="_blank"}{:rel="noopener noreferrer"}

### Lazy managed plugins

- [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip){:target="_blank"}{:rel="noopener noreferrer"}
- [goolord/alpha-nvim](https://github.com/goolord/alpha-nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-buffer](https://github.com/hrsh7th/cmp-buffer){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-path](https://github.com/hrsh7th/cmp-path){:target="_blank"}{:rel="noopener noreferrer"}
- [saadparwaiz1/cmp_luasnip](https://github.com/saadparwaiz1/cmp_luasnip){:target="_blank"}{:rel="noopener noreferrer"}
- [feline-nvim/feline.nvim](https://github.com/feline-nvim/feline.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [lewis6991/gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [lukas-reineke/indent-blankline.nvim](https://github.com/lukas-reineke/indent-blankline.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/lazy.nvim](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [tanvirtin/monokai.nvim](https://github.com/tanvirtin/monokai.nvim.git){:target="_blank"}{:rel="noopener noreferrer"}
- [windwp/nvim-autopairs](https://github.com/windwp/nvim-autopairs){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp){:target="_blank"}{:rel="noopener noreferrer"}
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-tree.lua](https://github.com/kyazdani42/nvim-tree.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons){:target="_blank"}{:rel="noopener noreferrer"}
- [navarasu/onedark.nvim](https://github.com/navarasu/onedark.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [rose-pine/neovim](https://github.com/rose-pine/neovim){:target="_blank"}{:rel="noopener noreferrer"}
- [preservim/tagbar](https://github.com/preservim/tagbar.git){:target="_blank"}{:rel="noopener noreferrer"}

### Brain Keymaps

#### normal mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  |  q |  |
|  |  e |  |
|  | % | <Plug>(MatchitNormalForward) |
| Nvim builtin | & | :&&<CR> |
|  | ,z | :TagbarToggle<CR> |
|  | ,n | :NvimTreeFindFile<CR> |
|  | ,f | :NvimTreeRefresh<CR> |
|  | ,q | :qa!<CR> |
|  | ,s | :w<CR> |
|  | ,r | :so %<CR> |
|  | ,th | <C-W>t<C-W>H |
|  | ,tk | <C-W>t<C-W>K |
|  | ,c | :nohl<CR> |
| Nvim builtin | Y | y$ |
|  | [d |  |
|  | [% | <Plug>(MatchitNormalMultiBackward) |
|  | ]d |  |
|  | ]% | <Plug>(MatchitNormalMultiForward) |
|  | gx | <Plug>NetrwBrowseX |
|  | g% | <Plug>(MatchitNormalBackward) |
|  | <Plug>luasnip-expand-repeat |  |
|  | <Plug>luasnip-delete-check |  |
|  | <C-N> | :NvimTreeToggle<CR> |
|  | <C-T> | :Term<CR> |
|  | <C-K> | <C-W>k |
|  | <C-J> | <C-W>j |
|  | <C-H> | <C-W>h |
|  | <F2> | :set invpaste paste?<CR> |
|  | <Right> |  |
|  | <Left> |  |
|  | <Down> |  |
|  | <Up> |  |
|  | <Plug>NetrwBrowseX | :call netrw#BrowseX(netrw#GX(),netrw#CheckIfRemote(netrw#GX()))<CR> |
|  | <Plug>(MatchitNormalMultiForward) | :<C-U>call matchit#MultiMatch("W",  "n")<CR> |
|  | <Plug>(MatchitNormalMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "n")<CR> |
|  | <Plug>(MatchitNormalBackward) | :<C-U>call matchit#Match_wrapper('',0,'n')<CR> |
|  | <Plug>(MatchitNormalForward) | :<C-U>call matchit#Match_wrapper('',1,'n')<CR> |
|  | <Plug>PlenaryTestFile | :lua require('plenary.test_harness').test_directory(vim.fn.expand("%:p"))<CR> |
|  | <C-L> | <C-W>l |

#### visual mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
| Nvim builtin | # | y?\V<C-R>"<CR> |
|  | % | <Plug>(MatchitVisualForward) |
| Nvim builtin | * | y/\V<C-R>"<CR> |
|  | [% | <Plug>(MatchitVisualMultiBackward) |
|  | ]% | <Plug>(MatchitVisualMultiForward) |
|  | a% | <Plug>(MatchitVisualTextObject) |
|  | gx | <Plug>NetrwBrowseXVis |
|  | g% | <Plug>(MatchitVisualBackward) |
|  | <Plug>luasnip-expand-repeat |  |
|  | <Right> |  |
|  | <Left> |  |
|  | <Down> |  |
|  | <Up> |  |
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
|  | <Right> |  |
|  | <Left> |  |
|  | <Down> |  |
|  | <Up> |  |
|  | <Plug>(MatchitOperationMultiForward) | :<C-U>call matchit#MultiMatch("W",  "o")<CR> |
|  | <Plug>(MatchitOperationMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "o")<CR> |
|  | <Plug>(MatchitOperationBackward) | :<C-U>call matchit#Match_wrapper('',0,'o')<CR> |
|  | <Plug>(MatchitOperationForward) | :<C-U>call matchit#Match_wrapper('',1,'o')<CR> |

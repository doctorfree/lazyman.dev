---
layout: post
title: Slydragonn Configuration Info
toc: true
post_style: page
---

## Slydragonn Neovim Configuration Information

[Introductory video](https://youtu.be/vkCnPdaRBE0){:target="_blank"}{:rel="noopener noreferrer"}

- Install and initialize: **`lazyman -w Slydragonn`**
- Configuration category: [Personal](https://lazyman.dev/configurations/#personal-configurations)
- Base configuration:     Custom
- Plugin manager:         [Packer](https://github.com/wbthomason/packer.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- Installation location:  **`~/.config/nvim-Slydragonn`**


### Git repository

[https://github.com/slydragonn/dotfiles](https://github.com/slydragonn/dotfiles){:target="_blank"}{:rel="noopener noreferrer"}

### YouTube channel

[https://www.youtube.com/@slydragonn](https://www.youtube.com/@slydragonn){:target="_blank"}{:rel="noopener noreferrer"}

### Packer managed plugins

- [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-buffer](https://github.com/hrsh7th/cmp-buffer){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-path](https://github.com/hrsh7th/cmp-path){:target="_blank"}{:rel="noopener noreferrer"}
- [lewis6991/gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [rebelot/kanagawa.nvim](https://github.com/rebelot/kanagawa.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [onsails/lspkind-nvim](https://github.com/onsails/lspkind-nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lualine/lualine.nvim](https://github.com/nvim-lualine/lualine.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [iamcco/markdown-preview.nvim](https://github.com/iamcco/markdown-preview.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [williamboman/mason-lspconfig.nvim](https://github.com/williamboman/mason-lspconfig.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [williamboman/mason.nvim](https://github.com/williamboman/mason.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-neo-tree/neo-tree.nvim](https://github.com/nvim-neo-tree/neo-tree.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [MunifTanjim/nui.nvim](https://github.com/MunifTanjim/nui.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [jose-elias-alvarez/null-ls.nvim](https://github.com/jose-elias-alvarez/null-ls.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [windwp/nvim-autopairs](https://github.com/windwp/nvim-autopairs){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp){:target="_blank"}{:rel="noopener noreferrer"}
- [norcalli/nvim-colorizer.lua](https://github.com/norcalli/nvim-colorizer.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig){:target="_blank"}{:rel="noopener noreferrer"}
- [xiyaowong/nvim-transparent](https://github.com/xiyaowong/nvim-transparent){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter){:target="_blank"}{:rel="noopener noreferrer"}
- [windwp/nvim-ts-autotag](https://github.com/windwp/nvim-ts-autotag){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-tree/nvim-web-devicons](https://github.com/nvim-tree/nvim-web-devicons){:target="_blank"}{:rel="noopener noreferrer"}
- [wbthomason/packer.nvim](https://github.com/wbthomason/packer.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [akinsho/toggleterm.nvim](https://github.com/akinsho/toggleterm.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### Slydragonn Keymaps

#### normal mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  | <Tab> | <Cmd>bnext<CR> |
|  |  mn | <Cmd>MarkdownPreviewStop<CR> |
|  |  m | <Cmd>MarkdownPreview<CR> |
|  |  tv | <Cmd>ToggleTerm size=80 direction=vertical<CR> |
|  |  th | <Cmd>ToggleTerm size=10 direction=horizontal<CR> |
|  |  o | <Cmd>Neotree focus<CR> |
|  |  e | <Cmd>Neotree toggle<CR> |
|  |  p | <Cmd>split<CR> |
|  |  ñ | <Cmd>vsplit<CR> |
|  |  q | <Cmd>q<CR> |
|  |  w | <Cmd>update<CR> |
|  |  fc |  |
|  |  fs |  |
|  |  fh |  |
|  |  fb |  |
|  |  fg |  |
|  |  ff |  |
|  | % | <Plug>(MatchitNormalForward) |
| Nvim builtin | & | :&&<CR> |
| Nvim builtin | Y | y$ |
|  | [% | <Plug>(MatchitNormalMultiBackward) |
|  | ]% | <Plug>(MatchitNormalMultiForward) |
|  | gx | <Plug>NetrwBrowseX |
|  | g% | <Plug>(MatchitNormalBackward) |
|  | <Plug>PlenaryTestFile | :lua require('plenary.test_harness').test_directory(vim.fn.expand("%:p"))<CR> |
|  | <Plug>luasnip-expand-repeat |  |
|  | <Plug>luasnip-delete-check |  |
| Toggle Terminal | <F7> | <Cmd>execute v:count . "ToggleTerm"<CR> |
|  | <Plug>NetrwBrowseX | :call netrw#BrowseX(netrw#GX(),netrw#CheckIfRemote(netrw#GX()))<CR> |
|  | <Plug>(MatchitNormalMultiForward) | :<C-U>call matchit#MultiMatch("W",  "n")<CR> |
|  | <Plug>(MatchitNormalMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "n")<CR> |
|  | <Plug>(MatchitNormalBackward) | :<C-U>call matchit#Match_wrapper('',0,'n')<CR> |
|  | <Plug>(MatchitNormalForward) | :<C-U>call matchit#Match_wrapper('',1,'n')<CR> |
|  | <C-Down> | <C-W>- |
|  | <C-Up> | <C-W>+ |
|  | <C-Right> | <C-W>> |
|  | <C-Left> | <C-W><lt> |
|  | <C-J> | <C-W>j |
|  | <C-K> | <C-W>k |
|  | <C-H> | <C-W>h |
|  | <S-Tab> | <Cmd>bprevious<CR> |
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

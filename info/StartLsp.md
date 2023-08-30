---
layout: post
title: StartLsp Configuration Info
toc: true
post_style: page
---

## StartLsp Neovim Configuration Information

Configures the built-in LSP client with autocompletion, based on 'Opinionated'

- Install and initialize: **`lazyman -x StartLsp`**
- Configuration category: [Starter](https://lazyman.dev/configurations/#starter-configurations)
- Base configuration:     Custom
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- Installation location:  **`~/.config/nvim-StartLsp`**


### Git repository

[https://github.com/VonHeikemen/nvim-starter/tree/03-lsp](https://github.com/VonHeikemen/nvim-starter/tree/03-lsp){:target="_blank"}{:rel="noopener noreferrer"}

### Lazy managed plugins

- [numToStr/Comment.nvim](https://github.com/numToStr/Comment.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip){:target="_blank"}{:rel="noopener noreferrer"}
- [akinsho/bufferline.nvim](https://github.com/akinsho/bufferline.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-buffer](https://github.com/hrsh7th/cmp-buffer){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-path](https://github.com/hrsh7th/cmp-path){:target="_blank"}{:rel="noopener noreferrer"}
- [saadparwaiz1/cmp_luasnip](https://github.com/saadparwaiz1/cmp_luasnip){:target="_blank"}{:rel="noopener noreferrer"}
- [lunarvim/darkplus.nvim](https://github.com/lunarvim/darkplus.nvim.git){:target="_blank"}{:rel="noopener noreferrer"}
- [rafamadriz/friendly-snippets](https://github.com/rafamadriz/friendly-snippets){:target="_blank"}{:rel="noopener noreferrer"}
- [lewis6991/gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [lukas-reineke/indent-blankline.nvim](https://github.com/lukas-reineke/indent-blankline.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/lazy.nvim](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lualine/lualine.nvim](https://github.com/nvim-lualine/lualine.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [tanvirtin/monokai.nvim](https://github.com/tanvirtin/monokai.nvim.git){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp){:target="_blank"}{:rel="noopener noreferrer"}
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-tree.lua](https://github.com/kyazdani42/nvim-tree.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter-textobjects](https://github.com/nvim-treesitter/nvim-treesitter-textobjects){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons){:target="_blank"}{:rel="noopener noreferrer"}
- [joshdick/onedark.vim](https://github.com/joshdick/onedark.vim.git){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [wellle/targets.vim](https://github.com/wellle/targets.vim.git){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-telescope/telescope-fzf-native.nvim](https://github.com/nvim-telescope/telescope-fzf-native.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [akinsho/toggleterm.nvim](https://github.com/akinsho/toggleterm.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/tokyonight.nvim](https://github.com/folke/tokyonight.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [moll/vim-bbye](https://github.com/moll/vim-bbye){:target="_blank"}{:rel="noopener noreferrer"}
- [tpope/vim-fugitive](https://github.com/tpope/vim-fugitive){:target="_blank"}{:rel="noopener noreferrer"}
- [tpope/vim-repeat](https://github.com/tpope/vim-repeat){:target="_blank"}{:rel="noopener noreferrer"}
- [kylechui/nvim-surround](https://github.com/kylechui/nvim-surround){:target="_blank"}{:rel="noopener noreferrer"}

### StartLsp Keymaps

#### normal mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  |  e | <Cmd>NvimTreeToggle<CR> |
|  |  fs | <Cmd>Telescope current_buffer_fuzzy_find<CR> |
|  |  fd | <Cmd>Telescope diagnostics<CR> |
|  |  fg | <Cmd>Telescope live_grep<CR> |
|  |  ff | <Cmd>Telescope find_files<CR> |
|  |    | <Cmd>Telescope buffers<CR> |
|  |  ? | <Cmd>Telescope oldfiles<CR> |
|  |  bc | <Cmd>Bdelete<CR> |
|  |  bl | <Cmd>buffer #<CR> |
|  |  bq | <Cmd>bdelete<CR> |
|  |  w | <Cmd>write<CR> |
|  |  a | :keepjumps normal! ggVG<CR> |
|  |  l | g_ |
|  |  h | ^ |
|  | % | <Plug>(MatchitNormalForward) |
| Nvim builtin | & | :&&<CR> |
| Nvim builtin | Y | y$ |
|  | [% | <Plug>(MatchitNormalMultiBackward) |
|  | ]% | <Plug>(MatchitNormalMultiForward) |
|  | cS | <Plug>CSurround |
|  | cs | <Plug>Csurround |
|  | ds | <Plug>Dsurround |
| Comment insert end of line | gcA |  |
| Comment insert above | gcO |  |
| Comment insert below | gco |  |
| Comment toggle current block | gbc |  |
| Comment toggle current line | gcc |  |
| Comment toggle blockwise | gb | <Plug>(comment_toggle_blockwise) |
| Comment toggle linewise | gc | <Plug>(comment_toggle_linewise) |
|  | gx | <Plug>NetrwBrowseX |
|  | g% | <Plug>(MatchitNormalBackward) |
|  | gp | "+p |
|  | gy | "+y |
|  | x | "_x |
|  | y<C-G> | :<C-U>call setreg(v:register, fugitive#Object(@%))<CR> |
|  | ySS | <Plug>YSsurround |
|  | ySs | <Plug>YSsurround |
|  | yss | <Plug>Yssurround |
|  | yS | <Plug>YSurround |
|  | ys | <Plug>Ysurround |
| Toggle Terminal | <C-G> | <Cmd>execute v:count . "ToggleTerm"<CR> |
|  | <Plug>NetrwBrowseX | :call netrw#BrowseX(netrw#GX(),netrw#CheckIfRemote(netrw#GX()))<CR> |
|  | <Plug>(MatchitNormalMultiForward) | :<C-U>call matchit#MultiMatch("W",  "n")<CR> |
|  | <Plug>(MatchitNormalMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "n")<CR> |
|  | <Plug>(MatchitNormalBackward) | :<C-U>call matchit#Match_wrapper('',0,'n')<CR> |
|  | <Plug>(MatchitNormalForward) | :<C-U>call matchit#Match_wrapper('',1,'n')<CR> |
|  | <Plug>fugitive: |  |
|  | <Plug>fugitive:y<C-G> | :<C-U>call setreg(v:register, fugitive#Object(@%))<CR> |
|  | <Plug>luasnip-expand-repeat |  |
|  | <Plug>luasnip-delete-check |  |
|  | <Plug>YSurround | <SNR>13_opfunc2('setup') |
|  | <Plug>Ysurround | <SNR>13_opfunc('setup') |
|  | <Plug>YSsurround | <SNR>13_opfunc2('setup').'_' |
|  | <Plug>Yssurround | '^'.v:count1.<SNR>13_opfunc('setup').'g_' |
|  | <Plug>CSurround | :<C-U>call <SNR>13_changesurround(1)<CR> |
|  | <Plug>Csurround | :<C-U>call <SNR>13_changesurround()<CR> |
|  | <Plug>Dsurround | :<C-U>call <SNR>13_dosurround(<SNR>13_inputtarget())<CR> |
|  | <Plug>SurroundRepeat | . |
| Comment toggle blockwise with count | <Plug>(comment_toggle_blockwise_count) |  |
| Comment toggle linewise with count | <Plug>(comment_toggle_linewise_count) |  |
| Comment toggle current block | <Plug>(comment_toggle_blockwise_current) |  |
| Comment toggle current line | <Plug>(comment_toggle_linewise_current) |  |
| Comment toggle blockwise | <Plug>(comment_toggle_blockwise) |  |
| Comment toggle linewise | <Plug>(comment_toggle_linewise) |  |
|  | <Plug>PlenaryTestFile | :lua require('plenary.test_harness').test_directory(vim.fn.expand("%:p"))<CR> |
| Nvim builtin | <C-L> | <Cmd>nohlsearch|diffupdate|normal! <C-L><CR> |

#### visual mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  |  l | g_ |
|  |  h | ^ |
| Nvim builtin | # | y?\V<C-R>"<CR> |
|  | % | <Plug>(MatchitVisualForward) |
| Nvim builtin | * | y/\V<C-R>"<CR> |
|  | @(targets) | :<C-U>call targets#do()<CR> |
|  | A | targets#e('o', 'A', 'A') |
|  | I | targets#e('o', 'I', 'I') |
|  | S | <Plug>VSurround |
|  | [% | <Plug>(MatchitVisualMultiBackward) |
|  | ]% | <Plug>(MatchitVisualMultiForward) |
|  | a% | <Plug>(MatchitVisualTextObject) |
|  | a | targets#e('o', 'a', 'a') |
| Comment toggle blockwise (visual) | gb | <Plug>(comment_toggle_blockwise_visual) |
| Comment toggle linewise (visual) | gc | <Plug>(comment_toggle_linewise_visual) |
|  | gx | <Plug>NetrwBrowseXVis |
|  | g% | <Plug>(MatchitVisualBackward) |
|  | gS | <Plug>VgSurround |
|  | gp | "+p |
|  | gy | "+y |
|  | i | targets#e('o', 'i', 'i') |
|  | x | "_x |
|  | <Plug>NetrwBrowseXVis | :<C-U>call netrw#BrowseXVis()<CR> |
|  | <Plug>(MatchitVisualTextObject) | <Plug>(MatchitVisualMultiBackward)o<Plug>(MatchitVisualMultiForward) |
|  | <Plug>(MatchitVisualMultiForward) | :<C-U>call matchit#MultiMatch("W",  "n")<CR>m'gv`` |
|  | <Plug>(MatchitVisualMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "n")<CR>m'gv`` |
|  | <Plug>(MatchitVisualBackward) | :<C-U>call matchit#Match_wrapper('',0,'v')<CR>m'gv`` |
|  | <Plug>(MatchitVisualForward) | :<C-U>call matchit#Match_wrapper('',1,'v')<CR>:if col("''") != col("$") | exe ":normal! m'" | endif<CR>gv`` |
|  | <Plug>luasnip-expand-repeat |  |
| Comment toggle blockwise (visual) | <Plug>(comment_toggle_blockwise_visual) | <Esc><Cmd>lua require("Comment.api").locked("toggle.blockwise")(vim.fn.visualmode())<CR> |
| Comment toggle linewise (visual) | <Plug>(comment_toggle_linewise_visual) | <Esc><Cmd>lua require("Comment.api").locked("toggle.linewise")(vim.fn.visualmode())<CR> |
|  | <Plug>VgSurround | :<C-U>call <SNR>14_opfunc(visualmode(),visualmode() ==# 'V' ? 0 : 1)<CR> |
|  | <Plug>VSurround | :<C-U>call <SNR>14_opfunc(visualmode(),visualmode() ==# 'V' ? 1 : 0)<CR> |

#### operator mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  |  l | g_ |
|  |  h | ^ |
|  | % | <Plug>(MatchitOperationForward) |
|  | @(targets) | :<C-U>call targets#do()<CR> |
|  | A | targets#e('o', 'A', 'A') |
|  | I | targets#e('o', 'I', 'I') |
|  | [% | <Plug>(MatchitOperationMultiBackward) |
|  | ]% | <Plug>(MatchitOperationMultiForward) |
|  | a | targets#e('o', 'a', 'a') |
|  | g% | <Plug>(MatchitOperationBackward) |
|  | i | targets#e('o', 'i', 'i') |
|  | <Plug>(MatchitOperationMultiForward) | :<C-U>call matchit#MultiMatch("W",  "o")<CR> |
|  | <Plug>(MatchitOperationMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "o")<CR> |
|  | <Plug>(MatchitOperationBackward) | :<C-U>call matchit#Match_wrapper('',0,'o')<CR> |
|  | <Plug>(MatchitOperationForward) | :<C-U>call matchit#Match_wrapper('',1,'o')<CR> |
|  | <Plug>luasnip-expand-repeat |  |

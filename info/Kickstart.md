---
layout: post
title: Kickstart Configuration Info
toc: true
post_style: page
---

## Kickstart Neovim Configuration Information

Popular starting point, small, single file, well documented, modular

- Install and initialize: **`lazyman -k`**
- Configuration category: [Starter](https://lazyman.dev/configurations/#starter-configurations)
- Base configuration:     [Kickstart](https://github.com/nvim-lua/kickstart.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- Installation location:  **`~/.config/nvim-Kickstart`**


### Git repository

[https://github.com/doctorfree/kickstart.nvim](https://github.com/doctorfree/kickstart.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### Lazy managed plugins

- [numToStr/Comment.nvim](https://github.com/numToStr/Comment.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp){:target="_blank"}{:rel="noopener noreferrer"}
- [saadparwaiz1/cmp_luasnip](https://github.com/saadparwaiz1/cmp_luasnip){:target="_blank"}{:rel="noopener noreferrer"}
- [j-hui/fidget.nvim](https://github.com/j-hui/fidget.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [rafamadriz/friendly-snippets](https://github.com/rafamadriz/friendly-snippets){:target="_blank"}{:rel="noopener noreferrer"}
- [lewis6991/gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [lukas-reineke/indent-blankline.nvim](https://github.com/lukas-reineke/indent-blankline.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/lazy.nvim](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lualine/lualine.nvim](https://github.com/nvim-lualine/lualine.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [williamboman/mason-lspconfig.nvim](https://github.com/williamboman/mason-lspconfig.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-neo-tree/neo-tree.nvim](https://github.com/nvim-neo-tree/neo-tree.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/neodev.nvim](https://github.com/folke/neodev.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [MunifTanjim/nui.nvim](https://github.com/MunifTanjim/nui.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp){:target="_blank"}{:rel="noopener noreferrer"}
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter-textobjects](https://github.com/nvim-treesitter/nvim-treesitter-textobjects){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons){:target="_blank"}{:rel="noopener noreferrer"}
- [navarasu/onedark.nvim](https://github.com/navarasu/onedark.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-telescope/telescope-fzf-native.nvim](https://github.com/nvim-telescope/telescope-fzf-native.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [tpope/vim-fugitive](https://github.com/tpope/vim-fugitive){:target="_blank"}{:rel="noopener noreferrer"}
- [tpope/vim-rhubarb](https://github.com/tpope/vim-rhubarb){:target="_blank"}{:rel="noopener noreferrer"}
- [tpope/vim-sleuth](https://github.com/tpope/vim-sleuth.git){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/which-key.nvim](https://github.com/folke/which-key.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### Kickstart Keymaps

#### normal mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
| Open diagnostics list |  q |  |
| Open floating diagnostic message |  e |  |
| [S]earch [D]iagnostics |  sd |  |
| [S]earch by [G]rep |  sg |  |
| [S]earch current [W]ord |  sw |  |
| [S]earch [H]elp |  sh |  |
| [S]earch [F]iles |  sf |  |
| Search [G]it [F]iles |  gf |  |
| [/] Fuzzily search in current buffer |  / |  |
| [ ] Find existing buffers |    |  |
| [?] Find recently opened files |  ? |  |
|  |   |  |
|  | % | <Plug>(MatchitNormalForward) |
| Nvim builtin | & | :&&<CR> |
| Nvim builtin | Y | y$ |
| Go to previous diagnostic message | [d |  |
|  | [% | <Plug>(MatchitNormalMultiBackward) |
| Go to next diagnostic message | ]d |  |
|  | ]% | <Plug>(MatchitNormalMultiForward) |
|  | gx | <Plug>NetrwBrowseX |
|  | g% | <Plug>(MatchitNormalBackward) |
| Comment insert end of line | gcA |  |
| Comment insert above | gcO |  |
| Comment insert below | gco |  |
| Comment toggle current block | gbc |  |
| Comment toggle current line | gcc |  |
| Comment toggle blockwise | gb | <Plug>(comment_toggle_blockwise) |
| Comment toggle linewise | gc | <Plug>(comment_toggle_linewise) |
|  | j | v:count == 0 ? 'gj' : 'j' |
|  | k | v:count == 0 ? 'gk' : 'k' |
|  | y<C-G> | :<C-U>call setreg(v:register, fugitive#Object(@%))<CR> |
|  | <Plug>NetrwBrowseX | :call netrw#BrowseX(netrw#GX(),netrw#CheckIfRemote(netrw#GX()))<CR> |
|  | <Plug>(MatchitNormalMultiForward) | :<C-U>call matchit#MultiMatch("W",  "n")<CR> |
|  | <Plug>(MatchitNormalMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "n")<CR> |
|  | <Plug>(MatchitNormalBackward) | :<C-U>call matchit#Match_wrapper('',0,'n')<CR> |
|  | <Plug>(MatchitNormalForward) | :<C-U>call matchit#Match_wrapper('',1,'n')<CR> |
|  | <Plug>luasnip-expand-repeat |  |
|  | <Plug>luasnip-delete-check |  |
|  | <Plug>PlenaryTestFile | :lua require('plenary.test_harness').test_directory(vim.fn.expand("%:p"))<CR> |
| Comment toggle blockwise with count | <Plug>(comment_toggle_blockwise_count) |  |
| Comment toggle linewise with count | <Plug>(comment_toggle_linewise_count) |  |
| Comment toggle current block | <Plug>(comment_toggle_blockwise_current) |  |
| Comment toggle current line | <Plug>(comment_toggle_linewise_current) |  |
| Comment toggle blockwise | <Plug>(comment_toggle_blockwise) |  |
| Comment toggle linewise | <Plug>(comment_toggle_linewise) |  |
|  | <Plug>fugitive: |  |
|  | <Plug>fugitive:y<C-G> | :<C-U>call setreg(v:register, fugitive#Object(@%))<CR> |
| Nvim builtin | <C-L> | <Cmd>nohlsearch|diffupdate|normal! <C-L><CR> |

#### visual mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  |   |  |
| Nvim builtin | # | y?\V<C-R>"<CR> |
|  | % | <Plug>(MatchitVisualForward) |
| Nvim builtin | * | y/\V<C-R>"<CR> |
|  | [% | <Plug>(MatchitVisualMultiBackward) |
|  | ]% | <Plug>(MatchitVisualMultiForward) |
|  | a% | <Plug>(MatchitVisualTextObject) |
|  | gx | <Plug>NetrwBrowseXVis |
|  | g% | <Plug>(MatchitVisualBackward) |
| Comment toggle blockwise (visual) | gb | <Plug>(comment_toggle_blockwise_visual) |
| Comment toggle linewise (visual) | gc | <Plug>(comment_toggle_linewise_visual) |
|  | <Plug>NetrwBrowseXVis | :<C-U>call netrw#BrowseXVis()<CR> |
|  | <Plug>(MatchitVisualTextObject) | <Plug>(MatchitVisualMultiBackward)o<Plug>(MatchitVisualMultiForward) |
|  | <Plug>(MatchitVisualMultiForward) | :<C-U>call matchit#MultiMatch("W",  "n")<CR>m'gv`` |
|  | <Plug>(MatchitVisualMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "n")<CR>m'gv`` |
|  | <Plug>(MatchitVisualBackward) | :<C-U>call matchit#Match_wrapper('',0,'v')<CR>m'gv`` |
|  | <Plug>(MatchitVisualForward) | :<C-U>call matchit#Match_wrapper('',1,'v')<CR>:if col("''") != col("$") | exe ":normal! m'" | endif<CR>gv`` |
|  | <Plug>luasnip-expand-repeat |  |
| Comment toggle blockwise (visual) | <Plug>(comment_toggle_blockwise_visual) | <Esc><Cmd>lua require("Comment.api").locked("toggle.blockwise")(vim.fn.visualmode())<CR> |
| Comment toggle linewise (visual) | <Plug>(comment_toggle_linewise_visual) | <Esc><Cmd>lua require("Comment.api").locked("toggle.linewise")(vim.fn.visualmode())<CR> |

#### operator mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  | % | <Plug>(MatchitOperationForward) |
|  | [% | <Plug>(MatchitOperationMultiBackward) |
|  | ]% | <Plug>(MatchitOperationMultiForward) |
|  | g% | <Plug>(MatchitOperationBackward) |
|  | <Plug>(MatchitOperationMultiForward) | :<C-U>call matchit#MultiMatch("W",  "o")<CR> |
|  | <Plug>(MatchitOperationMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "o")<CR> |
|  | <Plug>(MatchitOperationBackward) | :<C-U>call matchit#Match_wrapper('',0,'o')<CR> |
|  | <Plug>(MatchitOperationForward) | :<C-U>call matchit#Match_wrapper('',1,'o')<CR> |
|  | <Plug>luasnip-expand-repeat |  |

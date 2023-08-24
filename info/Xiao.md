---
layout: post
title: Xiao Configuration Info
toc: true
post_style: page
---

## Xiao Neovim Configuration Information

Personal Neovim configuration of XiaoZhang

- Install and initialize: **`lazyman -w Xiao`**
- Configuration category: [Personal](https://lazyman.dev/configurations/#personal-configurations)
- Base configuration:     Custom
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- Installation location:  **`~/.config/nvim-Xiao`**


### Git repository

[https://github.com/onichandame/nvim-config](https://github.com/onichandame/nvim-config){:target="_blank"}{:rel="noopener noreferrer"}

### Lazy managed plugins

- [hrsh7th/cmp-buffer](https://github.com/hrsh7th/cmp-buffer){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-cmdline](https://github.com/hrsh7th/cmp-cmdline){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-path](https://github.com/hrsh7th/cmp-path){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-vsnip](https://github.com/hrsh7th/cmp-vsnip){:target="_blank"}{:rel="noopener noreferrer"}
- [ekalinin/dockerfile.vim](https://github.com/ekalinin/dockerfile.vim.git){:target="_blank"}{:rel="noopener noreferrer"}
- [rafamadriz/friendly-snippets](https://github.com/rafamadriz/friendly-snippets){:target="_blank"}{:rel="noopener noreferrer"}
- [f-person/git-blame.nvim](https://github.com/f-person/git-blame.nvim.git){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/lazy.nvim](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lua/lsp-status.nvim](https://github.com/nvim-lua/lsp-status.nvim.git){:target="_blank"}{:rel="noopener noreferrer"}
- [arkav/lualine-lsp-progress](https://github.com/arkav/lualine-lsp-progress){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lualine/lualine.nvim](https://github.com/nvim-lualine/lualine.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [williamboman/mason-lspconfig.nvim](https://github.com/williamboman/mason-lspconfig.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [jayp0521/mason-null-ls.nvim](https://github.com/jayp0521/mason-null-ls.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [windwp/nvim-autopairs](https://github.com/windwp/nvim-autopairs){:target="_blank"}{:rel="noopener noreferrer"}
- [kevinhwang91/nvim-bqf](https://github.com/kevinhwang91/nvim-bqf.git){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp){:target="_blank"}{:rel="noopener noreferrer"}
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig){:target="_blank"}{:rel="noopener noreferrer"}
- [ojroques/nvim-osc52](https://github.com/ojroques/nvim-osc52.git){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-tree.lua](https://github.com/kyazdani42/nvim-tree.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter){:target="_blank"}{:rel="noopener noreferrer"}
- [windwp/nvim-ts-autotag](https://github.com/windwp/nvim-ts-autotag){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [simrat39/rust-tools.nvim](https://github.com/simrat39/rust-tools.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [b0o/schemastore.nvim](https://github.com/b0o/schemastore.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [akinsho/toggleterm.nvim](https://github.com/akinsho/toggleterm.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [tpope/vim-fugitive](https://github.com/tpope/vim-fugitive){:target="_blank"}{:rel="noopener noreferrer"}
- [jparise/vim-graphql](https://github.com/jparise/vim-graphql.git){:target="_blank"}{:rel="noopener noreferrer"}
- [farmergreg/vim-lastplace](https://github.com/farmergreg/vim-lastplace.git){:target="_blank"}{:rel="noopener noreferrer"}
- [mzlogin/vim-markdown-toc](https://github.com/mzlogin/vim-markdown-toc.git){:target="_blank"}{:rel="noopener noreferrer"}
- [lbrayner/vim-rzip](https://github.com/lbrayner/vim-rzip.git){:target="_blank"}{:rel="noopener noreferrer"}
- [lifepillar/vim-solarized8](https://github.com/lifepillar/vim-solarized8.git){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/vim-vsnip](https://github.com/hrsh7th/vim-vsnip){:target="_blank"}{:rel="noopener noreferrer"}

### Xiao Keymaps

#### normal mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  |  w | <Cmd>lua vim.lsp.buf.format{timeout_ms=10000, filter = function(client) return client.name ~= "tsserver" end }<CR><Cmd>:w<CR> |
|  |  q | <Cmd>lua vim.diagnostic.setloclist()<CR> |
|  |  e | <Cmd>lua vim.diagnostic.open_float()<CR> |
|  | % | <Plug>(MatchitNormalForward) |
| Nvim builtin | & | :&&<CR> |
|  | ,cc | "+yy |
|  | ,c | "+y |
|  | ,fh |  |
|  | ,fb |  |
|  | ,fg |  |
|  | ,ff |  |
|  | ,t | :ToggleTerm<CR> |
|  | ,wq | :wq<CR> |
|  | ,q | :q<CR> |
|  | ,w | :w<CR> |
| Nvim builtin | Y | y$ |
|  | [g | <Cmd>lua vim.diagnostic.goto_prev()<CR> |
|  | [% | <Plug>(MatchitNormalMultiBackward) |
|  | ]g | <Cmd>lua vim.diagnostic.goto_next()<CR> |
|  | ]% | <Plug>(MatchitNormalMultiForward) |
|  | gx | <Plug>NetrwBrowseX |
|  | g% | <Plug>(MatchitNormalBackward) |
|  | y<C-G> | :<C-U>call setreg(v:register, fugitive#Object(@%))<CR> |
|  | <F2> | :NvimTreeFindFileToggle<CR> |
|  | <Plug>NetrwBrowseX | :call netrw#BrowseX(netrw#GX(),netrw#CheckIfRemote(netrw#GX()))<CR> |
|  | <Plug>(MatchitNormalMultiForward) | :<C-U>call matchit#MultiMatch("W",  "n")<CR> |
|  | <Plug>(MatchitNormalMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "n")<CR> |
|  | <Plug>(MatchitNormalBackward) | :<C-U>call matchit#Match_wrapper('',0,'n')<CR> |
|  | <Plug>(MatchitNormalForward) | :<C-U>call matchit#Match_wrapper('',1,'n')<CR> |
|  | <Plug>fugitive: |  |
|  | <Plug>fugitive:y<C-G> | :<C-U>call setreg(v:register, fugitive#Object(@%))<CR> |
|  | <Plug>(vsnip-cut-text) | :set operatorfunc=<SNR>13_vsnip_cut_text_normal<CR>g@ |
|  | <Plug>(vsnip-select-text) | :set operatorfunc=<SNR>13_vsnip_select_text_normal<CR>g@ |
|  | <Plug>PlenaryTestFile | :lua require('plenary.test_harness').test_directory(vim.fn.expand("%:p"))<CR> |
| Nvim builtin | <C-L> | <Cmd>nohlsearch|diffupdate|normal! <C-L><CR> |

#### visual mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
| Nvim builtin | # | y?\V<C-R>"<CR> |
|  | % | <Plug>(MatchitVisualForward) |
| Nvim builtin | * | y/\V<C-R>"<CR> |
|  | ,c | "+y |
|  | [% | <Plug>(MatchitVisualMultiBackward) |
|  | ]% | <Plug>(MatchitVisualMultiForward) |
|  | a% | <Plug>(MatchitVisualTextObject) |
|  | gx | <Plug>NetrwBrowseXVis |
|  | g% | <Plug>(MatchitVisualBackward) |
|  | <Plug>NetrwBrowseXVis | :<C-U>call netrw#BrowseXVis()<CR> |
|  | <Plug>(MatchitVisualTextObject) | <Plug>(MatchitVisualMultiBackward)o<Plug>(MatchitVisualMultiForward) |
|  | <Plug>(MatchitVisualMultiForward) | :<C-U>call matchit#MultiMatch("W",  "n")<CR>m'gv`` |
|  | <Plug>(MatchitVisualMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "n")<CR>m'gv`` |
|  | <Plug>(MatchitVisualBackward) | :<C-U>call matchit#Match_wrapper('',0,'v')<CR>m'gv`` |
|  | <Plug>(MatchitVisualForward) | :<C-U>call matchit#Match_wrapper('',1,'v')<CR>:if col("''") != col("$") | exe ":normal! m'" | endif<CR>gv`` |
|  | <Plug>(vsnip-cut-text) | :<C-U>call <SNR>7_vsnip_visual_text(visualmode())<CR>gv"_c |
|  | <Plug>(vsnip-select-text) | :<C-U>call <SNR>7_vsnip_visual_text(visualmode())<CR>gv |

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

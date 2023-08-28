---
layout: post
title: Kodo Configuration Info
toc: true
post_style: page
---

## Kodo Neovim Configuration Information

Personal Neovim configuration of chadcat, a high school student with no life. Kodo is a Neovim configuration that looks good and is fast (startuptime < 0.035s).

- Install and initialize: **`lazyman -w Kodo`**
- Configuration category: [Personal](https://lazyman.dev/configurations/#personal-configurations)
- Base configuration:     Custom
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- Installation location:  **`~/.config/lazyman/Kodo`**


### Git repository

[https://github.com/chadcat7/kodo](https://github.com/chadcat7/kodo){:target="_blank"}{:rel="noopener noreferrer"}

### Dotfyle entry

[https://dotfyle.com/chadcat7/kodo](https://dotfyle.com/chadcat7/kodo){:target="_blank"}{:rel="noopener noreferrer"}

### Lazy managed plugins

- [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip){:target="_blank"}{:rel="noopener noreferrer"}
- [goolord/alpha-nvim](https://github.com/goolord/alpha-nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-buffer](https://github.com/hrsh7th/cmp-buffer){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-nvim-lua](https://github.com/hrsh7th/cmp-nvim-lua){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/cmp-path](https://github.com/hrsh7th/cmp-path){:target="_blank"}{:rel="noopener noreferrer"}
- [saadparwaiz1/cmp_luasnip](https://github.com/saadparwaiz1/cmp_luasnip){:target="_blank"}{:rel="noopener noreferrer"}
- [lewis6991/gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [cbochs/grapple.nvim](https://github.com/cbochs/grapple.nvim.git){:target="_blank"}{:rel="noopener noreferrer"}
- [phaazon/hop.nvim](https://github.com/phaazon/hop.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [lukas-reineke/indent-blankline.nvim](https://github.com/lukas-reineke/indent-blankline.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/lazy.nvim](https://github.com/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [onsails/lspkind-nvim](https://github.com/onsails/lspkind-nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [glepnir/lspsaga.nvim](https://github.com/glepnir/lspsaga.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [windwp/nvim-autopairs](https://github.com/windwp/nvim-autopairs){:target="_blank"}{:rel="noopener noreferrer"}
- [code-biscuits/nvim-biscuits](https://github.com/code-biscuits/nvim-biscuits){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp){:target="_blank"}{:rel="noopener noreferrer"}
- [norcalli/nvim-colorizer.lua](https://github.com/norcalli/nvim-colorizer.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [terrortylor/nvim-comment](https://github.com/terrortylor/nvim-comment){:target="_blank"}{:rel="noopener noreferrer"}
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-tree.lua](https://github.com/kyazdani42/nvim-tree.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter){:target="_blank"}{:rel="noopener noreferrer"}
- [windwp/nvim-ts-autotag](https://github.com/windwp/nvim-ts-autotag){:target="_blank"}{:rel="noopener noreferrer"}
- [kevinhwang91/nvim-ufo](https://github.com/kevinhwang91/nvim-ufo){:target="_blank"}{:rel="noopener noreferrer"}
- [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [kevinhwang91/promise-async](https://github.com/kevinhwang91/promise-async){:target="_blank"}{:rel="noopener noreferrer"}
- [simrat39/symbols-outline.nvim](https://github.com/simrat39/symbols-outline.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-telescope/telescope-ui-select.nvim](https://github.com/nvim-telescope/telescope-ui-select.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [akinsho/toggleterm.nvim](https://github.com/akinsho/toggleterm.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [LnL7/vim-nix](https://github.com/LnL7/vim-nix.git){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/which-key.nvim](https://github.com/folke/which-key.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### Kodo Keymaps

#### normal mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  |   |  |
|  | % | <Plug>(MatchitNormalForward) |
| Nvim builtin | & | :&&<CR> |
|  | ' |  |
| Nvim builtin | Y | y$ |
|  | [% | <Plug>(MatchitNormalMultiBackward) |
|  | \ |  |
|  | ]% | <Plug>(MatchitNormalMultiForward) |
|  | ` |  |
|  | gx | <Plug>NetrwBrowseX |
|  | g% | <Plug>(MatchitNormalBackward) |
|  | g |  |
|  | zM | :lua require("ufo").closeAllFolds<CR> |
|  | zR | :lua require("ufo").openAllFolds<CR> |
|  | <C-Bslash> | :ToggleTerm<CR> |
|  | <C-F> | :lua vim.lsp.buf.format()<CR> |
|  | <C-B> | :NvimTreeToggle<CR> |
|  | <C-K> | <C-W>k |
|  | <C-J> | <C-W>j |
|  | <C-H> | <C-W>h |
|  | <Plug>NetrwBrowseX | :call netrw#BrowseX(netrw#GX(),netrw#CheckIfRemote(netrw#GX()))<CR> |
|  | <Plug>(MatchitNormalMultiForward) | :<C-U>call matchit#MultiMatch("W",  "n")<CR> |
|  | <Plug>(MatchitNormalMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "n")<CR> |
|  | <Plug>(MatchitNormalBackward) | :<C-U>call matchit#Match_wrapper('',0,'n')<CR> |
|  | <Plug>(MatchitNormalForward) | :<C-U>call matchit#Match_wrapper('',1,'n')<CR> |
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
|  | <Plug>(MatchitOperationMultiForward) | :<C-U>call matchit#MultiMatch("W",  "o")<CR> |
|  | <Plug>(MatchitOperationMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "o")<CR> |
|  | <Plug>(MatchitOperationBackward) | :<C-U>call matchit#Match_wrapper('',0,'o')<CR> |
|  | <Plug>(MatchitOperationForward) | :<C-U>call matchit#Match_wrapper('',1,'o')<CR> |

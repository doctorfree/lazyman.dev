---
layout: post
title: NvChad Configuration Info
toc: true
post_style: page
---

## NvChad Neovim Configuration Information

Advanced [customization of NvChad](https://github.com/doctorfree/NvChad-custom). Good [introductory video](https://youtu.be/Mtgo-nP_r8Y) to NvChad

- Install and initialize: **`lazyman -c`**
- Configuration category: [Base](https://lazyman.dev/configurations/#base-configurations)
- Base configuration:     [NvChad](https://nvchad.com)
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim)
- Installation location:  **`~/.config/nvim-NvChad`**

### Git repository

[https://github.com/doctorfree/NvChad-custom](https://github.com/doctorfree/NvChad-custom)

### Website

[https://nvchad.lazyman.dev](https://nvchad.lazyman.dev)

### YouTube channel

[https://www.youtube.com/@siduck_og](https://www.youtube.com/@siduck_og)

### Lazy managed plugins

- [numToStr/Comment.nvim](https://github.com/numToStr/Comment.nvim)
- [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip)
- [NvChad/base46](https://github.com/NvChad/base46.git)
- [max397574/better-escape.nvim](https://github.com/max397574/better-escape.nvim)
- [hrsh7th/cmp-buffer](https://github.com/hrsh7th/cmp-buffer)
- [hrsh7th/cmp-cmdline](https://github.com/hrsh7th/cmp-cmdline)
- [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp)
- [hrsh7th/cmp-nvim-lua](https://github.com/hrsh7th/cmp-nvim-lua)
- [hrsh7th/cmp-path](https://github.com/hrsh7th/cmp-path)
- [saadparwaiz1/cmp_luasnip](https://github.com/saadparwaiz1/cmp_luasnip)
- [rafamadriz/friendly-snippets](https://github.com/rafamadriz/friendly-snippets)
- [lewis6991/gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim)
- [olexsmir/gopher.nvim](https://github.com/olexsmir/gopher.nvim.git)
- [phaazon/hop.nvim](https://github.com/phaazon/hop.nvim)
- [lukas-reineke/indent-blankline.nvim](https://github.com/lukas-reineke/indent-blankline.nvim)
- [folke/lazy.nvim](https://github.com/folke/lazy.nvim)
- [williamboman/mason-lspconfig.nvim](https://github.com/williamboman/mason-lspconfig.nvim)
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim)
- [folke/neodev.nvim](https://github.com/folke/neodev.nvim)
- [jayp0521/mason-null-ls.nvim](https://github.com/jayp0521/mason-null-ls.nvim)
- [windwp/nvim-autopairs](https://github.com/windwp/nvim-autopairs)
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp)
- [norcalli/nvim-colorizer.lua](https://github.com/norcalli/nvim-colorizer.lua)
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim)
- [leoluz/nvim-dap-go](https://github.com/leoluz/nvim-dap-go)
- [mfussenegger/nvim-dap-python](https://github.com/mfussenegger/nvim-dap-python.git)
- [rcarriga/nvim-dap-ui](https://github.com/rcarriga/nvim-dap-ui)
- [jose-elias-alvarez/nvim-lsp-ts-utils](https://github.com/jose-elias-alvarez/nvim-lsp-ts-utils)
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig)
- [SmiteshP/nvim-navic](https://github.com/SmiteshP/nvim-navic)
- [kyazdani42/nvim-tree.lua](https://github.com/kyazdani42/nvim-tree.lua)
- [mfussenegger/nvim-treehopper](https://github.com/mfussenegger/nvim-treehopper.git)
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
- [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons)
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim)
- [b0o/schemastore.nvim](https://github.com/b0o/schemastore.nvim)
- [simrat39/symbols-outline.nvim](https://github.com/simrat39/symbols-outline.nvim)
- [ziontee113/syntax-tree-surfer](https://github.com/ziontee113/syntax-tree-surfer.git)
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)
- [rebelot/terminal.nvim](https://github.com/rebelot/terminal.nvim)
- [folke/trouble.nvim](https://github.com/folke/trouble.nvim)
- [bluz71/vim-nightfly-guicolors](https://github.com/bluz71/vim-nightfly-guicolors)
- [folke/which-key.nvim](https://github.com/folke/which-key.nvim)

### NvChad Keymaps

#### normal mode keymaps

|  LHS  |  RHS  | Description |
| ----- | ----- | ----------- |
| <code>"</code> |  |
 | | <code>&</code> | <code>:&&&lt;CR&gt;</code> |
 | Nvim builtin| <code>'</code> |  |
 | | <code>,vO</code> |  |
 | Open new line above HopLineStart target| <code>,vo</code> |  |
 | Open new line below HopLineStart target| <code>,vP</code> |  |
 | Paste above target using HopLineStart| <code>,vp</code> |  |
 | Paste below target using HopLineStart| <code>,hd</code> |  |
 | Jump to definition| <code>,hq]</code> | <code>&lt;Cmd&gt;lua require'hop'.hint_patterns({}, [[}]])&lt;CR&gt;</code> |
 | | <code>,hq[</code> | <code>&lt;Cmd&gt;lua require'hop'.hint_patterns({}, [[{]])&lt;CR&gt;</code> |
 | | <code>,hqk</code> | <code>&lt;Cmd&gt;lua require'hop'.hint_patterns({}, [[)]])&lt;CR&gt;</code> |
 | | <code>,hqj</code> | <code>&lt;Cmd&gt;lua require'hop'.hint_patterns({}, [[(]])&lt;CR&gt;</code> |
 | | <code>,hf/</code> | <code>&lt;Cmd&gt;lua require'hop'.hint_patterns({}, [[/\&#124;?]])&lt;CR&gt;</code> |
 | | <code>,hf;</code> | <code>&lt;Cmd&gt;lua require'hop'.hint_patterns({}, [[;\&#124;:]])&lt;CR&gt;</code> |
 | | <code>,hf-</code> | <code>&lt;Cmd&gt;lua require'hop'.hint_patterns({}, [[-\&#124;+]])&lt;CR&gt;</code> |
 | | <code>,hf'</code> | <code>&lt;Cmd&gt;lua require'hop'.hint_patterns({}, [["\&#124;']])&lt;CR&gt;</code> |
 | | <code>,hH</code> | <code>&lt;Cmd&gt;lua require'hop'.hint_patterns({}, [[\d\+]])&lt;CR&gt;</code> |
 | | <code>,hW</code> | <code>&lt;Cmd&gt;HopWordMW&lt;CR&gt;</code> |
 | | <code>,hl</code> | <code>&lt;Cmd&gt;HopLineStart&lt;CR&gt;</code> |
 | | <code>,hw</code> | <code>&lt;Cmd&gt;HopWord&lt;CR&gt;</code> |
 | | <code>,h]</code> |  |
 | Move to end of Treehopper node| <code>,h[</code> |  |
 | Move to start of Treehopper node| <code>,hm</code> |  |
 | Treehopper nodes| <code>,</code> |  |
 | | <code>?</code> | <code>/</code> |
 | | <code>F</code> |  |
 | | <code>Ls</code> |  |
 | Trigger LuaSnip snippet| <code>T</code> |  |
 | | <code>Y</code> | <code>y$</code> |
 | Nvim builtin| <code>`</code> |  |
 | | <code>c</code> |  |
 | | <code>f</code> |  |
 | | <code>g</code> |  |
 | | <code>gcc</code> |  |
 | Comment toggle current line| <code>gbc</code> |  |
 | Comment toggle current block| <code>gb</code> |  |
 | Comment toggle blockwise| <code>gc</code> |  |
 | Comment toggle linewise| <code>t</code> |  |
 | | <code>vy</code> |  |
 | Treehopper node target insert| <code>vY</code> |  |
 | HopLineStart target in normal mode| <code>vO</code> |  |
 | Open new line above HopLineStart target| <code>vo</code> |  |
 | Open new line below HopLineStart target| <code>vP</code> |  |
 | Paste above target using HopLineStart| <code>vp</code> |  |
 | Paste below target using HopLineStart| <code>v</code> |  |
 | | <code>ym</code> |  |
 | Yank using Treehopper| <code>yc</code> |  |
 | Yank a Treesitter code block| <code>yl</code> |  |
 | Yank a line with HopLineStart| <code>yx</code> |  |
 | Yank user syntax-tree-surfer| <code>&lt;M-q&gt;</code> | <code>q</code> |
 | | <code>&lt;C-R&gt;</code> |  |
 | | <code>&lt;C-L&gt;</code> | <code>&lt;Cmd&gt;nohlsearch&#124;diffupdate|normal! &lt;C-L&gt;&lt;CR&gt;</code> |
 | Nvim builtin
#### visual mode keymaps

|  LHS  |  RHS  | Description |
| ----- | ----- | ----------- |
| <code>#</code> | <code>y?\V&lt;C-R&gt;"&lt;CR&gt;</code> |
 | Nvim builtin| <code>*</code> | <code>y/\V&lt;C-R&gt;"&lt;CR&gt;</code> |
 | Nvim builtin| <code>,hl</code> | <code>&lt;Cmd&gt;HopLineStart&lt;CR&gt;</code> |
 | | <code>,hw</code> | <code>&lt;Cmd&gt;HopWord&lt;CR&gt;</code> |
 | | <code>F</code> |  |
 | | <code>T</code> |  |
 | | <code>f</code> |  |
 | | <code>gb</code> |  |
 | Comment toggle blockwise (visual)| <code>gc</code> |  |
 | Comment toggle linewise (visual)| <code>t</code> |  |
 | | <code>&lt;M-q&gt;</code> | <code>q</code> |
 | 
#### operator mode keymaps

|  LHS  |  RHS  | Description |
| ----- | ----- | ----------- |
| <code>F</code> |  |
 | | <code>T</code> |  |
 | | <code>f</code> |  |
 | | <code>gb</code> |  |
 | Comment toggle blockwise| <code>gc</code> |  |
 | Comment toggle linewise| <code>t</code> |  |
 | 

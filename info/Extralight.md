---
layout: post
title: Extralight Configuration Info
toc: true
post_style: page
---

## Extralight Neovim Configuration Information

Single file lightweight configuration focused on providing basic features

- Install and initialize: **`lazyman -x Extralight`**
- Configuration category: [Starter](https://lazyman.dev/configurations/#starter-configurations)
- Base configuration:     Custom
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim)
- Installation location:  **`~/.config/nvim-Extralight`**

### Git repository

[https://github.com/VonHeikemen/nvim-starter/tree/xx-light](https://github.com/VonHeikemen/nvim-starter/tree/xx-light)

### Lazy managed plugins

- [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip)
- [hrsh7th/cmp-buffer](https://github.com/hrsh7th/cmp-buffer)
- [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp)
- [folke/lazy.nvim](https://github.com/folke/lazy.nvim)
- [VonHeikemen/lsp-zero.nvim](https://github.com/VonHeikemen/lsp-zero.nvim)
- [nvim-lualine/lualine.nvim](https://github.com/nvim-lualine/lualine.nvim)
- [echasnovski/mini.bufremove](https://github.com/echasnovski/mini.bufremove.git)
- [echasnovski/mini.comment](https://github.com/echasnovski/mini.comment)
- [echasnovski/mini.surround](https://github.com/echasnovski/mini.surround.git)
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp)
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig)
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim)
- [nvim-telescope/telescope-fzf-native.nvim](https://github.com/nvim-telescope/telescope-fzf-native.nvim)
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)
- [folke/tokyonight.nvim](https://github.com/folke/tokyonight.nvim)

### Extralight Keymaps

#### normal mode keymaps

|  LHS  |  RHS  | Description |
| ----- | ----- | ----------- |
| <code> fs</code> | <code>&lt;Cmd&gt;Telescope current_buffer_fuzzy_find&lt;CR&gt;</code> |
 | | <code> fd</code> | <code>&lt;Cmd&gt;Telescope diagnostics&lt;CR&gt;</code> |
 | | <code> fg</code> | <code>&lt;Cmd&gt;Telescope live_grep&lt;CR&gt;</code> |
 | | <code> ff</code> | <code>&lt;Cmd&gt;Telescope find_files&lt;CR&gt;</code> |
 | | <code>  </code> | <code>&lt;Cmd&gt;Telescope buffers&lt;CR&gt;</code> |
 | | <code> ?</code> | <code>&lt;Cmd&gt;Telescope oldfiles&lt;CR&gt;</code> |
 | | <code> bc</code> | <code>&lt;Cmd&gt;lua pcall(MiniBufremove.delete)&lt;CR&gt;</code> |
 | | <code> E</code> | <code>&lt;Cmd&gt;Lexplore %:p:h&lt;CR&gt;</code> |
 | | <code> e</code> | <code>&lt;Cmd&gt;Lexplore&lt;CR&gt;</code> |
 | | <code>%</code> | <code>&lt;Plug&gt;(MatchitNormalForward)</code> |
 | | <code>&</code> | <code>:&&&lt;CR&gt;</code> |
 | Nvim builtin| <code>Y</code> | <code>y$</code> |
 | Nvim builtin| <code>[%</code> | <code>&lt;Plug&gt;(MatchitNormalMultiBackward)</code> |
 | | <code>]%</code> | <code>&lt;Plug&gt;(MatchitNormalMultiForward)</code> |
 | | <code>gcc</code> |  |
 | Comment line| <code>gc</code> |  |
 | Comment| <code>gx</code> | <code>&lt;Plug&gt;NetrwBrowseX</code> |
 | | <code>g%</code> | <code>&lt;Plug&gt;(MatchitNormalBackward)</code> |
 | | <code>gp</code> | <code>"+p</code> |
 | | <code>gy</code> | <code>"+y</code> |
 | | <code>shn</code> |  |
 | Highlight next surrounding| <code>sFn</code> |  |
 | Find next left surrounding| <code>sfn</code> |  |
 | Find next right surrounding| <code>srn</code> |  |
 | Replace next surrounding| <code>sdn</code> |  |
 | Delete next surrounding| <code>shl</code> |  |
 | Highlight previous surrounding| <code>sFl</code> |  |
 | Find previous left surrounding| <code>sfl</code> |  |
 | Find previous right surrounding| <code>srl</code> |  |
 | Replace previous surrounding| <code>sdl</code> |  |
 | Delete previous surrounding| <code>sn</code> |  |
 | Update `MiniSurround.config.n_lines`| <code>sh</code> |  |
 | Highlight surrounding| <code>sF</code> |  |
 | Find left surrounding| <code>sf</code> |  |
 | Find right surrounding| <code>sr</code> |  |
 | Replace surrounding| <code>sd</code> |  |
 | Delete surrounding| <code>sa</code> |  |
 | Add surrounding| <code>&lt;Plug&gt;NetrwBrowseX</code> | <code>:call netrw#BrowseX(netrw#GX(),netrw#CheckIfRemote(netrw#GX()))&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalMultiForward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalMultiBackward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalBackward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'n')&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalForward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'n')&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;luasnip-expand-repeat</code> |  |
 | | <code>&lt;Plug&gt;luasnip-delete-check</code> |  |
 | | <code>&lt;Plug&gt;PlenaryTestFile</code> | <code>:lua require('plenary.test_harness').test_directory(vim.fn.expand("%:p"))&lt;CR&gt;</code> |
 | | <code>&lt;C-L&gt;</code> | <code>&lt;Cmd&gt;nohlsearch&#124;diffupdate|normal! &lt;C-L&gt;&lt;CR&gt;</code> |
 | Nvim builtin
#### visual mode keymaps

|  LHS  |  RHS  | Description |
| ----- | ----- | ----------- |
| <code>#</code> | <code>y?\V&lt;C-R&gt;"&lt;CR&gt;</code> |
 | Nvim builtin| <code>%</code> | <code>&lt;Plug&gt;(MatchitVisualForward)</code> |
 | | <code>*</code> | <code>y/\V&lt;C-R&gt;"&lt;CR&gt;</code> |
 | Nvim builtin| <code>[%</code> | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)</code> |
 | | <code>]%</code> | <code>&lt;Plug&gt;(MatchitVisualMultiForward)</code> |
 | | <code>a%</code> | <code>&lt;Plug&gt;(MatchitVisualTextObject)</code> |
 | | <code>gc</code> | <code>:&lt;C-U&gt;lua MiniComment.operator('visual')&lt;CR&gt;</code> |
 | Comment selection| <code>gx</code> | <code>&lt;Plug&gt;NetrwBrowseXVis</code> |
 | | <code>g%</code> | <code>&lt;Plug&gt;(MatchitVisualBackward)</code> |
 | | <code>gp</code> | <code>"+p</code> |
 | | <code>gy</code> | <code>"+y</code> |
 | | <code>sa</code> | <code>:&lt;C-U&gt;lua MiniSurround.add('visual')&lt;CR&gt;</code> |
 | Add surrounding to selection| <code>&lt;Plug&gt;NetrwBrowseXVis</code> | <code>:&lt;C-U&gt;call netrw#BrowseXVis()&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualTextObject)</code> | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)o&lt;Plug&gt;(MatchitVisualMultiForward)</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualMultiForward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualBackward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'v')&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualForward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'v')&lt;CR&gt;:if col("''") != col("$") &#124; exe ":normal! m'" | endif&lt;CR&gt;gv``</code> |
 | | <code>&lt;Plug&gt;luasnip-expand-repeat</code> |  |
 | 
#### operator mode keymaps

|  LHS  |  RHS  | Description |
| ----- | ----- | ----------- |
| <code>%</code> | <code>&lt;Plug&gt;(MatchitOperationForward)</code> |
 | | <code>[%</code> | <code>&lt;Plug&gt;(MatchitOperationMultiBackward)</code> |
 | | <code>]%</code> | <code>&lt;Plug&gt;(MatchitOperationMultiForward)</code> |
 | | <code>gc</code> | <code>&lt;Cmd&gt;lua MiniComment.textobject()&lt;CR&gt;</code> |
 | Comment textobject| <code>g%</code> | <code>&lt;Plug&gt;(MatchitOperationBackward)</code> |
 | | <code>gp</code> | <code>"+p</code> |
 | | <code>gy</code> | <code>"+y</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationMultiForward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "o")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationMultiBackward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "o")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationBackward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'o')&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationForward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'o')&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;luasnip-expand-repeat</code> |  |
 | 

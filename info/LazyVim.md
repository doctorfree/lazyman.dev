---
layout: post
title: LazyVim Configuration Info
toc: true
post_style: page
---

## LazyVim Neovim Configuration Information

The [LazyVim starter](https://github.com/LazyVim/starter) configuration

- Install and initialize: **`lazyman -l`**
- Configuration category: [Base](https://lazyman.dev/configurations/#base-configurations)
- Base configuration:     [LazyVim](https://lazyvim.github.io)
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim)
- Installation location:  **`~/.config/nvim-LazyVim`**

### Git repository

[https://github.com/LazyVim LazyVim/starter](https://github.com/LazyVim LazyVim/starter)

### Website

[https://lazyvim.lazyman.dev](https://lazyvim.lazyman.dev)

### Lazy managed plugins

- [LazyVim/LazyVim](https://github.com/LazyVim/LazyVim.git)
- [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip)
- [goolord/alpha-nvim](https://github.com/goolord/alpha-nvim)
- [akinsho/bufferline.nvim](https://github.com/akinsho/bufferline.nvim)
- [catppuccin/nvim](https://github.com/catppuccin/nvim)
- [hrsh7th/cmp-buffer](https://github.com/hrsh7th/cmp-buffer)
- [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp)
- [hrsh7th/cmp-path](https://github.com/hrsh7th/cmp-path)
- [saadparwaiz1/cmp_luasnip](https://github.com/saadparwaiz1/cmp_luasnip)
- [stevearc/dressing.nvim](https://github.com/stevearc/dressing.nvim)
- [folke/flash.nvim](https://github.com/folke/flash.nvim.git)
- [rafamadriz/friendly-snippets](https://github.com/rafamadriz/friendly-snippets)
- [lewis6991/gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim)
- [lukas-reineke/indent-blankline.nvim](https://github.com/lukas-reineke/indent-blankline.nvim)
- [folke/lazy.nvim](https://github.com/folke/lazy.nvim)
- [nvim-lualine/lualine.nvim](https://github.com/nvim-lualine/lualine.nvim)
- [williamboman/mason-lspconfig.nvim](https://github.com/williamboman/mason-lspconfig.nvim)
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim)
- [echasnovski/mini.ai](https://github.com/echasnovski/mini.ai.git)
- [echasnovski/mini.bufremove](https://github.com/echasnovski/mini.bufremove.git)
- [echasnovski/mini.comment](https://github.com/echasnovski/mini.comment)
- [echasnovski/mini.indentscope](https://github.com/echasnovski/mini.indentscope)
- [echasnovski/mini.pairs](https://github.com/echasnovski/mini.pairs.git)
- [echasnovski/mini.surround](https://github.com/echasnovski/mini.surround.git)
- [nvim-neo-tree/neo-tree.nvim](https://github.com/nvim-neo-tree/neo-tree.nvim)
- [folke/neoconf.nvim](https://github.com/folke/neoconf.nvim.git)
- [folke/neodev.nvim](https://github.com/folke/neodev.nvim)
- [folke/noice.nvim](https://github.com/folke/noice.nvim)
- [MunifTanjim/nui.nvim](https://github.com/MunifTanjim/nui.nvim)
- [jayp0521/mason-null-ls.nvim](https://github.com/jayp0521/mason-null-ls.nvim)
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp)
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig)
- [SmiteshP/nvim-navic](https://github.com/SmiteshP/nvim-navic)
- [rcarriga/nvim-notify](https://github.com/rcarriga/nvim-notify)
- [nvim-pack/nvim-spectre](https://github.com/nvim-pack/nvim-spectre.git)
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
- [nvim-treesitter/nvim-treesitter-textobjects](https://github.com/nvim-treesitter/nvim-treesitter-textobjects)
- [JoosepAlviste/nvim-ts-context-commentstring](https://github.com/JoosepAlviste/nvim-ts-context-commentstring)
- [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons)
- [folke/persistence.nvim](https://github.com/folke/persistence.nvim.git)
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim)
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)
- [folke/todo-comments.nvim](https://github.com/folke/todo-comments.nvim)
- [folke/tokyonight.nvim](https://github.com/folke/tokyonight.nvim)
- [folke/trouble.nvim](https://github.com/folke/trouble.nvim)
- [RRethy/vim-illuminate](https://github.com/RRethy/vim-illuminate)
- [dstein64/vim-startuptime](https://github.com/dstein64/vim-startuptime)
- [folke/which-key.nvim](https://github.com/folke/which-key.nvim)

### LazyVim Keymaps

#### normal mode keymaps

|  LHS  |  RHS  | Description |
| ----- | ----- | ----------- |
| <code> E</code> |  |
 | Explorer NeoTree (cwd)| <code> e</code> |  |
 | Explorer NeoTree (root dir)| <code> fE</code> |  |
 | Explorer NeoTree (cwd)| <code> fe</code> |  |
 | Explorer NeoTree (root dir)| <code> cm</code> |  |
 | Mason| <code> un</code> |  |
 | Dismiss all Notifications| <code> bp</code> |  |
 | Toggle pin| <code> bP</code> |  |
 | Delete non-pinned buffers| <code> snd</code> |  |
 | Dismiss All| <code> sna</code> |  |
 | Noice All| <code> snh</code> |  |
 | Noice History| <code> snl</code> |  |
 | Noice Last Message| <code> fF</code> |  |
 | Find Files (cwd)| <code> sR</code> |  |
 | Resume| <code> sm</code> |  |
 | Jump to Mark| <code> sM</code> |  |
 | Man Pages| <code> sS</code> |  |
 | Goto Symbol (Workspace)| <code> ss</code> |  |
 | Goto Symbol| <code> uC</code> |  |
 | Colorscheme with preview| <code> sW</code> |  |
 | Word (cwd)| <code> sw</code> |  |
 | Word (root dir)| <code> ff</code> |  |
 | Find Files (root dir)| <code> so</code> |  |
 | Options| <code> :</code> |  |
 | Command History| <code> /</code> |  |
 | Grep (root dir)| <code> ,</code> |  |
 | Switch Buffer| <code> sH</code> |  |
 | Search Highlight Groups| <code> sh</code> |  |
 | Help Pages| <code> sG</code> |  |
 | Grep (cwd)| <code> sg</code> |  |
 | Grep (root dir)| <code> sD</code> |  |
 | Workspace diagnostics| <code> sd</code> |  |
 | Document diagnostics| <code> sC</code> |  |
 | Commands| <code> sc</code> |  |
 | Command History| <code> sb</code> |  |
 | Buffer| <code> sa</code> |  |
 | Auto Commands| <code> s"</code> |  |
 | Registers| <code> gs</code> |  |
 | status| <code> gc</code> |  |
 | commits| <code> fR</code> |  |
 | Recent (cwd)| <code> fr</code> |  |
 | Recent| <code> fb</code> |  |
 | Buffers| <code> sk</code> |  |
 | Key Maps| <code>  </code> |  |
 | Find Files (root dir)| <code> sr</code> |  |
 | Replace in files (Spectre)| <code> ql</code> |  |
 | Restore Last Session| <code> qs</code> |  |
 | Restore Session| <code> qd</code> |  |
 | Don't Save Current Session| <code> bD</code> |  |
 | Delete Buffer (Force)| <code> bd</code> |  |
 | Delete Buffer| <code> st</code> |  |
 | Todo| <code> sT</code> |  |
 | Todo/Fix/Fixme| <code> xT</code> |  |
 | Todo/Fix/Fixme (Trouble)| <code> xt</code> |  |
 | Todo (Trouble)| <code> xQ</code> |  |
 | Quickfix List (Trouble)| <code> xL</code> |  |
 | Location List (Trouble)| <code> xX</code> |  |
 | Workspace Diagnostics (Trouble)| <code> xx</code> |  |
 | Document Diagnostics (Trouble)| <code>%</code> | <code>&lt;Plug&gt;(MatchitNormalForward)</code> |
 | | <code>&</code> | <code>:&&&lt;CR&gt;</code> |
 | Nvim builtin| <code>S</code> |  |
 | Flash Treesitter| <code>Y</code> | <code>y$</code> |
 | Nvim builtin| <code>[%</code> | <code>&lt;Plug&gt;(MatchitNormalMultiBackward)</code> |
 | | <code>[t</code> |  |
 | Previous todo comment| <code>[q</code> |  |
 | Previous trouble/quickfix item| <code>[[</code> |  |
 | Prev Reference| <code>]%</code> | <code>&lt;Plug&gt;(MatchitNormalMultiForward)</code> |
 | | <code>]t</code> |  |
 | Next todo comment| <code>]q</code> |  |
 | Next trouble/quickfix item| <code>]]</code> |  |
 | Next Reference| <code>gx</code> | <code>&lt;Plug&gt;NetrwBrowseX</code> |
 | | <code>g%</code> | <code>&lt;Plug&gt;(MatchitNormalBackward)</code> |
 | | <code>gzF</code> |  |
 | Find left surrounding| <code>gzr</code> |  |
 | Replace surrounding| <code>gzh</code> |  |
 | Highlight surrounding| <code>gza</code> |  |
 | Add surrounding| <code>gzf</code> |  |
 | Find right surrounding| <code>gzd</code> |  |
 | Delete surrounding| <code>gzn</code> |  |
 | Update `MiniSurround.config.n_lines`| <code>s</code> |  |
 | Flash| <code>&lt;Plug&gt;NetrwBrowseX</code> | <code>:call netrw#BrowseX(netrw#GX(),netrw#CheckIfRemote(netrw#GX()))&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalMultiForward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalMultiBackward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalBackward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'n')&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalForward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'n')&lt;CR&gt;</code> |
 | | <code>&lt;C-Space&gt;</code> |  |
 | Increment selection| <code>&lt;C-F&gt;</code> |  |
 | Scroll forward| <code>&lt;C-B&gt;</code> |  |
 | Scroll backward| <code>&lt;C-L&gt;</code> | <code>&lt;Cmd&gt;nohlsearch&#124;diffupdate|normal! &lt;C-L&gt;&lt;CR&gt;</code> |
 | Nvim builtin
#### visual mode keymaps

|  LHS  |  RHS  | Description |
| ----- | ----- | ----------- |
| <code> sW</code> |  |
 | Selection (cwd)| <code> sw</code> |  |
 | Selection (root dir)| <code>#</code> | <code>y?\V&lt;C-R&gt;"&lt;CR&gt;</code> |
 | Nvim builtin| <code>%</code> | <code>&lt;Plug&gt;(MatchitVisualForward)</code> |
 | | <code>*</code> | <code>y/\V&lt;C-R&gt;"&lt;CR&gt;</code> |
 | Nvim builtin| <code>R</code> |  |
 | Treesitter Search| <code>S</code> |  |
 | Flash Treesitter| <code>[%</code> | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)</code> |
 | | <code>]%</code> | <code>&lt;Plug&gt;(MatchitVisualMultiForward)</code> |
 | | <code>a%</code> | <code>&lt;Plug&gt;(MatchitVisualTextObject)</code> |
 | | <code>gx</code> | <code>&lt;Plug&gt;NetrwBrowseXVis</code> |
 | | <code>g%</code> | <code>&lt;Plug&gt;(MatchitVisualBackward)</code> |
 | | <code>gza</code> |  |
 | Add surrounding| <code>s</code> |  |
 | Flash| <code>&lt;Plug&gt;NetrwBrowseXVis</code> | <code>:&lt;C-U&gt;call netrw#BrowseXVis()&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualTextObject)</code> | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)o&lt;Plug&gt;(MatchitVisualMultiForward)</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualMultiForward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualBackward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'v')&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualForward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'v')&lt;CR&gt;:if col("''") != col("$") &#124; exe ":normal! m'" | endif&lt;CR&gt;gv``</code> |
 | | <code>&lt;BS&gt;</code> |  |
 | Decrement selection
#### operator mode keymaps

|  LHS  |  RHS  | Description |
| ----- | ----- | ----------- |
| <code>%</code> | <code>&lt;Plug&gt;(MatchitOperationForward)</code> |
 | | <code>R</code> |  |
 | Treesitter Search| <code>S</code> |  |
 | Flash Treesitter| <code>[%</code> | <code>&lt;Plug&gt;(MatchitOperationMultiBackward)</code> |
 | | <code>]%</code> | <code>&lt;Plug&gt;(MatchitOperationMultiForward)</code> |
 | | <code>g%</code> | <code>&lt;Plug&gt;(MatchitOperationBackward)</code> |
 | | <code>r</code> |  |
 | Remote Flash| <code>s</code> |  |
 | Flash| <code>&lt;Plug&gt;(MatchitOperationMultiForward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "o")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationMultiBackward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "o")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationBackward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'o')&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationForward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'o')&lt;CR&gt;</code> |
 | 

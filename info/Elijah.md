---
layout: post
title: Elijah Configuration Info
toc: true
post_style: page
---

## Elijah Neovim Configuration Information

Personal Neovim configuration of Elijah Manor

- Install and initialize: **`lazyman -w Elijah`**
- Configuration category: [Personal](https://lazyman.dev/configurations/#personal-configurations)
- Base configuration:     [LazyVim](https://lazyvim.github.io)
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim)
- Installation location:  **`~/.config/nvim-Elijah`**

### Git repository

[https://github.com/elijahmanor/dotfiles](https://github.com/elijahmanor/dotfiles)

### Website

[https://elijahmanor.com](https://elijahmanor.com)

### YouTube channel

[https://www.youtube.com/@ElijahManor](https://www.youtube.com/@ElijahManor)

### Lazy managed plugins

- [LazyVim/LazyVim](https://github.com/LazyVim/LazyVim.git)
- [goolord/alpha-nvim](https://github.com/goolord/alpha-nvim)
- [catppuccin/nvim](https://github.com/catppuccin/nvim)
- [sindrets/diffview.nvim](https://github.com/sindrets/diffview.nvim.git)
- [Rawnly/gist.nvim](https://github.com/Rawnly/gist.nvim.git)
- [folke/lazy.nvim](https://github.com/folke/lazy.nvim)
- [VidocqH/lsp-lens.nvim](https://github.com/VidocqH/lsp-lens.nvim.git)
- [nvim-lualine/lualine.nvim](https://github.com/nvim-lualine/lualine.nvim)
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim)
- [TimUntersberger/neogit](https://github.com/TimUntersberger/neogit)
- [folke/noice.nvim](https://github.com/folke/noice.nvim)
- [jayp0521/mason-null-ls.nvim](https://github.com/jayp0521/mason-null-ls.nvim)
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig)
- [rcarriga/nvim-notify](https://github.com/rcarriga/nvim-notify)
- [samjwill/nvim-unception](https://github.com/samjwill/nvim-unception.git)
- [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons)
- [pwntester/octo.nvim](https://github.com/pwntester/octo.nvim)
- [stevearc/oil.nvim](https://github.com/stevearc/oil.nvim.git)
- [mhanberg/output-panel.nvim](https://github.com/mhanberg/output-panel.nvim.git)
- [nvim-treesitter/playground](https://github.com/nvim-treesitter/playground)
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim)
- [luukvbaal/statuscol.nvim](https://github.com/luukvbaal/statuscol.nvim)
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)
- [akinsho/toggleterm.nvim](https://github.com/akinsho/toggleterm.nvim)
- [dmmulroy/tsc.nvim](https://github.com/dmmulroy/tsc.nvim)
- [jose-elias-alvarez/typescript.nvim](https://github.com/jose-elias-alvarez/typescript.nvim)
- [christoomey/vim-tmux-navigator](https://github.com/christoomey/vim-tmux-navigator)

### Elijah Keymaps

#### normal mode keymaps

|  LHS  |  RHS  | Description |
| ----- | ----- | ----------- |
| <code> ss</code> |  |
 | Goto Symbol| <code> uC</code> |  |
 | Colorscheme with preview| <code> sW</code> |  |
 | Word (cwd)| <code> sw</code> |  |
 | Word (root dir)| <code> sR</code> | <code>&lt;Cmd&gt;Telescope resume&lt;CR&gt;</code> |
 | Resume| <code> so</code> | <code>&lt;Cmd&gt;Telescope vim_options&lt;CR&gt;</code> |
 | Options| <code> sm</code> | <code>&lt;Cmd&gt;Telescope marks&lt;CR&gt;</code> |
 | Jump to Mark| <code> sM</code> | <code>&lt;Cmd&gt;Telescope man_pages&lt;CR&gt;</code> |
 | Man Pages| <code> sk</code> | <code>&lt;Cmd&gt;Telescope keymaps&lt;CR&gt;</code> |
 | Key Maps| <code> sH</code> | <code>&lt;Cmd&gt;Telescope highlights&lt;CR&gt;</code> |
 | Search Highlight Groups| <code> sh</code> | <code>&lt;Cmd&gt;Telescope help_tags&lt;CR&gt;</code> |
 | Help Pages| <code> sG</code> |  |
 | Grep (cwd)| <code> sg</code> |  |
 | Grep (root dir)| <code> sD</code> | <code>&lt;Cmd&gt;Telescope diagnostics&lt;CR&gt;</code> |
 | Workspace diagnostics| <code> sd</code> | <code>&lt;Cmd&gt;Telescope diagnostics bufnr=0&lt;CR&gt;</code> |
 | Document diagnostics| <code> sC</code> | <code>&lt;Cmd&gt;Telescope commands&lt;CR&gt;</code> |
 | Commands| <code> sc</code> | <code>&lt;Cmd&gt;Telescope command_history&lt;CR&gt;</code> |
 | Command History| <code> sb</code> | <code>&lt;Cmd&gt;Telescope current_buffer_fuzzy_find&lt;CR&gt;</code> |
 | Buffer| <code> sa</code> | <code>&lt;Cmd&gt;Telescope autocommands&lt;CR&gt;</code> |
 | Auto Commands| <code> s"</code> | <code>&lt;Cmd&gt;Telescope registers&lt;CR&gt;</code> |
 | Registers| <code> gs</code> | <code>&lt;Cmd&gt;Telescope git_status&lt;CR&gt;</code> |
 | status| <code> gc</code> | <code>&lt;Cmd&gt;Telescope git_commits&lt;CR&gt;</code> |
 | commits| <code> fR</code> |  |
 | Resume| <code> fr</code> | <code>&lt;Cmd&gt;Telescope oldfiles&lt;CR&gt;</code> |
 | Recent| <code> fF</code> |  |
 | Find Files (cwd)| <code> ff</code> |  |
 | Find Files (root dir)| <code> fb</code> | <code>&lt;Cmd&gt;Telescope buffers&lt;CR&gt;</code> |
 | Buffers| <code> :</code> | <code>&lt;Cmd&gt;Telescope command_history&lt;CR&gt;</code> |
 | Command History| <code> /</code> |  |
 | Grep (root dir)| <code> ,</code> | <code>&lt;Cmd&gt;Telescope buffers show_all_buffers=true&lt;CR&gt;</code> |
 | Switch Buffer| <code>  </code> |  |
 | Find Files (root dir)| <code> sB</code> | <code>:Telescope file_browser file_browser path=%:p:h=%:p:h&lt;CR&gt;</code> |
 | Browse Files| <code> sS</code> |  |
 | Goto Symbol (Workspace)| <code> sr</code> |  |
 | Replace in files (Spectre)| <code> snh</code> |  |
 | Noice History| <code> snl</code> |  |
 | Noice Last Message| <code> snd</code> |  |
 | Dismiss All| <code> sna</code> |  |
 | Noice All| <code> E</code> |  |
 | Explorer NeoTree (cwd)| <code> e</code> |  |
 | Explorer NeoTree (root dir)| <code> fE</code> |  |
 | Explorer NeoTree (cwd)| <code> fe</code> |  |
 | Explorer NeoTree (root dir)| <code> tc</code> |  |
 | Type-check| <code> tr</code> |  |
 | Run Nearest| <code> tT</code> |  |
 | Run All Test Files| <code> tt</code> |  |
 | Run File| <code> tS</code> |  |
 | Stop| <code> tO</code> |  |
 | Toggle Output Panel| <code> to</code> |  |
 | Show Output| <code> ts</code> |  |
 | Toggle Summary| <code> de</code> |  |
 | Eval| <code> du</code> |  |
 | Dap UI| <code> fM</code> |  |
 | Open mini.files (cwd)| <code> fm</code> |  |
 | Open mini.files (directory of current file)| <code> uo</code> |  |
 | Toggle LSP output| <code> st</code> |  |
 | Todo| <code> xT</code> |  |
 | Todo/Fix/Fixme (Trouble)| <code> xt</code> |  |
 | Todo (Trouble)| <code> sT</code> |  |
 | Todo/Fix/Fixme| <code> xQ</code> |  |
 | Quickfix List (Trouble)| <code> xL</code> |  |
 | Location List (Trouble)| <code> xX</code> |  |
 | Workspace Diagnostics (Trouble)| <code> xx</code> |  |
 | Document Diagnostics (Trouble)| <code> bd</code> |  |
 | Delete Buffer| <code> bD</code> |  |
 | Delete Buffer (Force)| <code> bP</code> |  |
 | Delete non-pinned buffers| <code> bp</code> |  |
 | Toggle pin| <code> gd</code> |  |
 | Diffview Open| <code> qd</code> |  |
 | Don't Save Current Session| <code> ql</code> |  |
 | Restore Last Session| <code> qs</code> |  |
 | Restore Session| <code> dw</code> |  |
 | Widgets| <code> dt</code> |  |
 | Terminate| <code> ds</code> |  |
 | Session| <code> dr</code> |  |
 | Toggle REPL| <code> dp</code> |  |
 | Pause| <code> dO</code> |  |
 | Step Over| <code> do</code> |  |
 | Step Out| <code> dl</code> |  |
 | Run Last| <code> dk</code> |  |
 | Up| <code> dj</code> |  |
 | Down| <code> di</code> |  |
 | Step Into| <code> dg</code> |  |
 | Go to line (no execute)| <code> dC</code> |  |
 | Run to Cursor| <code> dc</code> |  |
 | Continue| <code> db</code> |  |
 | Toggle Breakpoint| <code> dB</code> |  |
 | Breakpoint Condition| <code> td</code> |  |
 | Debug Nearest| <code> un</code> |  |
 | Dismiss all Notifications| <code> p</code> |  |
 | Open Yank History| <code> cm</code> |  |
 | Mason| <code> gn</code> |  |
 | Neogit| <code>%</code> | <code>&lt;Plug&gt;(MatchitNormalForward)</code> |
 | | <code>&</code> | <code>:&&&lt;CR&gt;</code> |
 | Nvim builtin| <code>-</code> |  |
 | Open parent directory| <code>&lt;lt&gt;P</code> |  |
 | Put before and indent left| <code>&lt;lt&gt;p</code> |  |
 | Put and indent left| <code>=p</code> |  |
 | Put after applying a filter| <code>=P</code> |  |
 | Put before applying a filter| <code>&gt;P</code> |  |
 | Put before and indent right| <code>&gt;p</code> |  |
 | Put and indent right| <code>P</code> |  |
 | Put yanked text before cursor| <code>S</code> |  |
 | Flash Treesitter| <code>Y</code> | <code>y$</code> |
 | Nvim builtin| <code>[%</code> | <code>&lt;Plug&gt;(MatchitNormalMultiBackward)</code> |
 | | <code>[t</code> |  |
 | Previous todo comment| <code>[q</code> |  |
 | Previous trouble/quickfix item| <code>[[</code> |  |
 | Prev Reference| <code>[y</code> |  |
 | Cycle forward through yank history| <code>[p</code> |  |
 | Put indented before cursor (linewise)| <code>[P</code> |  |
 | Put indented before cursor (linewise)| <code>]%</code> | <code>&lt;Plug&gt;(MatchitNormalMultiForward)</code> |
 | | <code>]t</code> |  |
 | Next todo comment| <code>]q</code> |  |
 | Next trouble/quickfix item| <code>]]</code> |  |
 | Next Reference| <code>]y</code> |  |
 | Cycle backward through yank history| <code>]p</code> |  |
 | Put indented after cursor (linewise)| <code>]P</code> |  |
 | Put indented after cursor (linewise)| <code>gx</code> | <code>&lt;Plug&gt;NetrwBrowseX</code> |
 | | <code>g%</code> | <code>&lt;Plug&gt;(MatchitNormalBackward)</code> |
 | | <code>gP</code> |  |
 | Put yanked text before selection| <code>gp</code> |  |
 | Put yanked text after selection| <code>gza</code> |  |
 | Add surrounding| <code>gzd</code> |  |
 | Delete surrounding| <code>gzF</code> |  |
 | Find left surrounding| <code>gzn</code> |  |
 | Update `MiniSurround.config.n_lines`| <code>gzr</code> |  |
 | Replace surrounding| <code>gzf</code> |  |
 | Find right surrounding| <code>gzh</code> |  |
 | Highlight surrounding| <code>p</code> |  |
 | Put yanked text after cursor| <code>s</code> |  |
 | Flash| <code>y</code> |  |
 | Yank text| <code>&lt;Plug&gt;NetrwBrowseX</code> | <code>:call netrw#BrowseX(netrw#GX(),netrw#CheckIfRemote(netrw#GX()))&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalMultiForward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalMultiBackward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalBackward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'n')&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalForward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'n')&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;PlenaryTestFile</code> | <code>:lua require('plenary.test_harness').test_directory(vim.fn.expand("%:p"))&lt;CR&gt;</code> |
 | | <code>&lt;C-Bslash&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigatePrevious&lt;CR&gt;</code> |
 | | <code>&lt;C-K&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigateUp&lt;CR&gt;</code> |
 | | <code>&lt;C-J&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigateDown&lt;CR&gt;</code> |
 | | <code>&lt;C-H&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigateLeft&lt;CR&gt;</code> |
 | | <code>&lt;C-F&gt;</code> |  |
 | Scroll forward| <code>&lt;C-B&gt;</code> |  |
 | Scroll backward| <code>&lt;C-L&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigateRight&lt;CR&gt;</code> |
 | 
#### visual mode keymaps

|  LHS  |  RHS  | Description |
| ----- | ----- | ----------- |
| <code> sW</code> |  |
 | Selection (cwd)| <code> sw</code> |  |
 | Selection (root dir)| <code> de</code> |  |
 | Eval| <code>#</code> | <code>y?\V&lt;C-R&gt;"&lt;CR&gt;</code> |
 | Nvim builtin| <code>%</code> | <code>&lt;Plug&gt;(MatchitVisualForward)</code> |
 | | <code>*</code> | <code>y/\V&lt;C-R&gt;"&lt;CR&gt;</code> |
 | Nvim builtin| <code>P</code> |  |
 | Put yanked text before cursor| <code>R</code> |  |
 | Treesitter Search| <code>S</code> |  |
 | Flash Treesitter| <code>[%</code> | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)</code> |
 | | <code>]%</code> | <code>&lt;Plug&gt;(MatchitVisualMultiForward)</code> |
 | | <code>a%</code> | <code>&lt;Plug&gt;(MatchitVisualTextObject)</code> |
 | | <code>gx</code> | <code>&lt;Plug&gt;NetrwBrowseXVis</code> |
 | | <code>g%</code> | <code>&lt;Plug&gt;(MatchitVisualBackward)</code> |
 | | <code>gP</code> |  |
 | Put yanked text before selection| <code>gp</code> |  |
 | Put yanked text after selection| <code>gza</code> |  |
 | Add surrounding| <code>p</code> |  |
 | Put yanked text after cursor| <code>s</code> |  |
 | Flash| <code>y</code> |  |
 | Yank text| <code>&lt;Plug&gt;NetrwBrowseXVis</code> | <code>:&lt;C-U&gt;call netrw#BrowseXVis()&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualTextObject)</code> | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)o&lt;Plug&gt;(MatchitVisualMultiForward)</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualMultiForward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualBackward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'v')&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualForward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'v')&lt;CR&gt;:if col("''") != col("$") &#124; exe ":normal! m'" | endif&lt;CR&gt;gv``</code> |
 | | <code>&lt;C-Bslash&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigatePrevious&lt;CR&gt;</code> |
 | | <code>&lt;C-K&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigateUp&lt;CR&gt;</code> |
 | | <code>&lt;C-J&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigateDown&lt;CR&gt;</code> |
 | | <code>&lt;C-H&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigateLeft&lt;CR&gt;</code> |
 | | <code>&lt;C-L&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigateRight&lt;CR&gt;</code> |
 | 
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
 | | <code>&lt;C-Bslash&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigatePrevious&lt;CR&gt;</code> |
 | | <code>&lt;C-K&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigateUp&lt;CR&gt;</code> |
 | | <code>&lt;C-J&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigateDown&lt;CR&gt;</code> |
 | | <code>&lt;C-H&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigateLeft&lt;CR&gt;</code> |
 | | <code>&lt;C-L&gt;</code> | <code>:&lt;C-U&gt;TmuxNavigateRight&lt;CR&gt;</code> |
 | 

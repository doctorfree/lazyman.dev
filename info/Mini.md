---
layout: post
title: Mini Configuration Info
toc: true
post_style: page
---

## Mini Neovim Configuration Information

Uses the [mini.nvim](https://github.com/echasnovski/mini.nvim) library. Personal configuration of the 'mini.nvim' author

- Install and initialize: **`lazyman -M`**
- Configuration category: [Personal](https://lazyman.dev/configurations/#personal-configurations)
- Base configuration:     Custom
- Plugin manager:         [Mini](https://github.com/echasnovski/mini.nvim)
- Installation location:  **`~/.config/nvim-Mini`**

### Git repository

[https://github.com/echasnovski/nvim](https://github.com/echasnovski/nvim)

### Neovimcraft entry

[http://neovimcraft.com/plugin/echasnovski/nvim](http://neovimcraft.com/plugin/echasnovski/nvim)

### Mini.nvim managed plugins


### Mini Keymaps

#### normal mode keymaps

|  LHS  |  RHS  | Description |
| :---- | ----: | :---------- |
| <code> Ts</code> | <code>&lt;Cmd&gt;TestSuite&lt;CR&gt;</code> |
 | Suite| <code> TS</code> | <code>&lt;Cmd&gt;TestSuite -strategy=make &#124; copen&lt;CR&gt;</code> |
 | Suite (quickfix)| <code> Tn</code> | <code>&lt;Cmd&gt;TestNearest&lt;CR&gt;</code> |
 | Nearest| <code> TN</code> | <code>&lt;Cmd&gt;TestNearest -strategy=make &#124; copen&lt;CR&gt;</code> |
 | Nearest (quickfix)| <code> Tl</code> | <code>&lt;Cmd&gt;TestLast&lt;CR&gt;</code> |
 | Last| <code> TL</code> | <code>&lt;Cmd&gt;TestLast -strategy=make &#124; copen&lt;CR&gt;</code> |
 | Last (quickfix)| <code> Tf</code> | <code>&lt;Cmd&gt;TestFile&lt;CR&gt;</code> |
 | File| <code> TF</code> | <code>&lt;Cmd&gt;TestFile -strategy=make &#124; copen&lt;CR&gt;</code> |
 | File (quickfix)| <code> tt</code> | <code>&lt;Cmd&gt;vertical Tnew&lt;CR&gt;</code> |
 | Terminal (vertical)| <code> tT</code> | <code>&lt;Cmd&gt;belowright Tnew&lt;CR&gt;</code> |
 | Terminal (horizontal)| <code> ts</code> | <code>&lt;Cmd&gt;lua EC.minitest_screenshots.browse()&lt;CR&gt;</code> |
 | Test show screenshot| <code> tl</code> | <code>&lt;Cmd&gt;lua MiniTest.run_at_location()&lt;CR&gt;</code> |
 | Test run location| <code> tf</code> | <code>&lt;Cmd&gt;lua MiniTest.run_file()&lt;CR&gt;</code> |
 | Test run file| <code> ta</code> | <code>&lt;Cmd&gt;lua MiniTest.run()&lt;CR&gt;</code> |
 | Test run all| <code> s</code> | <code>&lt;Cmd&gt;TREPLSendLine&lt;CR&gt;j</code> |
 | Send to terminal| <code> rt</code> | <code>&lt;Cmd&gt;T devtools::test()&lt;CR&gt;</code> |
 | Test| <code> rT</code> | <code>&lt;Cmd&gt;T testthat::test_file("%")&lt;CR&gt;</code> |
 | Test file| <code> rl</code> | <code>&lt;Cmd&gt;T devtools::load_all()&lt;CR&gt;</code> |
 | Load all| <code> rk</code> | <code>&lt;Cmd&gt;T rmarkdown::render("%")&lt;CR&gt;</code> |
 | Knit file| <code> ri</code> | <code>&lt;Cmd&gt;T devtools::install(keep_source=TRUE)&lt;CR&gt;</code> |
 | Install| <code> rd</code> | <code>&lt;Cmd&gt;T devtools::document()&lt;CR&gt;</code> |
 | Document| <code> rC</code> | <code>&lt;Cmd&gt;T devtools::test_coverage()&lt;CR&gt;</code> |
 | Coverage| <code> rc</code> | <code>&lt;Cmd&gt;T devtools::check()&lt;CR&gt;</code> |
 | Check| <code> oz</code> | <code>&lt;Cmd&gt;lua MiniMisc.zoom()&lt;CR&gt;</code> |
 | Zoom toggle| <code> oT</code> | <code>&lt;Cmd&gt;lua vim.b.minitrailspace_disable = not vim.b.minitrailspace_disable&lt;CR&gt;</code> |
 | Trailspace hl toggle| <code> ot</code> | <code>&lt;Cmd&gt;lua MiniTrailspace.trim()&lt;CR&gt;</code> |
 | Trim trailspace| <code> oS</code> | <code>&lt;Cmd&gt;lua EC.insert_section()&lt;CR&gt;</code> |
 | Section insert| <code> os</code> | <code>&lt;Cmd&gt;lua MiniSessions.select()&lt;CR&gt;</code> |
 | Session select| <code> or</code> | <code>&lt;Cmd&gt;lua MiniMisc.resize_window()&lt;CR&gt;</code> |
 | Resize to default width| <code> ol</code> | <code>&lt;Cmd&gt;normal gxiagxina&lt;CR&gt;</code> |
 | Move arg right| <code> og</code> | <code>&lt;Cmd&gt;lua MiniDoc.generate()&lt;CR&gt;</code> |
 | Generate plugin doc| <code> oH</code> | <code>&lt;Cmd&gt;TSBufToggle highlight&lt;CR&gt;</code> |
 | Highlight toggle| <code> oh</code> | <code>&lt;Cmd&gt;normal gxiagxila&lt;CR&gt;</code> |
 | Move arg left| <code> od</code> | <code>&lt;Cmd&gt;Neogen&lt;CR&gt;</code> |
 | Document| <code> oC</code> | <code>&lt;Cmd&gt;lua MiniCursorword.toggle()&lt;CR&gt;</code> |
 | Cursor word hl toggle| <code> mt</code> | <code>&lt;Cmd&gt;lua MiniMap.toggle()&lt;CR&gt;</code> |
 | Toggle| <code> ms</code> | <code>&lt;Cmd&gt;lua MiniMap.toggle_side()&lt;CR&gt;</code> |
 | Side (toggle)| <code> mr</code> | <code>&lt;Cmd&gt;lua MiniMap.refresh()&lt;CR&gt;</code> |
 | Refresh| <code> mo</code> | <code>&lt;Cmd&gt;lua MiniMap.open()&lt;CR&gt;</code> |
 | Open| <code> mf</code> | <code>&lt;Cmd&gt;lua MiniMap.toggle_focus()&lt;CR&gt;</code> |
 | Focus (toggle)| <code> mc</code> | <code>&lt;Cmd&gt;lua MiniMap.close()&lt;CR&gt;</code> |
 | Close| <code> Lx</code> | <code>&lt;Cmd&gt;lua EC.execute_lua_line()&lt;CR&gt;</code> |
 | Execute `lua` line| <code> Lf</code> | <code>&lt;Cmd&gt;luafile %&lt;CR&gt;</code> |
 | `luafile` buffer| <code> ls</code> | <code>&lt;Cmd&gt;lua vim.lsp.buf.definition()&lt;CR&gt;</code> |
 | Source definition| <code> lr</code> | <code>&lt;Cmd&gt;lua vim.lsp.buf.rename()&lt;CR&gt;</code> |
 | Rename| <code> lR</code> | <code>&lt;Cmd&gt;lua vim.lsp.buf.references()&lt;CR&gt;</code> |
 | References| <code> lk</code> | <code>&lt;Cmd&gt;lua vim.diagnostic.goto_prev()&lt;CR&gt;</code> |
 | Prev diagnostic| <code> lj</code> | <code>&lt;Cmd&gt;lua vim.diagnostic.goto_next()&lt;CR&gt;</code> |
 | Next diagnostic| <code> li</code> | <code>&lt;Cmd&gt;lua vim.lsp.buf.hover()&lt;CR&gt;</code> |
 | Information| <code> lf</code> | <code>&lt;Cmd&gt;lua vim.lsp.buf.format({ async = true })&lt;CR&gt;</code> |
 | Format| <code> ld</code> | <code>&lt;Cmd&gt;lua vim.diagnostic.open_float()&lt;CR&gt;</code> |
 | Diagnostics popup| <code> la</code> | <code>&lt;Cmd&gt;lua vim.lsp.buf.signature_help()&lt;CR&gt;</code> |
 | Arguments popup| <code> gX</code> | <code>&lt;Cmd&gt;lua require("gitsigns").reset_buffer()&lt;CR&gt;</code> |
 | Discard (reset) buffer| <code> gx</code> | <code>&lt;Cmd&gt;lua require("gitsigns").reset_hunk()&lt;CR&gt;</code> |
 | Discard (reset) hunk| <code> gu</code> | <code>&lt;Cmd&gt;lua require("gitsigns").undo_stage_hunk()&lt;CR&gt;</code> |
 | Undo stage hunk| <code> gq</code> | <code>&lt;Cmd&gt;lua require("gitsigns").setqflist()&lt;CR&gt;:copen&lt;CR&gt;</code> |
 | Quickfix hunks| <code> gp</code> | <code>&lt;Cmd&gt;lua require("gitsigns").preview_hunk()&lt;CR&gt;</code> |
 | Preview hunk| <code> gg</code> | <code>&lt;Cmd&gt;lua EC.open_lazygit()&lt;CR&gt;</code> |
 | Git tab| <code> gb</code> | <code>&lt;Cmd&gt;lua require("gitsigns").blame_line()&lt;CR&gt;</code> |
 | Blame line| <code> ga</code> | <code>&lt;Cmd&gt;lua require("gitsigns").stage_hunk()&lt;CR&gt;</code> |
 | Add (stage) hunk| <code> gA</code> | <code>&lt;Cmd&gt;lua require("gitsigns").stage_buffer()&lt;CR&gt;</code> |
 | Add buffer| <code> ft</code> | <code>&lt;Cmd&gt;Telescope file_browser&lt;CR&gt;</code> |
 | File browser| <code> fS</code> | <code>&lt;Cmd&gt;Telescope treesitter&lt;CR&gt;</code> |
 | Symbols (treesitter)| <code> fs</code> | <code>&lt;Cmd&gt;Telescope spell_suggest&lt;CR&gt;</code> |
 | Spell suggestions| <code> fR</code> | <code>&lt;Cmd&gt;Telescope lsp_references&lt;CR&gt;</code> |
 | References (LSP)| <code> fr</code> | <code>&lt;Cmd&gt;lua MiniPick.builtin.resume()&lt;CR&gt;</code> |
 | Resume| <code> fO</code> | <code>&lt;Cmd&gt;Telescope vim_options&lt;CR&gt;</code> |
 | Options| <code> fo</code> | <code>&lt;Cmd&gt;Telescope oldfiles&lt;CR&gt;</code> |
 | Old files| <code> fj</code> | <code>&lt;Cmd&gt;Telescope jumplist&lt;CR&gt;</code> |
 | Jumplist| <code> fH</code> | <code>&lt;Cmd&gt;Telescope highlights&lt;CR&gt;</code> |
 | Highlight groups| <code> fh</code> | <code>&lt;Cmd&gt;lua MiniPick.builtin.help()&lt;CR&gt;</code> |
 | Help tags| <code> fg</code> | <code>&lt;Cmd&gt;lua MiniPick.builtin.grep_live()&lt;CR&gt;</code> |
 | Grep live| <code> ff</code> | <code>&lt;Cmd&gt;lua MiniPick.builtin.files()&lt;CR&gt;</code> |
 | Files| <code> fD</code> | <code>&lt;Cmd&gt;Telescope diagnostics bufnr=0&lt;CR&gt;</code> |
 | Diagnostic buffer| <code> fd</code> | <code>&lt;Cmd&gt;Telescope diagnostics&lt;CR&gt;</code> |
 | Diagnostic workspace| <code> fC</code> | <code>&lt;Cmd&gt;Telescope git_bcommits&lt;CR&gt;</code> |
 | Buffer commits| <code> fc</code> | <code>&lt;Cmd&gt;Telescope git_commits&lt;CR&gt;</code> |
 | Commits| <code> fB</code> | <code>&lt;Cmd&gt;Telescope current_buffer_fuzzy_find&lt;CR&gt;</code> |
 | Open buffers| <code> fb</code> | <code>&lt;Cmd&gt;lua MiniPick.builtin.buffers()&lt;CR&gt;</code> |
 | Open buffers| <code> f:</code> | <code>&lt;Cmd&gt;Telescope command_history&lt;CR&gt;</code> |
 | Commands| <code> f/</code> | <code>&lt;Cmd&gt;Telescope search_history&lt;CR&gt;</code> |
 | "/" history| <code> eq</code> | <code>&lt;Cmd&gt;lua EC.toggle_quickfix()&lt;CR&gt;</code> |
 | Quickfix| <code> em</code> | <code>&lt;Cmd&gt;lua MiniFiles.open('~/.config/nvim-Mini/pack/plugins/opt/mini')&lt;CR&gt;</code> |
 | Mini.nvim directory| <code> ef</code> | <code>&lt;Cmd&gt;lua MiniFiles.open(vim.api.nvim_buf_get_name(0))&lt;CR&gt;</code> |
 | File directory| <code> ed</code> | <code>&lt;Cmd&gt;lua MiniFiles.open()&lt;CR&gt;</code> |
 | Directory| <code> bW</code> | <code>&lt;Cmd&gt;lua MiniBufremove.wipeout(0, true)&lt;CR&gt;</code> |
 | Wipeout!| <code> bw</code> | <code>&lt;Cmd&gt;lua MiniBufremove.wipeout()&lt;CR&gt;</code> |
 | Wipeout| <code> bs</code> | <code>&lt;Cmd&gt;lua EC.new_scratch_buffer()&lt;CR&gt;</code> |
 | Scratch| <code> bD</code> | <code>&lt;Cmd&gt;lua MiniBufremove.delete(0, true)&lt;CR&gt;</code> |
 | Delete!| <code> bd</code> | <code>&lt;Cmd&gt;lua MiniBufremove.delete()&lt;CR&gt;</code> |
 | Delete| <code> ba</code> | <code>&lt;Cmd&gt;b#&lt;CR&gt;</code> |
 | Alternate| <code>%</code> | <code>&lt;Plug&gt;(MatchitNormalForward)</code> |
 | | <code>&</code> | <code>:&&&lt;CR&gt;</code> |
 | Nvim builtin| <code>Y</code> | <code>y$</code> |
 | Nvim builtin| <code>[%</code> | <code>&lt;Plug&gt;(MatchitNormalMultiBackward)</code> |
 | | <code>[p</code> | <code>&lt;Cmd&gt;exe "put! " . v:register&lt;CR&gt;</code> |
 | Paste Above| <code>\h</code> |  |
 | Toggle hlsearch| <code>]%</code> | <code>&lt;Plug&gt;(MatchitNormalMultiForward)</code> |
 | | <code>]p</code> | <code>&lt;Cmd&gt;exe "put "  . v:register&lt;CR&gt;</code> |
 | Paste Below| <code>gx</code> | <code>&lt;Plug&gt;NetrwBrowseX</code> |
 | | <code>g%</code> | <code>&lt;Plug&gt;(MatchitNormalBackward)</code> |
 | | <code>s</code> | <code></code> |
 | | <code>&lt;Plug&gt;NetrwBrowseX</code> | <code>:call netrw#BrowseX(netrw#GX(),netrw#CheckIfRemote(netrw#GX()))&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalMultiForward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalMultiBackward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalBackward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'n')&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalForward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'n')&lt;CR&gt;</code> |
 | | <code>&lt;C-L&gt;</code> | <code>&lt;Cmd&gt;nohlsearch&#124;diffupdate|normal! &lt;C-L&gt;&lt;CR&gt;</code> |
 | Nvim builtin
#### visual mode keymaps

|  LHS  |  RHS  | Description |
| :---- | ----: | :---------- |
| <code> s</code> | <code>mode() ==# "v" ? ":TREPLSendSelection&lt;CR&gt;`&gt;l" : ":TREPLSendSelection&lt;CR&gt;'&gt;j"</code> |
 | Send to terminal| <code> rx</code> | <code>"+y :T reprex::reprex()&lt;CR&gt;</code> |
 | Reprex selection| <code> lf</code> | <code>&lt;Cmd&gt;lua vim.lsp.buf.format()&lt;CR&gt;&lt;Esc&gt;</code> |
 | Format selection| <code>#</code> | <code>y?\V&lt;C-R&gt;"&lt;CR&gt;</code> |
 | Nvim builtin| <code>%</code> | <code>&lt;Plug&gt;(MatchitVisualForward)</code> |
 | | <code>*</code> | <code>y/\V&lt;C-R&gt;"&lt;CR&gt;</code> |
 | Nvim builtin| <code>[%</code> | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)</code> |
 | | <code>[p</code> | <code>&lt;Cmd&gt;exe "put! " . v:register&lt;CR&gt;</code> |
 | Paste Above| <code>]%</code> | <code>&lt;Plug&gt;(MatchitVisualMultiForward)</code> |
 | | <code>]p</code> | <code>&lt;Cmd&gt;exe "put "  . v:register&lt;CR&gt;</code> |
 | Paste Below| <code>a%</code> | <code>&lt;Plug&gt;(MatchitVisualTextObject)</code> |
 | | <code>gx</code> | <code>&lt;Plug&gt;NetrwBrowseXVis</code> |
 | | <code>g%</code> | <code>&lt;Plug&gt;(MatchitVisualBackward)</code> |
 | | <code>s</code> | <code></code> |
 | | <code>&lt;Plug&gt;NetrwBrowseXVis</code> | <code>:&lt;C-U&gt;call netrw#BrowseXVis()&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualTextObject)</code> | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)o&lt;Plug&gt;(MatchitVisualMultiForward)</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualMultiForward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualBackward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'v')&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualForward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'v')&lt;CR&gt;:if col("''") != col("$") &#124; exe ":normal! m'" | endif&lt;CR&gt;gv``</code> |
 | 
#### operator mode keymaps

|  LHS  |  RHS  | Description |
| :---- | ----: | :---------- |
| <code>%</code> | <code>&lt;Plug&gt;(MatchitOperationForward)</code> |
 | | <code>[%</code> | <code>&lt;Plug&gt;(MatchitOperationMultiBackward)</code> |
 | | <code>]%</code> | <code>&lt;Plug&gt;(MatchitOperationMultiForward)</code> |
 | | <code>g%</code> | <code>&lt;Plug&gt;(MatchitOperationBackward)</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationMultiForward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "o")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationMultiBackward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "o")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationBackward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'o')&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationForward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'o')&lt;CR&gt;</code> |
 | 

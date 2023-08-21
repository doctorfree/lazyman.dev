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

- [lewis6991/gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim)
- [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip)
- [iamcco/markdown-preview.nvim](https://github.com/iamcco/markdown-preview.nvim)
- [echasnovski/mini.nvim](https://github.com/echasnovski/mini.nvim)
- [danymat/neogen](https://github.com/danymat/neogen.git)
- [kassio/neoterm](https://github.com/kassio/neoterm)
- [jose-elias-alvarez/null-ls.nvim](https://github.com/jose-elias-alvarez/null-ls.nvim)
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig)
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
- [nvim-treesitter/nvim-treesitter-textobjects](https://github.com/nvim-treesitter/nvim-treesitter-textobjects)
- [nvim-tree/nvim-web-devicons](https://github.com/nvim-tree/nvim-web-devicons)
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim)
- [mechatroner/rainbow_csv](https://github.com/mechatroner/rainbow_csv)
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim.git)
- [tpope/vim-dispatch](https://github.com/tpope/vim-dispatch)
- [tommcdo/vim-exchange](https://github.com/tommcdo/vim-exchange)
- [vim-pandoc/vim-pandoc](https://github.com/vim-pandoc/vim-pandoc)
- [vim-pandoc/vim-pandoc-syntax](https://github.com/vim-pandoc/vim-pandoc-syntax)
- [vim-pandoc/vim-rmarkdown](https://github.com/vim-pandoc/vim-rmarkdown)
- [vim-test/vim-test](https://github.com/vim-test/vim-test)
- [folke/which-key.nvim](https://github.com/folke/which-key.nvim)

### Mini Keymaps

#### normal mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  |  rk | <Cmd>T rmarkdown::render("%")<CR> |
|  |  rd | <Cmd>T devtools::document()<CR> |
|  |  rl | <Cmd>T devtools::load_all()<CR> |
|  |  rt | <Cmd>T devtools::test()<CR> |
|  |  ri | <Cmd>T devtools::install(keep_source=TRUE)<CR> |
|  |  rC | <Cmd>T devtools::test_coverage()<CR> |
|  |  rT | <Cmd>T testthat::test_file("%")<CR> |
|  |  rc | <Cmd>T devtools::check()<CR> |
|  |  mr | <Cmd>lua MiniMap.refresh()<CR> |
|  |  mf | <Cmd>lua MiniMap.toggle_focus()<CR> |
|  |  mo | <Cmd>lua MiniMap.open()<CR> |
|  |  ms | <Cmd>lua MiniMap.toggle_side()<CR> |
|  |  mt | <Cmd>lua MiniMap.toggle()<CR> |
|  |  mc | <Cmd>lua MiniMap.close()<CR> |
|  |  lr | <Cmd>lua vim.lsp.buf.rename()<CR> |
|  |  lj | <Cmd>lua vim.diagnostic.goto_next()<CR> |
|  |  ld | <Cmd>lua vim.diagnostic.open_float()<CR> |
|  |  ls | <Cmd>lua vim.lsp.buf.definition()<CR> |
|  |  li | <Cmd>lua vim.lsp.buf.hover()<CR> |
|  |  lR | <Cmd>lua vim.lsp.buf.references()<CR> |
|  |  lk | <Cmd>lua vim.diagnostic.goto_prev()<CR> |
|  |  la | <Cmd>lua vim.lsp.buf.signature_help()<CR> |
|  |  lf | <Cmd>lua vim.lsp.buf.format({ async = true })<CR> |
|  |  Lx | <Cmd>lua EC.execute_lua_line()<CR> |
|  |  Lf | <Cmd>luafile %<CR> |
|  |  s | <Cmd>TREPLSendLine<CR>j |
|  |  em | <Cmd>lua MiniFiles.open('~/.config/nvim-Mini/pack/plugins/opt/mini')<CR> |
|  |  ef | <Cmd>lua MiniFiles.open(vim.api.nvim_buf_get_name(0))<CR> |
|  |  eq | <Cmd>lua EC.toggle_quickfix()<CR> |
|  |  ed | <Cmd>lua MiniFiles.open()<CR> |
|  |  ta | <Cmd>lua MiniTest.run()<CR> |
|  |  tl | <Cmd>lua MiniTest.run_at_location()<CR> |
|  |  tT | <Cmd>belowright Tnew<CR> |
|  |  ts | <Cmd>lua EC.minitest_screenshots.browse()<CR> |
|  |  tt | <Cmd>vertical Tnew<CR> |
|  |  tf | <Cmd>lua MiniTest.run_file()<CR> |
|  |  or | <Cmd>lua MiniMisc.resize_window()<CR> |
|  |  os | <Cmd>lua MiniSessions.select()<CR> |
|  |  ol | <Cmd>lua EC.move_arg('right')<CR> |
|  |  ot | <Cmd>lua MiniTrailspace.trim()<CR> |
|  |  oH | <Cmd>TSBufToggle highlight<CR> |
|  |  oS | <Cmd>lua EC.insert_section()<CR> |
|  |  oh | <Cmd>lua EC.move_arg('left')<CR> |
|  |  oT | <Cmd>lua vim.b.minitrailspace_disable = not vim.b.minitrailspace_disable<CR> |
|  |  oC | <Cmd>lua MiniCursorword.toggle()<CR> |
|  |  oz | <Cmd>lua MiniMisc.zoom()<CR> |
|  |  og | <Cmd>lua MiniDoc.generate()<CR> |
|  |  od | <Cmd>Neogen<CR> |
|  |  Tn | <Cmd>TestNearest<CR> |
|  |  Tf | <Cmd>TestFile<CR> |
|  |  Tl | <Cmd>TestLast<CR> |
|  |  TL | <Cmd>TestLast -strategy=make | copen<CR> |
|  |  Ts | <Cmd>TestSuite<CR> |
|  |  TS | <Cmd>TestSuite -strategy=make | copen<CR> |
|  |  TN | <Cmd>TestNearest -strategy=make | copen<CR> |
|  |  TF | <Cmd>TestFile -strategy=make | copen<CR> |
|  |  gA | <Cmd>lua require("gitsigns").stage_buffer()<CR> |
|  |  gx | <Cmd>lua require("gitsigns").reset_hunk()<CR> |
|  |  gu | <Cmd>lua require("gitsigns").undo_stage_hunk()<CR> |
|  |  gq | <Cmd>lua require("gitsigns").setqflist()<CR>:copen<CR> |
|  |  gX | <Cmd>lua require("gitsigns").reset_buffer()<CR> |
|  |  gp | <Cmd>lua require("gitsigns").preview_hunk()<CR> |
|  |  gg | <Cmd>lua EC.open_lazygit()<CR> |
|  |  ga | <Cmd>lua require("gitsigns").stage_hunk()<CR> |
|  |  gb | <Cmd>lua require("gitsigns").blame_line()<CR> |
|  |  ba | <Cmd>b#<CR> |
|  |  bD | <Cmd>lua MiniBufremove.delete(0, true)<CR> |
|  |  bw | <Cmd>lua MiniBufremove.wipeout()<CR> |
|  |  bW | <Cmd>lua MiniBufremove.wipeout(0, true)<CR> |
|  |  bs | <Cmd>lua EC.new_scratch_buffer()<CR> |
|  |  bd | <Cmd>lua MiniBufremove.delete()<CR> |
|  |  fn | <Cmd>TodoTelescope<CR> |
|  |  fD | <Cmd>Telescope diagnostics bufnr=0<CR> |
|  |  ff | <Cmd>lua EC.telescope_project_files()<CR> |
|  |  f: | <Cmd>Telescope command_history<CR> |
|  |  fB | <Cmd>Telescope current_buffer_fuzzy_find<CR> |
|  |  fO | <Cmd>Telescope vim_options<CR> |
|  |  fo | <Cmd>Telescope oldfiles<CR> |
|  |  fR | <Cmd>Telescope lsp_references<CR> |
|  |  fh | <Cmd>Telescope help_tags<CR> |
|  |  fs | <Cmd>Telescope spell_suggest<CR> |
|  |  ft | <Cmd>Telescope file_browser<CR> |
|  |  fb | <Cmd>Telescope buffers<CR> |
|  |  fc | <Cmd>Telescope git_commits<CR> |
|  |  fr | <Cmd>Telescope resume<CR> |
|  |  fj | <Cmd>Telescope jumplist<CR> |
|  |  fH | <Cmd>Telescope highlights<CR> |
|  |  fS | <Cmd>Telescope treesitter<CR> |
|  |  f/ | <Cmd>Telescope search_history<CR> |
|  |  fC | <Cmd>Telescope git_bcommits<CR> |
|  |  fg | <Cmd>Telescope live_grep<CR> |
|  |  fd | <Cmd>Telescope diagnostics<CR> |
|  | % | <Plug>(MatchitNormalForward) |
| Nvim builtin | & | :&&<CR> |
| Execute macro without 'mini.clue' triggers | @ |  |
| Execute macro without 'mini.clue' triggers | Q |  |
| Nvim builtin | Y | y$ |
|  | [% | <Plug>(MatchitNormalMultiBackward) |
| Paste Above | [p | <Cmd>exe "put! " . v:register<CR> |
|  | \h |  |
|  | ]% | <Plug>(MatchitNormalMultiForward) |
| Paste Below | ]p | <Cmd>exe "put "  . v:register<CR> |
|  | gx | <Plug>NetrwBrowseX |
|  | g% | <Plug>(MatchitNormalBackward) |
|  | s |  |
|  | <Plug>NetrwBrowseX | :call netrw#BrowseX(netrw#GX(),netrw#CheckIfRemote(netrw#GX()))<CR> |
|  | <Plug>(MatchitNormalMultiForward) | :<C-U>call matchit#MultiMatch("W",  "n")<CR> |
|  | <Plug>(MatchitNormalMultiBackward) | :<C-U>call matchit#MultiMatch("bW", "n")<CR> |
|  | <Plug>(MatchitNormalBackward) | :<C-U>call matchit#Match_wrapper('',0,'n')<CR> |
|  | <Plug>(MatchitNormalForward) | :<C-U>call matchit#Match_wrapper('',1,'n')<CR> |
|  | <Plug>PlenaryTestFile | :lua require('plenary.test_harness').test_directory(vim.fn.expand("%:p"))<CR> |
| Nvim builtin | <C-L> | <Cmd>nohlsearch|diffupdate|normal! <C-L><CR> |

#### visual mode keymaps

| Description | LHS | RHS |
| ----------- | --- | --- |
|  |  lf | :lua vim.lsp.buf.range_formatting()<CR> |
|  |  s | mode() ==# "v" ? ":TREPLSendSelection<CR>`>l" : ":TREPLSendSelection<CR>'>j" |
|  |  rx | "+y :T reprex::reprex()<CR> |
| Nvim builtin | # | y?\V<C-R>"<CR> |
|  | % | <Plug>(MatchitVisualForward) |
| Nvim builtin | * | y/\V<C-R>"<CR> |
|  | [% | <Plug>(MatchitVisualMultiBackward) |
| Paste Above | [p | <Cmd>exe "put! " . v:register<CR> |
|  | ]% | <Plug>(MatchitVisualMultiForward) |
| Paste Below | ]p | <Cmd>exe "put "  . v:register<CR> |
|  | a% | <Plug>(MatchitVisualTextObject) |
|  | gx | <Plug>NetrwBrowseXVis |
|  | g% | <Plug>(MatchitVisualBackward) |
|  | s |  |
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

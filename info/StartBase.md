---
layout: post
title: StartBase Configuration Info
toc: true
post_style: page
---

## StartBase Neovim Configuration Information

Small configuration that includes a plugin manager

- Install and initialize: **`lazyman -x StartBase`**
- Configuration category: [Starter](https://lazyman.dev/configurations/#starter-configurations)
- Base configuration:     Custom
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim)
- Installation location:  **`~/.config/nvim-StartBase`**

### Git repository

[https://github.com/VonHeikemen/nvim-starter/tree/01-base](https://github.com/VonHeikemen/nvim-starter/tree/01-base)

### Lazy managed plugins

- [folke/lazy.nvim](https://github.com/folke/lazy.nvim)
- [nvim-lualine/lualine.nvim](https://github.com/nvim-lualine/lualine.nvim)
- [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons)
- [folke/tokyonight.nvim](https://github.com/folke/tokyonight.nvim)

### StartBase Keymaps

#### normal mode keymaps

|  LHS  |  RHS  | Description |
| ----- | ----- | ----------- |
| <code> bl</code> | <code>&lt;Cmd&gt;buffer #&lt;CR&gt;</code> |
 | | <code> bq</code> | <code>&lt;Cmd&gt;bdelete&lt;CR&gt;</code> |
 | | <code> w</code> | <code>&lt;Cmd&gt;write&lt;CR&gt;</code> |
 | | <code> a</code> | <code>:keepjumps normal! ggVG&lt;CR&gt;</code> |
 | | <code> l</code> | <code>g_</code> |
 | | <code> h</code> | <code>^</code> |
 | | <code>%</code> | <code>&lt;Plug&gt;(MatchitNormalForward)</code> |
 | | <code>&</code> | <code>:&&&lt;CR&gt;</code> |
 | Nvim builtin| <code>Y</code> | <code>y$</code> |
 | Nvim builtin| <code>[%</code> | <code>&lt;Plug&gt;(MatchitNormalMultiBackward)</code> |
 | | <code>]%</code> | <code>&lt;Plug&gt;(MatchitNormalMultiForward)</code> |
 | | <code>gx</code> | <code>&lt;Plug&gt;NetrwBrowseX</code> |
 | | <code>g%</code> | <code>&lt;Plug&gt;(MatchitNormalBackward)</code> |
 | | <code>gp</code> | <code>"+p</code> |
 | | <code>gy</code> | <code>"+y</code> |
 | | <code>x</code> | <code>"_x</code> |
 | | <code>&lt;Plug&gt;NetrwBrowseX</code> | <code>:call netrw#BrowseX(netrw#GX(),netrw#CheckIfRemote(netrw#GX()))&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalMultiForward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalMultiBackward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalBackward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'n')&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitNormalForward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'n')&lt;CR&gt;</code> |
 | | <code>&lt;C-L&gt;</code> | <code>&lt;Cmd&gt;nohlsearch&#124;diffupdate|normal! &lt;C-L&gt;&lt;CR&gt;</code> |
 | Nvim builtin
#### visual mode keymaps

|  LHS  |  RHS  | Description |
| ----- | ----- | ----------- |
| <code> l</code> | <code>g_</code> |
 | | <code> h</code> | <code>^</code> |
 | | <code>#</code> | <code>y?\V&lt;C-R&gt;"&lt;CR&gt;</code> |
 | Nvim builtin| <code>%</code> | <code>&lt;Plug&gt;(MatchitVisualForward)</code> |
 | | <code>*</code> | <code>y/\V&lt;C-R&gt;"&lt;CR&gt;</code> |
 | Nvim builtin| <code>[%</code> | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)</code> |
 | | <code>]%</code> | <code>&lt;Plug&gt;(MatchitVisualMultiForward)</code> |
 | | <code>a%</code> | <code>&lt;Plug&gt;(MatchitVisualTextObject)</code> |
 | | <code>gx</code> | <code>&lt;Plug&gt;NetrwBrowseXVis</code> |
 | | <code>g%</code> | <code>&lt;Plug&gt;(MatchitVisualBackward)</code> |
 | | <code>gp</code> | <code>"+p</code> |
 | | <code>gy</code> | <code>"+y</code> |
 | | <code>x</code> | <code>"_x</code> |
 | | <code>&lt;Plug&gt;NetrwBrowseXVis</code> | <code>:&lt;C-U&gt;call netrw#BrowseXVis()&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualTextObject)</code> | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)o&lt;Plug&gt;(MatchitVisualMultiForward)</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualMultiForward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualBackward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'v')&lt;CR&gt;m'gv``</code> |
 | | <code>&lt;Plug&gt;(MatchitVisualForward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'v')&lt;CR&gt;:if col("''") != col("$") &#124; exe ":normal! m'" | endif&lt;CR&gt;gv``</code> |
 | 
#### operator mode keymaps

|  LHS  |  RHS  | Description |
| ----- | ----- | ----------- |
| <code> l</code> | <code>g_</code> |
 | | <code> h</code> | <code>^</code> |
 | | <code>%</code> | <code>&lt;Plug&gt;(MatchitOperationForward)</code> |
 | | <code>[%</code> | <code>&lt;Plug&gt;(MatchitOperationMultiBackward)</code> |
 | | <code>]%</code> | <code>&lt;Plug&gt;(MatchitOperationMultiForward)</code> |
 | | <code>g%</code> | <code>&lt;Plug&gt;(MatchitOperationBackward)</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationMultiForward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "o")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationMultiBackward)</code> | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "o")&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationBackward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'o')&lt;CR&gt;</code> |
 | | <code>&lt;Plug&gt;(MatchitOperationForward)</code> | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'o')&lt;CR&gt;</code> |
 | 

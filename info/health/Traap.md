---
layout: post
title: Traap Configuration Health Check
toc: true
post_style: page
---

# nvim-Traap Neovim health check

--------
clipboard-image: require("clipboard-image.health").check()

- ERROR Failed to run healthcheck for "clipboard-image" plugin. Exception:
  command line..function health#check, line 25
  Vim(eval):E5108: Error executing lua ...lazy/clipboard-image.nvim/lua/clipboard-image/health.lua:3: module 'health' not found:
  no field package.preload['health']
  cache_loader: module health not found
  cache_loader_lib: module health not found
  no file './health.lua'
  no file '/__w/neovim/neovim/.deps/usr/share/luajit-2.1.0-beta3/health.lua'
  no file '/usr/local/share/lua/5.1/health.lua'
  no file '/usr/local/share/lua/5.1/health/init.lua'
  no file '/__w/neovim/neovim/.deps/usr/share/lua/5.1/health.lua'
  no file '/__w/neovim/neovim/.deps/usr/share/lua/5.1/health/init.lua'
  no file './health.so'
  no file '/usr/local/lib/lua/5.1/health.so'
  no file '/__w/neovim/neovim/.deps/usr/lib/lua/5.1/health.so'
  no file '/usr/local/lib/lua/5.1/loadall.so'
  stack traceback:
  [C]: in function 'require'
  ...lazy/clipboard-image.nvim/lua/clipboard-image/health.lua:3: in main chunk
  [C]: in function 'require'
  [string "luaeval()"]:1: in main chunk

--------
lazy: require("lazy.health").check()

lazy.nvim ~
- OK Git installed
- OK no existing packages found by other package managers
- OK packer_compiled.lua not found
- WARNING {nvim-dap-ui}: overriding <config>
- WARNING {flash.nvim}: unknown key <vscode>
- ERROR Issues were reported when loading your specs:
- ERROR Failed to load `plugins.wiki-vim`
- ERROR
- ERROR /home/ronnie/.config/nvim-Traap/lua/plugins/wiki-vim.lua:16: attempt to concatenate a nil value
- ERROR
- ERROR # stacktrace:
- ERROR   - ~/.config/nvim-Traap/lua/plugins/wiki-vim.lua:16
- ERROR   - ~/.config/nvim-Traap/lua/config/lazy.lua:3
- ERROR   - ~/.config/nvim-Traap/init.lua:7

--------
lazyvim: require("lazyvim.health").check()

LazyVim ~
- OK Using Neovim >= 0.8.0
- OK `git` is installed
- OK `rg` is installed
- OK `fd` is installed
- OK `lazygit` is installed

--------
mason: require("mason.health").check()

- ERROR Failed to run healthcheck for "mason" plugin. Exception:
  command line..function health#check, line 25
  Vim(eval):Error executing vim.schedule lua callback: ...are/nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns/async.lua:76: The coroutine failed with this message: ...hare/nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns/util.lua:45: Vim:Failed to load `plugins.wiki-vim`
  stack traceback:
  [C]: in function '__index'
  ...hare/nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns/util.lua:45: in function 'buf_lines'
  ...e/nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns/manager.lua:416: in function 'fn'
  .../nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns/debounce.lua:76: in function 'update'
  ...re/nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns/attach.lua:365: in function 'fn'
  .../nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns/debounce.lua:76: in function 'attach_throttled'
  ...re/nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns/attach.lua:426: in function 'attach'
  ...cal/share/nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns.lua:125: in function 'setup_attach'
  ...cal/share/nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns.lua:183: in function <...cal/share/nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns.lua:159>
  stack traceback:
  [C]: in function 'error'
  ...are/nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns/async.lua:76: in function 'cb'
  ...are/nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns/async.lua:113: in function 'cb'
  ...are/nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns/async.lua:186: in function <...are/nvim-Traap/lazy/gitsigns.nvim/lua/gitsigns/async.lua:184>
  [C]: in function 'wait'
  ...nvim-Traap/lazy/mason.nvim/lua/mason-core/async/init.lua:127: in function 'run_blocking'
  ...al/share/nvim-Traap/lazy/mason.nvim/lua/mason/health.lua:332: in function 'check'
  [string "luaeval()"]:1: in main chunk

--------
neoconf: require("neoconf.health").check()

neoconf.nvim ~
- OK **treesitter-nvim** is installed
- OK **TreeSitter jsonc** parser is installed
- OK **neodev.nvim** is installed
- OK **lspconfig** is installed
- WARNING **lspconfig jsonls** is not installed? You won't get any auto completion in your settings files
- WARNING **lspconfig lua_ls** is not installed? You won't get any auto completion in your lua settings files

--------
null-ls: require("null-ls.health").check()

- ERROR fish_indent: the command "fish_indent" is not executable.
- ERROR fish: the command "fish" is not executable.
- OK stylua: the command "stylua" is executable.
- ERROR shfmt: the command "shfmt" is not executable.
- OK gomodifytags: the source "gomodifytags" can be ran.
- OK impl: the source "impl" can be ran.
- OK gofumpt: the command "gofumpt" is executable.
- ERROR goimports_reviser: the command "goimports-reviser" is not executable.
- typescript: cannot verify if the command is an executable.

--------
nvim: require("nvim.health").check()

Configuration ~
- OK no issues found

Runtime ~
- OK $VIMRUNTIME: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/share/nvim/runtime

Performance ~
- OK Build type: Release

Remote Plugins ~
- OK Up to date

terminal ~
- key_backspace (kbs) terminfo entry: `key_backspace=\177`
- key_dc (kdch1) terminfo entry: `key_dc=\E[3~`
- $SSH_TTY="/dev/pts/4"

--------
nvim-treesitter: require("nvim-treesitter.health").check()

Installation ~
- OK `tree-sitter` found 0.20.8 (d4c1bf7ce78051b7f4a381d1508d68928512ed5f) (parser generator, only needed for :TSInstallFromGrammar)
- OK `node` found v18.16.0 (only needed for :TSInstallFromGrammar)
- OK `git` executable found.
- OK `cc` executable found. Selected from { vim.NIL, "cc", "gcc", "clang", "cl", "zig" }
  Version: cc (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0
- OK Neovim was compiled with tree-sitter runtime ABI version 14 (required >=13). Parsers must be compatible with runtime ABI.

OS Info:
{
  machine = "x86_64",
  release = "6.2.0-26-generic",
  sysname = "Linux",
  version = "#26~22.04.1-Ubuntu SMP PREEMPT_DYNAMIC Thu Jul 13 16:27:29 UTC 2"
} ~

Parser/Features         H L F I J
  - c                   ✓ ✓ ✓ ✓ ✓
  - gosum               ✓ . . . .
  - gowork              ✓ . . . ✓
  - html                ✓ ✓ ✓ ✓ ✓
  - json                ✓ ✓ ✓ ✓ .
  - json5               ✓ . . . ✓
  - jsonc               ✓ ✓ ✓ ✓ ✓
  - lua                 ✓ ✓ ✓ ✓ ✓
  - luadoc              ✓ . . . .
  - luap                ✓ . . . .
  - markdown            ✓ . ✓ ✓ ✓
  - markdown_inline     ✓ . . . ✓
  - ninja               ✓ . ✓ ✓ .
  - python              ✓ ✓ ✓ ✓ ✓
  - query               ✓ ✓ ✓ ✓ ✓
  - regex               ✓ . . . .
  - ron                 ✓ ✓ ✓ ✓ ✓
  - rst                 ✓ ✓ . . ✓
  - rust                ✓ ✓ ✓ ✓ ✓
  - toml                ✓ ✓ ✓ ✓ ✓
  - tsx                 ✓ ✓ ✓ ✓ ✓
  - typescript          ✓ ✓ ✓ ✓ ✓
  - vim                 ✓ ✓ ✓ . ✓
  - vimdoc              ✓ . . . ✓
  - yaml                ✓ ✓ ✓ ✓ ✓

  Legend: H[ighlight], L[ocals], F[olds], I[ndents], In[j]ections
         +) multiple parsers found, only one will be used
         x) errors found in the query, try to run :TSUpdate {lang} ~

--------
provider: health#provider#check

Clipboard (optional) ~
- OK Clipboard tool found: lemonade

Python 3 provider (optional) ~
- `g:python3_host_prog` is not set.  Searching for python3 in the environment.
- Multiple python3 executables found.  Set `g:python3_host_prog` to avoid surprises.
- Executable: /usr/bin/python3
- Other python executable: /bin/python3
- Python version: 3.10.12
- pynvim version: 0.4.3
- OK Latest pynvim is installed.

Python virtualenv ~
- OK no $VIRTUAL_ENV

Ruby provider (optional) ~
- Ruby: ruby 3.0.2p107 (2021-07-07 revision 0db68f0233) [x86_64-linux-gnu]
- WARNING `neovim-ruby-host` not found.
  - ADVICE:
    - Run `gem install neovim` to ensure the neovim RubyGem is installed.
    - Run `gem environment` to ensure the gem bin directory is in $PATH.
    - If you are using rvm/rbenv/chruby, try "rehashing".
    - See :help |g:ruby_host_prog| for non-standard gem installations.
    - You may disable this provider (and warning) by adding `let g:loaded_ruby_provider = 0` to your init.vim

Node.js provider (optional) ~
- Node.js: v18.16.0
- Nvim node.js host: /home/ronnie/.local/lib/node_modules/neovim/bin/cli.js
- OK Latest "neovim" npm/yarn/pnpm package is installed: 4.10.1

Perl provider (optional) ~
- WARNING "Neovim::Ext" cpan module is not installed
  - ADVICE:
    - See :help |provider-perl| for more information.
    - You may disable this provider (and warning) by adding `let g:loaded_perl_provider = 0` to your init.vim

--------
vim.lsp: require("vim.lsp.health").check()

- LSP log level : WARN
- Log path: /home/ronnie/.local/state/nvim-Traap/lsp.log
- Log size: 0 KB

vim.lsp: Active Clients ~
- No active clients

--------
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: c          ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/c.so
- OK Parser: gosum      ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/gosum.so
- OK Parser: gowork     ABI: 13, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/gowork.so
- OK Parser: html       ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/html.so
- OK Parser: json       ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/json.so
- OK Parser: json5      ABI: 13, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/json5.so
- OK Parser: jsonc      ABI: 13, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/jsonc.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/lua.so
- OK Parser: luadoc     ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/luadoc.so
- OK Parser: luap       ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/luap.so
- OK Parser: markdown   ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/markdown.so
- OK Parser: markdown_inline ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/markdown_inline.so
- OK Parser: ninja      ABI: 13, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/ninja.so
- OK Parser: python     ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/python.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/query.so
- OK Parser: regex      ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/regex.so
- OK Parser: ron        ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/ron.so
- OK Parser: rst        ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/rst.so
- OK Parser: rust       ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/rust.so
- OK Parser: toml       ABI: 13, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/toml.so
- OK Parser: tsx        ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/tsx.so
- OK Parser: typescript ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/typescript.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/vimdoc.so
- OK Parser: yaml       ABI: 13, path: /home/ronnie/.local/share/nvim-Traap/lazy/nvim-treesitter/parser/yaml.so
- OK Parser: c          ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/c.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/query.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vimdoc.so


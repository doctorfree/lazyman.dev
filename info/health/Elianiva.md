---
layout: post
title: Lazyman Configuration Health Check
toc: true
post_style: page
---

# nvim-Elianiva Neovim health check

==============================================================================
lazy: require("lazy.health").check()

lazy.nvim ~
- OK Git installed
- OK no existing packages found by other package managers
- OK packer_compiled.lua not found

==============================================================================
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

==============================================================================
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
  - c                   x ✓ x x ✓
  - comment             x . . . .
  - cpp                 x x x x ✓
  - css                 ✓ . ✓ ✓ ✓
  - glimmer             ✓ ✓ ✓ ✓ .
  - go                  ✓ ✓ ✓ ✓ ✓
  - html                ✓ ✓ ✓ ✓ ✓
  - java                x ✓ ✓ ✓ ✓
  - javascript          x ✓ ✓ x ✓
  - jsdoc               ✓ . . . .
  - json                ✓ ✓ ✓ ✓ .
  - jsonc               ✓ ✓ ✓ ✓ ✓
  - lua                 x ✓ ✓ ✓ x
  - markdown            ✓ . ✓ ✓ ✓
  - python              x ✓ ✓ ✓ ✓
  - query               ✓ ✓ ✓ ✓ ✓
  - rst                 ✓ ✓ . . ✓
  - rust                ✓ ✓ ✓ ✓ ✓
  - svelte              ✓ . ✓ ✓ ✓
  - tsx                 x ✓ ✓ x ✓
  - typescript          ✓ ✓ ✓ ✓ ✓
  - vim                 ✓ ✓ ✓ . ✓
  - vimdoc              ✓ . . . ✓
  - yaml                ✓ ✓ ✓ ✓ ✓

  Legend: H[ighlight], L[ocals], F[olds], I[ndents], In[j]ections
         +) multiple parsers found, only one will be used
         x) errors found in the query, try to run :TSUpdate {lang} ~

The following errors have been detected: ~
- ERROR c(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 242 for language c
  c(highlights) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/c/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 242 for language c
- ERROR c(folds): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 249 for language c
  c(folds) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/c/folds.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 249 for language c
- ERROR c(indents): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1109 for language c
  c(indents) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/c/indents.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1109 for language c
- ERROR comment(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1185 for language comment
  comment(highlights) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/comment/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1185 for language comment
- ERROR cpp(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 242 for language cpp
  cpp(highlights) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/c/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 242 for language cpp
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/cpp/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 3916 for language cpp
- ERROR cpp(locals): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 2426 for language cpp
  cpp(locals) is concatenated from the following files:
  |    [OK]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/c/locals.scm"
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/cpp/locals.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1046 for language cpp
- ERROR cpp(folds): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 249 for language cpp
  cpp(folds) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/c/folds.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 249 for language cpp
  |    [OK]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/cpp/folds.scm"
- ERROR cpp(indents): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1109 for language cpp
  cpp(indents) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/c/indents.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1109 for language cpp
  |    [OK]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/cpp/indents.scm"
- ERROR java(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 3484 for language java
  java(highlights) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/java/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 3484 for language java
- ERROR javascript(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 6135 for language javascript
  javascript(highlights) is concatenated from the following files:
  |    [OK]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/ecma/highlights.scm"
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/jsx/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 122 for language javascript
  |    [OK]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/javascript/highlights.scm"
- ERROR javascript(indents): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1309 for language javascript
  javascript(indents) is concatenated from the following files:
  |    [OK]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/ecma/indents.scm"
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/jsx/indents.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 150 for language javascript
  |    [OK]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/javascript/indents.scm"
- ERROR lua(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 3624 for language lua
  lua(highlights) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/lua/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 3624 for language lua
- ERROR lua(injections): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1682 for language lua
  lua(injections) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/lua/injections.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1682 for language lua
- ERROR python(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 727 for language python
  python(highlights) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/python/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 727 for language python
- ERROR tsx(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 9142 for language tsx
  tsx(highlights) is concatenated from the following files:
  |    [OK]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/ecma/highlights.scm"
  |    [OK]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/typescript/highlights.scm"
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/jsx/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 122 for language tsx
  |    [OK]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/tsx/highlights.scm"
- ERROR tsx(indents): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1408 for language tsx
  tsx(indents) is concatenated from the following files:
  |    [OK]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/ecma/indents.scm"
  |    [OK]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/typescript/indents.scm"
  | [ERROR]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/jsx/indents.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 150 for language tsx
  |    [OK]:"/home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/queries/tsx/indents.scm"

==============================================================================
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

==============================================================================
vim.lsp: require("vim.lsp.health").check()

- LSP log level : WARN
- Log path: /home/ronnie/.local/state/nvim-Elianiva/lsp.log
- Log size: 0 KB

vim.lsp: Active Clients ~
- No active clients

==============================================================================
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: c          ABI: 13, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/c.so
- OK Parser: comment    ABI: 13, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/comment.so
- OK Parser: cpp        ABI: 14, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/cpp.so
- OK Parser: css        ABI: 13, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/css.so
- OK Parser: glimmer    ABI: 13, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/glimmer.so
- OK Parser: go         ABI: 14, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/go.so
- OK Parser: html       ABI: 13, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/html.so
- OK Parser: java       ABI: 14, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/java.so
- OK Parser: javascript ABI: 14, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/javascript.so
- OK Parser: jsdoc      ABI: 13, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/jsdoc.so
- OK Parser: json       ABI: 13, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/json.so
- OK Parser: jsonc      ABI: 13, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/jsonc.so
- OK Parser: lua        ABI: 13, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/lua.so
- OK Parser: markdown   ABI: 13, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/markdown.so
- OK Parser: python     ABI: 14, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/python.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/query.so
- OK Parser: rst        ABI: 13, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/rst.so
- OK Parser: rust       ABI: 14, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/rust.so
- OK Parser: svelte     ABI: 13, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/svelte.so
- OK Parser: tsx        ABI: 14, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/tsx.so
- OK Parser: typescript ABI: 14, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/typescript.so
- OK Parser: yaml       ABI: 13, path: /home/ronnie/.local/share/nvim-Elianiva/lazy/nvim-treesitter/parser/yaml.so
- OK Parser: c          ABI: 13, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/c.so
- OK Parser: lua        ABI: 13, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/query.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vimdoc.so


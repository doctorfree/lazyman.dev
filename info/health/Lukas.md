---
layout: post
title: Lukas Configuration Health Check
toc: true
post_style: page
---

# nvim-Lukas Neovim health check

--------
crates: require("crates.health").check()

Checking required plugins ~
- OK plenary.nvim installed
- WARNING null-ls.nvim not found

Checking external dependencies ~
- OK curl installed
- OK xdg-open installed
- OK open installed

--------
diffview: require("diffview.health").check()

Checking plugin dependencies ~
- OK nvim-web-devicons installed.

Checking VCS tools ~
- The plugin requires at least one of the supported VCS tools to be valid.
- OK Git found.
- OK Git is up-to-date. (2.34.1)
- WARNING Configured `hg_cmd` is not executable: 'hg'

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
  - bash                ✓ ✓ ✓ . ✓
  - c                   x ✓ x x ✓
  - cpp                 ✓ ✓ ✓ ✓ ✓
  - go                  ✓ ✓ ✓ ✓ ✓
  - graphql             ✓ . . ✓ ✓
  - html                ✓ ✓ ✓ ✓ ✓
  - java                ✓ ✓ ✓ ✓ ✓
  - javascript          ✓ ✓ ✓ ✓ ✓
  - json                ✓ ✓ ✓ ✓ .
  - lua                 ✓ ✓ ✓ ✓ ✓
  - markdown            ✓ . ✓ ✓ ✓
  - markdown_inline     ✓ . . . ✓
  - php                 ✓ ✓ ✓ ✓ ✓
  - python              ✓ ✓ ✓ ✓ ✓
  - query               ✓ ✓ ✓ ✓ ✓
  - regex               ✓ . . . .
  - rust                ✓ ✓ ✓ ✓ ✓
  - scss                ✓ . ✓ ✓ .
  - toml                ✓ ✓ ✓ ✓ ✓
  - tsx                 ✓ ✓ ✓ ✓ ✓
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
  | [ERROR]:"/home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/queries/c/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 242 for language c
- ERROR c(folds): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 249 for language c
  c(folds) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/queries/c/folds.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 249 for language c
- ERROR c(indents): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1109 for language c
  c(indents) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/queries/c/indents.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1109 for language c

--------
provider: health#provider#check

Clipboard (optional) ~
- OK Clipboard tool found: lemonade

Python 3 provider (optional) ~
- Using: g:python3_host_prog = "/usr/bin/python3"
- Executable: /usr/bin/python3
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
targets: health#targets#check

- WARNING Conflicting mapping found:
  ab → <Plug>(textobj-sandwich-auto-a)
  b → {'pair': [{'c': ')', 'o': '('}, {'c': ']', 'o': '['}, {'c': '}', 'o': '{'}]}
- WARNING Conflicting mapping found:
  ib → <Plug>(textobj-sandwich-auto-i)
  b → {'pair': [{'c': ')', 'o': '('}, {'c': ']', 'o': '['}, {'c': '}', 'o': '{'}]}

--------
telescope: require("telescope.health").check()

Checking for required plugins ~
- OK plenary installed.
- OK nvim-treesitter installed.

Checking external dependencies ~
- OK rg: found ripgrep 13.0.0
- OK fd: found fd 8.7.0

--------

--------
vim.lsp: require("vim.lsp.health").check()

- LSP log level : WARN
- Log path: /home/ronnie/.local/state/nvim-Lukas/lsp.log
- Log size: 0 KB

vim.lsp: Active Clients ~
- No active clients

--------
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: bash       ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/bash.so
- OK Parser: cpp        ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/cpp.so
- OK Parser: go         ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/go.so
- OK Parser: graphql    ABI: 13, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/graphql.so
- OK Parser: html       ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/html.so
- OK Parser: java       ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/java.so
- OK Parser: javascript ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/javascript.so
- OK Parser: json       ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/json.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/lua.so
- OK Parser: markdown   ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/markdown.so
- OK Parser: markdown_inline ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/markdown_inline.so
- OK Parser: php        ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/php.so
- OK Parser: python     ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/python.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/query.so
- OK Parser: regex      ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/regex.so
- OK Parser: rust       ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/rust.so
- OK Parser: scss       ABI: 13, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/scss.so
- OK Parser: toml       ABI: 13, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/toml.so
- OK Parser: tsx        ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/tsx.so
- OK Parser: typescript ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/typescript.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/vimdoc.so
- OK Parser: yaml       ABI: 13, path: /home/ronnie/.local/share/nvim-Lukas/site/pack/packer/start/nvim-treesitter/parser/yaml.so
- OK Parser: c          ABI: 13, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/c.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/query.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vimdoc.so


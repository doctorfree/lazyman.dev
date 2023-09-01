---
layout: post
title: Lazyman Configuration Health Check
toc: true
post_style: page
---

# nvim-J4de Neovim health check

==============================================================================
lazy: require("lazy.health").check()

lazy.nvim ~
- OK Git installed
- OK no existing packages found by other package managers
- OK packer_compiled.lua not found

==============================================================================
mason: require("mason.health").check()

mason.nvim ~
- OK mason.nvim version v1.7.0
- OK PATH: prepend
- OK Providers:
  mason.providers.registry-api
  mason.providers.client
- OK neovim version >= 0.7.0

mason.nvim [Registries] ~
- OK Registry `github.com/mason-org/mason-registry version: 2023-09-01-painless-letter` is installed.

mason.nvim [Core utils] ~
- OK unzip: `UnZip 6.00 of 20 April 2009, by Debian. Original by Info-ZIP.`
- OK wget: `GNU Wget 1.21.2 built on linux-gnu.`
- OK curl: `curl 7.81.0 (x86_64-pc-linux-gnu) libcurl/7.81.0 OpenSSL/3.0.2 zlib/1.2.11 brotli/1.0.9 zstd/1.4.8 libidn2/2.3.2 libpsl/0.21.0 (+libidn2/2.3.2) libssh/0.9.6/openssl/zlib nghttp2/1.43.0 librtmp/2.3 OpenLDAP/2.5.16`
- OK gzip: `gzip 1.10`
- OK tar: `tar (GNU tar) 1.34`
- OK bash: `GNU bash, version 5.1.16(1)-release (x86_64-pc-linux-gnu)`
- OK sh: `Ok`

mason.nvim [Languages] ~
- OK Go: `go version go1.20.3 linux/amd64`
- OK Ruby: `ruby 3.0.2p107 (2021-07-07 revision 0db68f0233) [x86_64-linux-gnu]`
- OK cargo: `cargo 1.72.0 (103a7ff2e 2023-08-15)`
- OK PHP: `PHP 8.1.2-1ubuntu2.14 (cli) (built: Aug 18 2023 11:41:11) (NTS)`
- OK node: `v18.16.0`
- OK Composer: `Composer 2.2.6 2022-02-04 17:00:38`
- OK luarocks: `/usr/bin/luarocks 3.8.0`
- WARNING julia: not available
  - ADVICE:
    - spawn: julia failed with exit code - and signal -. julia is not executable
- OK python: `Python 3.10.12`
- OK java: `openjdk version "11.0.20.1" 2023-08-24`
- OK RubyGem: `3.3.5`
- OK javac: `javac 11.0.20.1`
- OK npm: `9.5.1`
- OK pip: `pip 23.2.1 from /home/ronnie/.local/lib/python3.10/site-packages/pip (python 3.10)`
- OK python venv: `Ok`

mason.nvim [GitHub] ~
- OK GitHub API rate limit. Used: 20. Remaining: 4980. Limit: 5000. Reset: Fri 01 Sep 2023 12:37:11 PM PDT.

==============================================================================
null-ls: require("null-ls.health").check()

- OK stylua: the command "stylua" is executable.
- ERROR mdformat: the command "mdformat" is not executable.
- ERROR clang_format: the command "clang-format" is not executable.
- ERROR markdownlint: the command "markdownlint" is not executable.
- ERROR cpplint: the command "cpplint" is not executable.
- OK beautysh: the command "beautysh" is executable.

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
  - bash                ✓ ✓ ✓ . ✓
  - c                   x ✓ x x ✓
  - cpp                 ✓ ✓ ✓ ✓ ✓
  - diff                ✓ . . . .
  - git_config          ✓ . . . .
  - git_rebase          ✓ . . . ✓
  - gitcommit           ✓ . . . ✓
  - lua                 ✓ ✓ ✓ ✓ ✓
  - luadoc              ✓ . . . .
  - luap                ✓ . . . .
  - markdown            ✓ . ✓ ✓ ✓
  - markdown_inline     ✓ . . . ✓
  - query               ✓ ✓ ✓ ✓ ✓
  - regex               ✓ . . . .
  - toml                ✓ ✓ ✓ ✓ ✓
  - vim                 ✓ ✓ ✓ . ✓
  - vimdoc              ✓ . . . ✓

  Legend: H[ighlight], L[ocals], F[olds], I[ndents], In[j]ections
         +) multiple parsers found, only one will be used
         x) errors found in the query, try to run :TSUpdate {lang} ~

The following errors have been detected: ~
- ERROR c(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 242 for language c
  c(highlights) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/queries/c/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 242 for language c
- ERROR c(folds): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 249 for language c
  c(folds) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/queries/c/folds.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 249 for language c
- ERROR c(indents): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1109 for language c
  c(indents) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/queries/c/indents.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1109 for language c

==============================================================================
provider: health#provider#check

Clipboard (optional) ~
- OK Clipboard tool found: lemonade

Python 3 provider (optional) ~
- Disabled (g:loaded_python3_provider=0).

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
- Disabled (g:loaded_node_provider=0).

Perl provider (optional) ~
- Disabled (g:loaded_perl_provider=0).

==============================================================================
rainbow-delimiters: require("rainbow-delimiters.health").check()

- No custom configuration; see :help |rb-delimiters-setup| for information.

==============================================================================
vim.lsp: require("vim.lsp.health").check()

- LSP log level : WARN
- Log path: /home/ronnie/.local/state/nvim-J4de/lsp.log
- Log size: 0 KB

vim.lsp: Active Clients ~
- null-ls (id=1, root_dir=/home/ronnie/.config/nvim-Lazyman)

==============================================================================
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: bash       ABI: 14, path: /home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/parser/bash.so
- OK Parser: cpp        ABI: 14, path: /home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/parser/cpp.so
- OK Parser: diff       ABI: 14, path: /home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/parser/diff.so
- OK Parser: git_config ABI: 13, path: /home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/parser/git_config.so
- OK Parser: git_rebase ABI: 14, path: /home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/parser/git_rebase.so
- OK Parser: gitcommit  ABI: 14, path: /home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/parser/gitcommit.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/parser/lua.so
- OK Parser: luadoc     ABI: 14, path: /home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/parser/luadoc.so
- OK Parser: luap       ABI: 14, path: /home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/parser/luap.so
- OK Parser: markdown   ABI: 14, path: /home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/parser/markdown.so
- OK Parser: markdown_inline ABI: 14, path: /home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/parser/markdown_inline.so
- OK Parser: regex      ABI: 14, path: /home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/parser/regex.so
- OK Parser: toml       ABI: 13, path: /home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/parser/toml.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/nvim-J4de/lazy/nvim-treesitter/parser/vimdoc.so
- OK Parser: c          ABI: 13, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/c.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/query.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vimdoc.so


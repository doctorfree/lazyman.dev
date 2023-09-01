---
layout: post
title: Lazyman Configuration Health Check
toc: true
post_style: page
---

# nvim-Scratch Neovim health check

==============================================================================
gitsigns: require("gitsigns.health").check()

- OK git version 2.34.1

==============================================================================
lazy: require("lazy.health").check()

lazy.nvim ~
- OK Git installed
- OK no existing packages found by other package managers
- OK packer_compiled.lua not found
- WARNING {mini.nvim}: unknown key <comment>
- WARNING {mini.nvim}: unknown key <align>
- WARNING {mini.nvim}: unknown key <pairs>
- ERROR Issues were reported when loading your specs:
- WARNING {nvim-colorizer.lua}: setting a table to `Plugin.config` is deprecated. Please use `Plugin.opts` instead
- WARNING {mason-lspconfig.nvim}: setting a table to `Plugin.config` is deprecated. Please use `Plugin.opts` instead
- WARNING {lualine.nvim}: setting a table to `Plugin.config` is deprecated. Please use `Plugin.opts` instead
- WARNING {nvim-tree.lua}: setting a table to `Plugin.config` is deprecated. Please use `Plugin.opts` instead

==============================================================================
mason: require("mason.health").check()

mason.nvim report ~
- OK neovim version >= 0.7.0
- OK **Go**: `go version go1.20.3 linux/amd64`
- OK **cargo**: `cargo 1.72.0 (103a7ff2e 2023-08-15)`
- OK **luarocks**: `/usr/bin/luarocks 3.8.0`
- OK **Ruby**: `ruby 3.0.2p107 (2021-07-07 revision 0db68f0233) [x86_64-linux-gnu]`
- OK **RubyGem**: `3.3.5`
- OK **Composer**: `Composer 2.2.6 2022-02-04 17:00:38`
- OK **PHP**: `PHP 8.1.2-1ubuntu2.14 (cli) (built: Aug 18 2023 11:41:11) (NTS)`
- OK **npm**: `9.5.1`
- OK **node**: `v18.16.0`
- OK **python3**: `Python 3.10.12`
- OK **pip3**: `pip 23.2.1 from /home/ronnie/.local/lib/python3.10/site-packages/pip (python 3.10)`
- OK **javac**: `javac 11.0.20.1`
- OK **java**: `openjdk version "11.0.20.1" 2023-08-24`
- WARNING **julia**: not available
- OK **wget**: `GNU Wget 1.21.2 built on linux-gnu.`
- OK **curl**: `curl 7.81.0 (x86_64-pc-linux-gnu) libcurl/7.81.0 OpenSSL/3.0.2 zlib/1.2.11 brotli/1.0.9 zstd/1.4.8 libidn2/2.3.2 libpsl/0.21.0 (+libidn2/2.3.2) libssh/0.9.6/openssl/zlib nghttp2/1.43.0 librtmp/2.3 OpenLDAP/2.5.16`
- OK **gzip**: `gzip 1.10`
- OK **tar**: `tar (GNU tar) 1.34`
- WARNING **pwsh**: not available
- OK **bash**: `GNU bash, version 5.1.16(1)-release (x86_64-pc-linux-gnu)`
- OK **sh**: `Ok`
- OK GitHub API rate limit. Used: 21. Remaining: 4979. Limit: 5000. Reset: Fri 01 Sep 2023 12:37:11 PM PDT.

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
  - gitignore           ✓ . . . .
  - heex                ✓ ✓ ✓ ✓ ✓
  - javascript          ✓ ✓ ✓ ✓ ✓
  - toml                ✓ ✓ ✓ ✓ ✓
  - regex               ✓ . . . .
  - diff                ✓ . . . .
  - json                ✓ ✓ ✓ ✓ .
  - c                   ✓ ✓ ✓ ✓ ✓
  - help                ✓ . . . ✓
  - html                ✓ ✓ ✓ ✓ ✓
  - yaml                ✓ ✓ ✓ ✓ ✓
  - query               ✓ ✓ ✓ ✓ ✓
  - lua                 ✓ ✓ ✓ ✓ ✓
  - vim                 ✓ ✓ ✓ . ✓
  - bash                ✓ ✓ ✓ . ✓
  - css                 ✓ . ✓ ✓ ✓

  Legend: H[ighlight], L[ocals], F[olds], I[ndents], In[j]ections
         +) multiple parsers found, only one will be used
         x) errors found in the query, try to run :TSUpdate {lang} ~

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
- Log path: /home/ronnie/.local/state/nvim-Scratch/lsp.log
- Log size: 0 KB

vim.lsp: Active Clients ~
- No active clients

==============================================================================
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: bash       ABI: 14, path: /home/ronnie/.local/share/nvim-Scratch/lazy/nvim-treesitter/parser/bash.so
- OK Parser: css        ABI: 13, path: /home/ronnie/.local/share/nvim-Scratch/lazy/nvim-treesitter/parser/css.so
- OK Parser: diff       ABI: 14, path: /home/ronnie/.local/share/nvim-Scratch/lazy/nvim-treesitter/parser/diff.so
- OK Parser: gitignore  ABI: 14, path: /home/ronnie/.local/share/nvim-Scratch/lazy/nvim-treesitter/parser/gitignore.so
- OK Parser: heex       ABI: 14, path: /home/ronnie/.local/share/nvim-Scratch/lazy/nvim-treesitter/parser/heex.so
- OK Parser: help       ABI: 14, path: /home/ronnie/.local/share/nvim-Scratch/lazy/nvim-treesitter/parser/help.so
- OK Parser: html       ABI: 13, path: /home/ronnie/.local/share/nvim-Scratch/lazy/nvim-treesitter/parser/html.so
- OK Parser: javascript ABI: 14, path: /home/ronnie/.local/share/nvim-Scratch/lazy/nvim-treesitter/parser/javascript.so
- OK Parser: json       ABI: 13, path: /home/ronnie/.local/share/nvim-Scratch/lazy/nvim-treesitter/parser/json.so
- OK Parser: lua        ABI: 13, path: /home/ronnie/.local/share/nvim-Scratch/lazy/nvim-treesitter/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/nvim-Scratch/lazy/nvim-treesitter/parser/query.so
- OK Parser: regex      ABI: 13, path: /home/ronnie/.local/share/nvim-Scratch/lazy/nvim-treesitter/parser/regex.so
- OK Parser: toml       ABI: 13, path: /home/ronnie/.local/share/nvim-Scratch/lazy/nvim-treesitter/parser/toml.so
- OK Parser: yaml       ABI: 13, path: /home/ronnie/.local/share/nvim-Scratch/lazy/nvim-treesitter/parser/yaml.so
- OK Parser: c          ABI: 13, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/c.so
- OK Parser: lua        ABI: 13, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/query.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vimdoc.so

==============================================================================
which_key: health#which_key#check

WhichKey: checking conflicting keymaps ~


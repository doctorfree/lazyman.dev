---
layout: post
title: RNvim Configuration Health Check
toc: true
post_style: page
---

# nvim-RNvim Neovim health check

--------
diffview: require("diffview.health").check()

Checking plugin dependencies ~
- OK nvim-web-devicons installed.

Checking VCS tools ~
- The plugin requires at least one of the supported VCS tools to be valid.
- OK Git found.
- WARNING Git version is outdated! Some functionality might not work as expected, or not at all! Current: 2.25.1, wanted: 2.31.0
- WARNING Configured `hg_cmd` is not executable: 'hg'
- ERROR No valid VCS tool was found!

--------
hydra: require("hydra.health").check()

Hydra: Checking settings ~
- OK             `timeoutlen` (value: 1000) is set to a good value.
  

--------
lazy: require("lazy.health").check()

lazy.nvim ~
- OK Git installed
- OK no existing packages found by other package managers
- OK packer_compiled.lua not found

--------
lspsaga: require("lspsaga.health").check()

Lspsaga.nvim report ~
- OK `tree-sitter` found 
- OK tree-sitter `markdown` parser found
- ERROR tree-sitter `markdown_inline` parser not found

--------
magma: health#magma#check

requirements ~
- OK NeoVim >=0.5
- OK Python >=3.8
- OK Python package pynvim found
- ERROR Python package jupyter-client not found
  - ADVICE:
    - pip install jupyter-client
- OK Python package ueberzug found
- OK Python package Pillow found
- ERROR Python package cairosvg not found
  - ADVICE:
    - pip install cairosvg
- ERROR Python package pnglatex not found
  - ADVICE:
    - pip install pnglatex
- ERROR Python package plotly not found
  - ADVICE:
    - pip install plotly
- ERROR Python package kaleido not found
  - ADVICE:
    - pip install kaleido

--------
mason: require("mason.health").check()

mason.nvim ~
- OK mason.nvim version v1.8.0
- OK PATH: prepend
- OK Providers: 
  mason.providers.registry-api
  mason.providers.client
- OK neovim version >= 0.7.0

mason.nvim [Registries] ~
- ERROR Registry `github.com/mason-org/mason-registry [uninstalled]` is not installed.
  - ADVICE:
    - Run :MasonUpdate to install.

mason.nvim [Core utils] ~
- OK unzip: `UnZip 6.00 of 20 April 2009, by Debian. Original by Info-ZIP.`
- OK wget: `GNU Wget 1.20.3 built on linux-gnu.`
- OK curl: `curl 7.68.0 (x86_64-pc-linux-gnu) libcurl/7.68.0 OpenSSL/1.1.1f zlib/1.2.11 brotli/1.0.7 libidn2/2.2.0 libpsl/0.21.0 (+libidn2/2.2.0) libssh/0.9.3/openssl/zlib nghttp2/1.40.0 librtmp/2.3`
- OK gzip: `gzip 1.10`
- OK tar: `tar (GNU tar) 1.30`
- OK bash: `GNU bash, version 5.0.17(1)-release (x86_64-pc-linux-gnu)`
- OK sh: `Ok`

mason.nvim [Languages] ~
- OK Go: `go version go1.20.3 linux/amd64`
- OK Ruby: `ruby 2.7.0p0 (2019-12-25 revision 647ee6f091) [x86_64-linux-gnu]`
- OK cargo: `cargo 1.72.0 (103a7ff2e 2023-08-15)`
- OK PHP: `PHP 7.4.3-4ubuntu2.19 (cli) (built: Jun 27 2023 15:49:59) ( NTS )`
- OK node: `v16.13.2`
- WARNING luarocks: unsupported version `/usr/bin/luarocks 2.4.2`
  - ADVICE:
    - Luarocks version must be >= 3.0.0.
- OK Composer: `Composer 1.10.1 2020-03-13 20:34:27`
- OK julia: `julia version 1.4.1`
- OK python: `Python 3.8.10`
- OK java: `openjdk version "11.0.20.1" 2023-08-24`
- OK RubyGem: `3.1.2`
- OK javac: `javac 11.0.20.1`
- OK npm: `8.5.2`
- OK pip: `pip 23.2.1 from /home/ronnie/.local/lib/python3.8/site-packages/pip (python 3.8)`
- OK python venv: `Ok`

mason.nvim [GitHub] ~
- OK GitHub API rate limit. Used: 27. Remaining: 4973. Limit: 5000. Reset: Mon 11 Sep 2023 11:43:58 AM PDT.

--------
null-ls: require("null-ls.health").check()

- no sources registered

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
- $COLORTERM="truecolor"

--------
nvim-treesitter: require("nvim-treesitter.health").check()

Installation ~
- OK `tree-sitter` found 0.20.8 (parser generator, only needed for :TSInstallFromGrammar)
- OK `node` found v16.13.2 (only needed for :TSInstallFromGrammar)
- OK `git` executable found.
- OK `cc` executable found. Selected from { vim.NIL, "cc", "gcc", "clang", "cl", "zig" }
  Version: cc (Ubuntu 10.5.0-1ubuntu1~20.04) 10.5.0
- OK Neovim was compiled with tree-sitter runtime ABI version 14 (required >=13). Parsers must be compatible with runtime ABI.

OS Info:
{
  machine = "x86_64",
  release = "5.4.0-162-generic",
  sysname = "Linux",
  version = "#179-Ubuntu SMP Mon Aug 14 08:51:31 UTC 2023"
} ~

Parser/Features         H L F I J
  - lua                 ✓ ✓ ✓ ✓ ✓
  - markdown            ✓ . ✓ ✓ ✓
  - yaml                ✓ ✓ ✓ ✓ ✓

  Legend: H[ighlight], L[ocals], F[olds], I[ndents], In[j]ections
         +) multiple parsers found, only one will be used
         x) errors found in the query, try to run :TSUpdate {lang} ~

--------
provider: health#provider#check

Clipboard (optional) ~
- OK Clipboard tool found: xsel

Python 3 provider (optional) ~
- `g:python3_host_prog` is not set.  Searching for python3 in the environment.
- Multiple python3 executables found.  Set `g:python3_host_prog` to avoid surprises.
- Executable: /usr/bin/python3
- Other python executable: /bin/python3
- Python version: 3.8.10
- pynvim version: 0.4.3
- OK Latest pynvim is installed.

Python virtualenv ~
- OK no $VIRTUAL_ENV

Ruby provider (optional) ~
- Ruby: ruby 2.7.0p0 (2019-12-25 revision 647ee6f091) [x86_64-linux-gnu]
- WARNING `neovim-ruby-host` not found.
  - ADVICE:
    - Run `gem install neovim` to ensure the neovim RubyGem is installed.
    - Run `gem environment` to ensure the gem bin directory is in $PATH.
    - If you are using rvm/rbenv/chruby, try "rehashing".
    - See :help |g:ruby_host_prog| for non-standard gem installations.
    - You may disable this provider (and warning) by adding `let g:loaded_ruby_provider = 0` to your init.vim

Node.js provider (optional) ~
- Node.js: v16.13.2
- Nvim node.js host: /home/ronnie/.local/lib/node_modules/neovim/bin/cli.js
- OK Latest "neovim" npm/yarn/pnpm package is installed: 4.10.1

Perl provider (optional) ~
- WARNING "Neovim::Ext" cpan module is not installed
  - ADVICE:
    - See :help |provider-perl| for more information.
    - You may disable this provider (and warning) by adding `let g:loaded_perl_provider = 0` to your init.vim

--------
telescope: require("telescope.health").check()

Checking for required plugins ~
- OK plenary installed.
- OK nvim-treesitter installed.

Checking external dependencies ~
- OK rg: found ripgrep 12.1.1 (rev 7cb211378a)
- OK fd: found fd 7.4.0

--------

Telescope Extension: `dap` ~
- No healthcheck provided

Telescope Extension: `file_browser` ~
- No healthcheck provided

Telescope Extension: `fzy_native` ~
- No healthcheck provided

Telescope Extension: `lazy` ~
- No healthcheck provided

Telescope Extension: `notify` ~
- No healthcheck provided

Telescope Extension: `ui-select` ~
- No healthcheck provided

--------
vim.lsp: require("vim.lsp.health").check()

- LSP log level : WARN
- Log path: /home/ronnie/.local/state/nvim-RNvim/lsp.log
- Log size: 1 KB

vim.lsp: Active Clients ~
- No active clients

--------
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/nvim-RNvim/lazy/nvim-treesitter/parser/lua.so
- OK Parser: markdown   ABI: 14, path: /home/ronnie/.local/share/nvim-RNvim/lazy/nvim-treesitter/parser/markdown.so
- OK Parser: yaml       ABI: 13, path: /home/ronnie/.local/share/nvim-RNvim/lazy/nvim-treesitter/parser/yaml.so

--------
which-key: require("which-key.health").check()

WhichKey: checking conflicting keymaps ~
- OK No conflicting keymaps found


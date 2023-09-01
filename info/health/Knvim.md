---
layout: post
title: Knvim Configuration Health Check
toc: true
post_style: page
---

# nvim-Knvim Neovim health check

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
lazy: require("lazy.health").check()

lazy.nvim ~
- OK Git installed
- OK no existing packages found by other package managers
- OK packer_compiled.lua not found

--------
mason: require("mason.health").check()

mason.nvim ~
- OK mason.nvim version v1.7.0
- OK PATH: prepend
- OK Providers: 
  mason.providers.registry-api
  mason.providers.client
- OK neovim version >= 0.7.0

mason.nvim [Registries] ~
- OK Registry `github.com/mason-org/mason-registry version: 2023-09-01-roman-brace` is installed.

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
- OK python3_host_prog: `Python 3.10.12`
- OK java: `openjdk version "11.0.20.1" 2023-08-24`
- OK RubyGem: `3.3.5`
- OK javac: `javac 11.0.20.1`
- OK python3_host_prog pip: `pip 23.2.1 from /home/ronnie/.local/lib/python3.10/site-packages/pip (python 3.10)`
- OK pip: `pip 23.2.1 from /home/ronnie/.local/lib/python3.10/site-packages/pip (python 3.10)`
- OK python venv: `Ok`
- OK npm: `9.5.1`

mason.nvim [GitHub] ~
- OK GitHub API rate limit. Used: 20. Remaining: 4980. Limit: 5000. Reset: Fri 01 Sep 2023 12:37:11 PM PDT.

--------
noice: require("noice.health").check()

noice.nvim ~
- OK **Neovim** >= 0.8.0
- OK **vim.go.lazyredraw** is not enabled
- OK **nvim-notify** is installed
- OK **TreeSitter vim** parser is installed
- OK **TreeSitter regex** parser is installed
- OK **TreeSitter lua** parser is installed
- OK **TreeSitter bash** parser is installed
- OK **TreeSitter markdown** parser is installed
- OK **TreeSitter markdown_inline** parser is installed

--------
null-ls: require("null-ls.health").check()

- OK black: the command "black" is executable.
- ERROR prettierd: the command "prettierd" is not executable.
- OK pycodestyle: the command "pycodestyle" is executable.
- ERROR cpplint: the command "cpplint" is not executable.
- OK shellcheck: the command "shellcheck" is executable.

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
nvim-dap-repl-highlights: require("nvim-dap-repl-highlights.health").check()

- OK 

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
  - bibtex              ✓ . ✓ ✓ .
  - c                   ✓ ✓ ✓ ✓ ✓
  - cmake               ✓ . ✓ ✓ .
  - cpp                 ✓ ✓ ✓ ✓ ✓
  - css                 ✓ . ✓ ✓ ✓
  - dap_repl            ✓ . . . .
  - dockerfile          ✓ . . . ✓
  - html                ✓ ✓ ✓ ✓ ✓
  - javascript          ✓ ✓ ✓ ✓ ✓
  - json                ✓ ✓ ✓ ✓ .
  - latex               ✓ . ✓ . ✓
  - lua                 ✓ ✓ ✓ ✓ ✓
  - markdown            ✓ . ✓ ✓ ✓
  - markdown_inline     ✓ . . . ✓
  - python              ✓ ✓ ✓ ✓ ✓
  - query               ✓ ✓ ✓ ✓ ✓
  - regex               ✓ . . . .
  - sql                 ✓ . . ✓ ✓
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
- Using: g:python3_host_prog = "/usr/bin/python3"
- Executable: /usr/bin/python3
- Python version: 3.10.12
- pynvim version: 0.4.3
- OK Latest pynvim is installed.

Python virtualenv ~
- OK no $VIRTUAL_ENV

Ruby provider (optional) ~
- Disabled (g:loaded_ruby_provider=0).

Node.js provider (optional) ~
- Node.js: v18.16.0
- Nvim node.js host: /home/ronnie/.local/lib/node_modules/neovim/bin/cli.js
- OK Latest "neovim" npm/yarn/pnpm package is installed: 4.10.1

Perl provider (optional) ~
- Disabled (g:loaded_perl_provider=0).

--------
rainbow-delimiters: require("rainbow-delimiters.health").check()

Custom strategies ~
- OK Valid custom default strategy.
- OK Valid custom strategy for 'vim'.

Custom queries ~

Custom highlight groups ~
- OK Highlight group 'RainbowDelimiterRed' defined.
- OK Highlight group 'RainbowDelimiterYellow' defined.
- OK Highlight group 'RainbowDelimiterBlue' defined.
- OK Highlight group 'RainbowDelimiterOrange' defined.
- OK Highlight group 'RainbowDelimiterGreen' defined.
- OK Highlight group 'RainbowDelimiterViolet' defined.
- OK Highlight group 'RainbowDelimiterCyan' defined.

--------
telescope: require("telescope.health").check()

Checking for required plugins ~
- OK plenary installed.
- OK nvim-treesitter installed.

Checking external dependencies ~
- OK rg: found ripgrep 13.0.0
- OK fd: found fd 8.7.0

--------

Telescope Extension: `bibtex` ~
- No healthcheck provided

Telescope Extension: `file_browser` ~
- No healthcheck provided

Telescope Extension: `fzf` ~
- OK lib working as expected
- OK file_sorter correctly configured
- OK generic_sorter correctly configured

Telescope Extension: `notify` ~
- No healthcheck provided

--------
vim.lsp: require("vim.lsp.health").check()

- LSP log level : WARN
- Log path: /home/ronnie/.local/state/nvim-Knvim/lsp.log
- Log size: 0 KB

vim.lsp: Active Clients ~
- null-ls (id=1, root_dir=/home/ronnie/.config/nvim-Lazyman)

--------
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: bash       ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/bash.so
- OK Parser: bibtex     ABI: 13, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/bibtex.so
- OK Parser: c          ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/c.so
- OK Parser: cmake      ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/cmake.so
- OK Parser: cpp        ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/cpp.so
- OK Parser: css        ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/css.so
- OK Parser: dap_repl   ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/dap_repl.so
- OK Parser: dockerfile ABI: 13, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/dockerfile.so
- OK Parser: html       ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/html.so
- OK Parser: javascript ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/javascript.so
- OK Parser: json       ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/json.so
- OK Parser: latex      ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/latex.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/lua.so
- OK Parser: markdown   ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/markdown.so
- OK Parser: markdown_inline ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/markdown_inline.so
- OK Parser: python     ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/python.so
- OK Parser: regex      ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/regex.so
- OK Parser: sql        ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/sql.so
- OK Parser: typescript ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/typescript.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/vim.so
- OK Parser: yaml       ABI: 13, path: /home/ronnie/.local/share/nvim-Knvim/lazy/nvim-treesitter/parser/yaml.so
- OK Parser: c          ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/c.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/query.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vimdoc.so


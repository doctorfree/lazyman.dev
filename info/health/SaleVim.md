---
layout: post
title: SaleVim Configuration Health Check
toc: true
post_style: page
---

# nvim-SaleVim Neovim health check

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
- ERROR Registry `github.com/mason-org/mason-registry [uninstalled]` is not installed.
  - ADVICE:
    - Run :MasonUpdate to install.

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
- OK PHP: `PHP 8.1.2-1ubuntu2.14 (cli) (built: Aug 18 2023 11:41:11) (NTS)`
- OK cargo: `cargo 1.72.0 (103a7ff2e 2023-08-15)`
- OK node: `v18.16.0`
- OK luarocks: `/usr/bin/luarocks 3.8.0`
- OK Composer: `Composer 2.2.6 2022-02-04 17:00:38`
- WARNING julia: not available
  - ADVICE:
    - spawn: julia failed with exit code - and signal -. julia is not executable
- OK python: `Python 3.10.12`
- OK RubyGem: `3.3.5`
- OK java: `openjdk version "11.0.20.1" 2023-08-24`
- OK javac: `javac 11.0.20.1`
- OK pip: `pip 23.2.1 from /home/ronnie/.local/lib/python3.10/site-packages/pip (python 3.10)`
- OK python venv: `Ok`
- OK npm: `9.5.1`

mason.nvim [GitHub] ~
- OK GitHub API rate limit. Used: 20. Remaining: 4980. Limit: 5000. Reset: Fri 01 Sep 2023 12:37:11 PM PDT.

--------
null-ls: require("null-ls.health").check()

- ERROR prettier: the command "prettier" is not executable.
- OK black: the command "black" is executable.
- OK stylua: the command "stylua" is executable.

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
  - ada                 ✓ ✓ ✓ . .
  - agda                ✓ . ✓ . .
  - arduino             ✓ ✓ ✓ ✓ ✓
  - astro               ✓ ✓ ✓ ✓ ✓
  - awk                 ✓ . . . ✓
  - bash                ✓ ✓ ✓ . ✓
  - bass                ✓ ✓ ✓ ✓ ✓
  - beancount           ✓ . ✓ . .
  - bibtex              ✓ . ✓ ✓ .
  - bicep               ✓ ✓ ✓ ✓ ✓
  - bitbake             ✓ ✓ ✓ ✓ ✓
  - blueprint           ✓ . . . .
  - c                   ✓ ✓ ✓ ✓ ✓
  - c_sharp             ✓ ✓ ✓ . ✓
  - cairo               ✓ ✓ ✓ ✓ ✓
  - capnp               ✓ ✓ ✓ ✓ ✓
  - chatito             ✓ ✓ ✓ ✓ ✓
  - clojure             ✓ ✓ ✓ . ✓
  - cmake               ✓ . ✓ ✓ .
  - comment             ✓ . . . .
  - commonlisp          ✓ ✓ ✓ . .
  - cooklang            ✓ . . . .
  - corn                ✓ ✓ ✓ ✓ .
  - cpon                ✓ ✓ ✓ ✓ ✓
  - cpp                 ✓ ✓ ✓ ✓ ✓
  - css                 ✓ . ✓ ✓ ✓
  - csv                 ✓ . . . .
  - cuda                ✓ ✓ ✓ ✓ ✓
  - cue                 ✓ ✓ ✓ ✓ ✓
  - dart                ✓ ✓ ✓ ✓ ✓
  - devicetree          ✓ ✓ ✓ ✓ ✓
  - dhall               ✓ . ✓ . ✓
  - diff                ✓ . . . .
  - dockerfile          ✓ . . . ✓
  - dot                 ✓ . . . ✓
  - doxygen             ✓ . . ✓ ✓
  - dtd                 ✓ . ✓ . ✓
  - ebnf                ✓ . . . .
  - eex                 ✓ . . . ✓
  - elixir              ✓ ✓ ✓ ✓ ✓
  - elm                 ✓ . . . ✓
  - elsa                ✓ ✓ ✓ ✓ ✓
  - elvish              ✓ . . . ✓
  - embedded_template   ✓ . . . ✓
  - erlang              ✓ . ✓ . .
  - fennel              ✓ ✓ ✓ . ✓
  - firrtl              ✓ ✓ ✓ ✓ ✓
  - fish                ✓ ✓ ✓ ✓ ✓
  - foam                ✓ ✓ ✓ ✓ ✓
  - forth               ✓ ✓ ✓ ✓ ✓
  - fortran             ✓ . ✓ ✓ .
  - fsh                 ✓ . . . .
  - func                ✓ . . . .
  - fusion              ✓ ✓ ✓ ✓ .
  - gdscript            ✓ ✓ ✓ ✓ ✓
  - git_config          ✓ . . . .
  - git_rebase          ✓ . . . ✓
  - gitattributes       ✓ . . . ✓
  - gitcommit           ✓ . . . ✓
  - gitignore           ✓ . . . .
  - gleam               ✓ ✓ ✓ ✓ ✓
  - glimmer             ✓ ✓ ✓ ✓ .
  - glsl                ✓ ✓ ✓ ✓ ✓
  - go                  ✓ ✓ ✓ ✓ ✓
  - godot_resource      ✓ ✓ ✓ . .
  - gomod               ✓ . . . ✓
  - gosum               ✓ . . . .
  - gowork              ✓ . . . ✓
  - gpg                 ✓ . . . ✓
  - graphql             ✓ . . ✓ ✓
  - groovy              ✓ . . . ✓
  - hack                ✓ . . . .
  - hare                ✓ ✓ ✓ ✓ ✓
  - haskell             ✓ . ✓ . ✓
  - haskell_persistent  ✓ . ✓ . .
  - hcl                 ✓ . ✓ ✓ ✓
  - heex                ✓ ✓ ✓ ✓ ✓
  - hjson               ✓ ✓ ✓ ✓ ✓
  - hlsl                ✓ ✓ ✓ ✓ ✓
  - hocon               ✓ . . . ✓
  - hoon                ✓ ✓ ✓ . .
  - html                ✓ ✓ ✓ ✓ ✓
  - htmldjango          ✓ . ✓ ✓ ✓
  - http                ✓ . . . ✓
  - hurl                ✓ . ✓ ✓ ✓
  - ini                 ✓ . ✓ . .
  - ispc                ✓ ✓ ✓ ✓ ✓
  - janet_simple        ✓ ✓ ✓ . ✓
  - java                ✓ ✓ ✓ ✓ ✓
  - javascript          ✓ ✓ ✓ ✓ ✓
  - jq                  ✓ . . . ✓
  - jsdoc               ✓ . . . .
  - json                ✓ ✓ ✓ ✓ .
  - json5               ✓ . . . ✓
  - jsonc               ✓ ✓ ✓ ✓ ✓
  - jsonnet             ✓ ✓ ✓ . .
  - julia               ✓ ✓ ✓ ✓ ✓
  - kconfig             ✓ ✓ ✓ ✓ ✓
  - kdl                 ✓ ✓ ✓ ✓ ✓
  - kotlin              ✓ ✓ ✓ . ✓
  - lalrpop             ✓ ✓ . . ✓
  - latex               ✓ . ✓ . ✓
  - ledger              ✓ . ✓ ✓ ✓
  - llvm                ✓ . . . .
  - lua                 ✓ ✓ ✓ ✓ ✓
  - luadoc              ✓ . . . .
  - luap                ✓ . . . .
  - luau                ✓ ✓ ✓ ✓ ✓
  - m68k                ✓ ✓ ✓ . ✓
  - make                ✓ . ✓ . ✓
  - markdown            ✓ . ✓ ✓ ✓
  - markdown_inline     ✓ . . . ✓
  - matlab              ✓ ✓ ✓ ✓ ✓
  - menhir              ✓ . . . ✓
  - mermaid             ✓ . . . .
  - meson               ✓ . ✓ . ✓
  - nickel              ✓ . . ✓ .
  - ninja               ✓ . ✓ ✓ .
  - nix                 ✓ ✓ ✓ . ✓
  - norg                . . . . .
  - nqc                 ✓ ✓ ✓ ✓ ✓
  - objc                ✓ ✓ ✓ ✓ ✓
  - ocaml               ✓ ✓ ✓ ✓ ✓
  - ocaml_interface     ✓ ✓ ✓ ✓ ✓
  - ocamllex            ✓ . . . ✓
  - odin                ✓ ✓ ✓ ✓ ✓
  - org                 . . . . .
  - pascal              ✓ ✓ ✓ ✓ ✓
  - passwd              ✓ . . . .
  - pem                 ✓ . ✓ . ✓
  - perl                ✓ . ✓ . ✓
  - php                 ✓ ✓ ✓ ✓ ✓
  - phpdoc              ✓ . . . .
  - pioasm              ✓ . . . ✓
  - po                  ✓ . ✓ . ✓
  - poe_filter          ✓ . ✓ ✓ ✓
  - pony                ✓ ✓ ✓ ✓ ✓
  - prisma              ✓ . . . .
  - promql              ✓ . . . ✓
  - proto               ✓ . ✓ . .
  - prql                ✓ . . . ✓
  - psv                 ✓ . . . .
  - pug                 ✓ . . . ✓
  - puppet              ✓ ✓ ✓ ✓ ✓
  - pymanifest          ✓ . . . ✓
  - python              ✓ ✓ ✓ ✓ ✓
  - ql                  ✓ ✓ ✓ ✓ ✓
  - qmldir              ✓ . . . ✓
  - qmljs               ✓ . ✓ . .
  - query               ✓ ✓ ✓ ✓ ✓
  - r                   ✓ ✓ . ✓ ✓
  - racket              ✓ . ✓ . ✓
  - rasi                ✓ ✓ ✓ ✓ .
  - re2c                ✓ ✓ ✓ ✓ ✓
  - regex               ✓ . . . .
  - rego                ✓ . . . ✓
  - requirements        ✓ . . . ✓
  - rnoweb              ✓ . ✓ . ✓
  - robot               ✓ . ✓ ✓ .
  - ron                 ✓ ✓ ✓ ✓ ✓
  - rst                 ✓ ✓ . . ✓
  - ruby                ✓ ✓ ✓ ✓ ✓
  - rust                ✓ ✓ ✓ ✓ ✓
  - scala               ✓ ✓ ✓ . ✓
  - scfg                ✓ . . . ✓
  - scheme              ✓ . ✓ . ✓
  - scss                ✓ . ✓ ✓ .
  - slint               ✓ . . ✓ .
  - smali               ✓ ✓ ✓ ✓ ✓
  - smithy              ✓ . . . .
  - solidity            ✓ . . . .
  - sparql              ✓ ✓ ✓ ✓ ✓
  - sql                 ✓ . . ✓ ✓
  - squirrel            ✓ ✓ ✓ ✓ ✓
  - starlark            ✓ ✓ ✓ ✓ ✓
  - strace              ✓ . . . ✓
  - supercollider       ✓ ✓ ✓ ✓ ✓
  - surface             ✓ . ✓ ✓ ✓
  - svelte              ✓ . ✓ ✓ ✓
  - sxhkdrc             ✓ . ✓ . ✓
  - systemtap           ✓ ✓ ✓ . ✓
  - t32                 ✓ ✓ ✓ ✓ ✓
  - tablegen            ✓ ✓ ✓ ✓ ✓
  - teal                ✓ ✓ ✓ ✓ ✓
  - terraform           ✓ . ✓ ✓ ✓
  - thrift              ✓ ✓ ✓ ✓ ✓
  - tiger               ✓ ✓ ✓ ✓ ✓
  - tlaplus             ✓ ✓ ✓ . ✓
  - todotxt             ✓ . . . .
  - toml                ✓ ✓ ✓ ✓ ✓
  - tsv                 ✓ . . . .
  - tsx                 ✓ ✓ ✓ ✓ ✓
  - turtle              ✓ ✓ ✓ ✓ ✓
  - twig                ✓ . . . ✓
  - typescript          ✓ ✓ ✓ ✓ ✓
  - ungrammar           ✓ ✓ ✓ ✓ ✓
  - usd                 ✓ ✓ ✓ ✓ .
  - uxntal              ✓ ✓ ✓ ✓ ✓
  - v                   ✓ ✓ ✓ ✓ ✓
  - vala                ✓ . ✓ . .
  - verilog             ✓ ✓ ✓ . ✓
  - vhs                 ✓ . . . .
  - vim                 ✓ ✓ ✓ . ✓
  - vimdoc              ✓ . . . ✓
  - vue                 ✓ . ✓ ✓ ✓
  - wgsl                ✓ . ✓ ✓ .
  - wgsl_bevy           ✓ . ✓ ✓ .
  - xml                 ✓ . ✓ ✓ ✓
  - yaml                ✓ ✓ ✓ ✓ ✓
  - yang                ✓ . ✓ ✓ ✓
  - yuck                ✓ ✓ ✓ ✓ ✓
  - zig                 ✓ . ✓ ✓ ✓

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
telescope: require("telescope.health").check()

Checking for required plugins ~
- OK plenary installed.
- OK nvim-treesitter installed.

Checking external dependencies ~
- OK rg: found ripgrep 13.0.0
- OK fd: found fd 8.7.0

--------

Telescope Extension: `projects` ~
- No healthcheck provided

--------
vim.lsp: require("vim.lsp.health").check()

- LSP log level : WARN
- Log path: /home/ronnie/.local/state/nvim-SaleVim/lsp.log
- Log size: 0 KB

vim.lsp: Active Clients ~
- null-ls (id=1, root_dir=/home/ronnie/.config/nvim-Lazyman)

--------
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: ada        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/ada.so
- OK Parser: agda       ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/agda.so
- OK Parser: arduino    ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/arduino.so
- OK Parser: astro      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/astro.so
- OK Parser: awk        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/awk.so
- OK Parser: bash       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/bash.so
- OK Parser: bass       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/bass.so
- OK Parser: beancount  ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/beancount.so
- OK Parser: bibtex     ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/bibtex.so
- OK Parser: bicep      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/bicep.so
- OK Parser: bitbake    ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/bitbake.so
- OK Parser: blueprint  ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/blueprint.so
- OK Parser: c          ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/c.so
- OK Parser: c_sharp    ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/c_sharp.so
- OK Parser: cairo      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/cairo.so
- OK Parser: capnp      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/capnp.so
- OK Parser: chatito    ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/chatito.so
- OK Parser: clojure    ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/clojure.so
- OK Parser: cmake      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/cmake.so
- OK Parser: comment    ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/comment.so
- OK Parser: commonlisp ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/commonlisp.so
- OK Parser: cooklang   ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/cooklang.so
- OK Parser: corn       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/corn.so
- OK Parser: cpon       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/cpon.so
- OK Parser: cpp        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/cpp.so
- OK Parser: css        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/css.so
- OK Parser: csv        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/csv.so
- OK Parser: cuda       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/cuda.so
- OK Parser: cue        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/cue.so
- OK Parser: dart       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/dart.so
- OK Parser: devicetree ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/devicetree.so
- OK Parser: dhall      ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/dhall.so
- OK Parser: diff       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/diff.so
- OK Parser: dockerfile ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/dockerfile.so
- OK Parser: dot        ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/dot.so
- OK Parser: doxygen    ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/doxygen.so
- OK Parser: dtd        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/dtd.so
- OK Parser: ebnf       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/ebnf.so
- OK Parser: eex        ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/eex.so
- OK Parser: elixir     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/elixir.so
- OK Parser: elm        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/elm.so
- OK Parser: elsa       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/elsa.so
- OK Parser: elvish     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/elvish.so
- OK Parser: embedded_template ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/embedded_template.so
- OK Parser: erlang     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/erlang.so
- OK Parser: fennel     ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/fennel.so
- OK Parser: firrtl     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/firrtl.so
- OK Parser: fish       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/fish.so
- OK Parser: foam       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/foam.so
- OK Parser: forth      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/forth.so
- OK Parser: fortran    ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/fortran.so
- OK Parser: fsh        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/fsh.so
- OK Parser: func       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/func.so
- OK Parser: fusion     ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/fusion.so
- OK Parser: gdscript   ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/gdscript.so
- OK Parser: git_config ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/git_config.so
- OK Parser: git_rebase ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/git_rebase.so
- OK Parser: gitattributes ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/gitattributes.so
- OK Parser: gitcommit  ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/gitcommit.so
- OK Parser: gitignore  ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/gitignore.so
- OK Parser: gleam      ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/gleam.so
- OK Parser: glimmer    ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/glimmer.so
- OK Parser: glsl       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/glsl.so
- OK Parser: go         ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/go.so
- OK Parser: godot_resource ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/godot_resource.so
- OK Parser: gomod      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/gomod.so
- OK Parser: gosum      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/gosum.so
- OK Parser: gowork     ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/gowork.so
- OK Parser: gpg        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/gpg.so
- OK Parser: graphql    ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/graphql.so
- OK Parser: groovy     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/groovy.so
- OK Parser: hack       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/hack.so
- OK Parser: hare       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/hare.so
- OK Parser: haskell    ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/haskell.so
- OK Parser: haskell_persistent ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/haskell_persistent.so
- OK Parser: hcl        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/hcl.so
- OK Parser: heex       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/heex.so
- OK Parser: hjson      ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/hjson.so
- OK Parser: hlsl       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/hlsl.so
- OK Parser: hocon      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/hocon.so
- OK Parser: hoon       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/hoon.so
- OK Parser: html       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/html.so
- OK Parser: htmldjango ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/htmldjango.so
- OK Parser: http       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/http.so
- OK Parser: hurl       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/hurl.so
- OK Parser: ini        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/ini.so
- OK Parser: ispc       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/ispc.so
- OK Parser: janet_simple ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/janet_simple.so
- OK Parser: java       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/java.so
- OK Parser: javascript ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/javascript.so
- OK Parser: jq         ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/jq.so
- OK Parser: jsdoc      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/jsdoc.so
- OK Parser: json       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/json.so
- OK Parser: json5      ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/json5.so
- OK Parser: jsonc      ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/jsonc.so
- OK Parser: jsonnet    ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/jsonnet.so
- OK Parser: julia      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/julia.so
- OK Parser: kconfig    ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/kconfig.so
- OK Parser: kdl        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/kdl.so
- OK Parser: kotlin     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/kotlin.so
- OK Parser: lalrpop    ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/lalrpop.so
- OK Parser: latex      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/latex.so
- OK Parser: ledger     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/ledger.so
- OK Parser: llvm       ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/llvm.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/lua.so
- OK Parser: luadoc     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/luadoc.so
- OK Parser: luap       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/luap.so
- OK Parser: luau       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/luau.so
- OK Parser: m68k       ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/m68k.so
- OK Parser: make       ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/make.so
- OK Parser: markdown   ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/markdown.so
- OK Parser: markdown_inline ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/markdown_inline.so
- OK Parser: matlab     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/matlab.so
- OK Parser: menhir     ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/menhir.so
- OK Parser: mermaid    ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/mermaid.so
- OK Parser: meson      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/meson.so
- OK Parser: nickel     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/nickel.so
- OK Parser: ninja      ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/ninja.so
- OK Parser: nix        ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/nix.so
- OK Parser: norg       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/norg.so
- OK Parser: nqc        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/nqc.so
- OK Parser: objc       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/objc.so
- OK Parser: ocaml      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/ocaml.so
- OK Parser: ocaml_interface ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/ocaml_interface.so
- OK Parser: ocamllex   ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/ocamllex.so
- OK Parser: odin       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/odin.so
- OK Parser: org        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/org.so
- OK Parser: pascal     ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/pascal.so
- OK Parser: passwd     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/passwd.so
- OK Parser: pem        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/pem.so
- OK Parser: perl       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/perl.so
- OK Parser: php        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/php.so
- OK Parser: phpdoc     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/phpdoc.so
- OK Parser: pioasm     ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/pioasm.so
- OK Parser: po         ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/po.so
- OK Parser: poe_filter ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/poe_filter.so
- OK Parser: pony       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/pony.so
- OK Parser: prisma     ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/prisma.so
- OK Parser: promql     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/promql.so
- OK Parser: proto      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/proto.so
- OK Parser: prql       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/prql.so
- OK Parser: psv        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/psv.so
- OK Parser: pug        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/pug.so
- OK Parser: puppet     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/puppet.so
- OK Parser: pymanifest ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/pymanifest.so
- OK Parser: python     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/python.so
- OK Parser: ql         ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/ql.so
- OK Parser: qmldir     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/qmldir.so
- OK Parser: qmljs      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/qmljs.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/query.so
- OK Parser: r          ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/r.so
- OK Parser: racket     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/racket.so
- OK Parser: rasi       ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/rasi.so
- OK Parser: re2c       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/re2c.so
- OK Parser: regex      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/regex.so
- OK Parser: rego       ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/rego.so
- OK Parser: requirements ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/requirements.so
- OK Parser: rnoweb     ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/rnoweb.so
- OK Parser: robot      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/robot.so
- OK Parser: ron        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/ron.so
- OK Parser: rst        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/rst.so
- OK Parser: ruby       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/ruby.so
- OK Parser: rust       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/rust.so
- OK Parser: scala      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/scala.so
- OK Parser: scfg       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/scfg.so
- OK Parser: scheme     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/scheme.so
- OK Parser: scss       ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/scss.so
- OK Parser: slint      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/slint.so
- OK Parser: smali      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/smali.so
- OK Parser: smithy     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/smithy.so
- OK Parser: solidity   ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/solidity.so
- OK Parser: sparql     ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/sparql.so
- OK Parser: sql        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/sql.so
- OK Parser: squirrel   ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/squirrel.so
- OK Parser: starlark   ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/starlark.so
- OK Parser: strace     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/strace.so
- OK Parser: supercollider ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/supercollider.so
- OK Parser: surface    ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/surface.so
- OK Parser: svelte     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/svelte.so
- OK Parser: sxhkdrc    ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/sxhkdrc.so
- OK Parser: systemtap  ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/systemtap.so
- OK Parser: t32        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/t32.so
- OK Parser: tablegen   ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/tablegen.so
- OK Parser: teal       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/teal.so
- OK Parser: terraform  ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/terraform.so
- OK Parser: thrift     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/thrift.so
- OK Parser: tiger      ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/tiger.so
- OK Parser: tlaplus    ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/tlaplus.so
- OK Parser: todotxt    ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/todotxt.so
- OK Parser: toml       ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/toml.so
- OK Parser: tsv        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/tsv.so
- OK Parser: tsx        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/tsx.so
- OK Parser: turtle     ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/turtle.so
- OK Parser: twig       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/twig.so
- OK Parser: typescript ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/typescript.so
- OK Parser: ungrammar  ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/ungrammar.so
- OK Parser: usd        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/usd.so
- OK Parser: uxntal     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/uxntal.so
- OK Parser: v          ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/v.so
- OK Parser: vala       ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/vala.so
- OK Parser: verilog    ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/verilog.so
- OK Parser: vhs        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/vhs.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/vimdoc.so
- OK Parser: vue        ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/vue.so
- OK Parser: wgsl       ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/wgsl.so
- OK Parser: wgsl_bevy  ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/wgsl_bevy.so
- OK Parser: xml        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/xml.so
- OK Parser: yaml       ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/yaml.so
- OK Parser: yang       ABI: 13, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/yang.so
- OK Parser: yuck       ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/yuck.so
- OK Parser: zig        ABI: 14, path: /home/ronnie/.local/share/nvim-SaleVim/site/pack/packer/start/nvim-treesitter/parser/zig.so
- OK Parser: c          ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/c.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/query.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vimdoc.so

--------
which-key: require("which-key.health").check()

WhichKey: checking conflicting keymaps ~
- OK No conflicting keymaps found


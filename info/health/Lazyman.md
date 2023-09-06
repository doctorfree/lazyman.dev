---
layout: post
title: Lazyman Configuration Health Check
toc: true
post_style: page
---

# nvim-Lazyman Neovim health check

--------
hydra: require("hydra.health").check()

Hydra: Checking settings ~
- OK             `timeoutlen` (value: 300) is set to a good value.
  

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
- OK Registry `github.com/mason-org/mason-registry version: 2023-09-06-dirty-platy` is installed.

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
- OK python3_host_prog: `Python 3.8.10`
- OK java: `openjdk version "11.0.20.1" 2023-08-24`
- OK RubyGem: `3.1.2`
- OK javac: `javac 11.0.20.1`
- OK npm: `8.5.2`
- OK pip: `pip 23.2.1 from /home/ronnie/.local/lib/python3.8/site-packages/pip (python 3.8)`
- OK python venv: `Ok`
- OK python3_host_prog pip: `pip 23.2.1 from /home/ronnie/.local/lib/python3.8/site-packages/pip (python 3.8)`

mason.nvim [GitHub] ~
- OK GitHub API rate limit. Used: 27. Remaining: 4973. Limit: 5000. Reset: Wed 06 Sep 2023 01:01:44 PM PDT.

--------
mkdp: health#mkdp#check

- Platform: linux
- Nvim Version: NVIM v0.9.1
- Node version: v16.13.2

- Script: /home/ronnie/.local/share/nvim-Lazyman/lazy/markdown-preview.nvim/app/server.js
- Script exists: 1
- OK Using node

--------
noice: require("noice.health").check()

noice.nvim ~
- OK **Neovim** >= 0.8.0
- OK You're using a GUI that should work ok
- OK **vim.go.lazyredraw** is not enabled
- OK **nvim-notify** is installed
- OK **TreeSitter vim** parser is installed
- OK **TreeSitter regex** parser is installed
- OK **TreeSitter lua** parser is installed
- OK **TreeSitter bash** parser is installed
- OK **TreeSitter markdown** parser is installed
- OK **TreeSitter markdown_inline** parser is installed
- OK `vim.notify` is set to **Noice**
- WARNING `vim.lsp.handlers["textDocument/hover"]` is not configured to be handled by **Noice**
- OK `vim.lsp.handlers["textDocument/signatureHelp"]` is set to **Noice**
- OK `vim.lsp.handlers["window/showMessage"]` is set to **Noice**
- OK `vim.lsp.util.convert_input_to_markdown_lines` is set to **Noice**
- OK `vim.lsp.util.stylize_markdown` is set to **Noice**

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
  release = "5.4.0-156-generic",
  sysname = "Linux",
  version = "#173-Ubuntu SMP Tue Jul 11 07:25:22 UTC 2023"
} ~

Parser/Features         H L F I J
  - astro               ✓ ✓ ✓ ✓ ✓
  - bash                ✓ ✓ ✓ . ✓
  - css                 ✓ . ✓ ✓ ✓
  - gitcommit           ✓ . . . ✓
  - graphql             ✓ . . ✓ ✓
  - html                ✓ ✓ ✓ ✓ ✓
  - javascript          ✓ ✓ ✓ ✓ ✓
  - json                ✓ ✓ ✓ ✓ .
  - json5               ✓ . . . ✓
  - lua                 ✓ ✓ ✓ ✓ ✓
  - markdown            ✓ . ✓ ✓ ✓
  - markdown_inline     ✓ . . . ✓
  - prisma              ✓ . . . .
  - query               ✓ ✓ ✓ ✓ ✓
  - regex               ✓ . . . .
  - svelte              ✓ . ✓ ✓ ✓
  - tsx                 ✓ ✓ ✓ ✓ ✓
  - typescript          ✓ ✓ ✓ ✓ ✓
  - vim                 ✓ ✓ ✓ . ✓
  - vimdoc              ✓ . . . ✓
  - vue                 ✓ . ✓ ✓ ✓

  Legend: H[ighlight], L[ocals], F[olds], I[ndents], In[j]ections
         +) multiple parsers found, only one will be used
         x) errors found in the query, try to run :TSUpdate {lang} ~

--------
provider: health#provider#check

Clipboard (optional) ~
- OK Clipboard tool found: xsel

Python 3 provider (optional) ~
- Using: g:python3_host_prog = "/usr/bin/python3"
- Executable: /usr/bin/python3
- Python version: 3.8.10
- pynvim version: 0.4.3
- OK Latest pynvim is installed.

Python virtualenv ~
- OK no $VIRTUAL_ENV

Ruby provider (optional) ~
- Ruby: ruby 2.7.0p0 (2019-12-25 revision 647ee6f091) [x86_64-linux-gnu]
- Host: /home/ronnie/.gem/ruby/2.7.0/bin/neovim-ruby-host
- OK Latest "neovim" gem is installed: 0.9.1

Node.js provider (optional) ~
- Node.js: v16.13.2
- Nvim node.js host: /home/ronnie/.local/lib/node_modules/neovim/bin/cli.js
- OK Latest "neovim" npm/yarn/pnpm package is installed: 4.10.1

Perl provider (optional) ~
- Disabled (g:loaded_perl_provider=0).

--------
rainbow-delimiters: require("rainbow-delimiters.health").check()

- No custom configuration; see :help |rb-delimiters-setup| for information.

--------
telescope: require("telescope.health").check()

- ERROR Failed to run healthcheck for "telescope" plugin. Exception:
  function health#check, line 25
  Vim(eval):E5108: Error executing lua ...share/nvim-Lazyman/lazy/plenary.nvim/lua/plenary/job.lua:498: 'fdfind --hidden --case-sensitive --absolute-path --exec echo {//} ; ^\.git$' was unable to complete in 5000 ms
  stack traceback:
  [C]: in function 'error'
  ...share/nvim-Lazyman/lazy/plenary.nvim/lua/plenary/job.lua:498: in function 'wait'
  ...share/nvim-Lazyman/lazy/plenary.nvim/lua/plenary/job.lua:452: in function 'sync'
  ...cope-repo.nvim/lua/telescope/_extensions/repo/health.lua:25: in function 'find_repos'
  ...cope-repo.nvim/lua/telescope/_extensions/repo/health.lua:54: in function 'check_list_cmd'
  ...cope-repo.nvim/lua/telescope/_extensions/repo/health.lua:115: in function 'check'
  ...y/telescope-repo.nvim/lua/telescope/_extensions/repo.lua:7: in function 'extension_healthcheck'
  ...vim-Lazyman/lazy/telescope.nvim/lua/telescope/health.lua:123: in function 'check'
  [string "luaeval()"]:1: in main chunk

--------
telescope._extensions.repo: require("telescope._extensions.repo.health").check()

- ERROR Failed to run healthcheck for "telescope._extensions.repo" plugin. Exception:
  function health#check, line 25
  Vim(eval):E5108: Error executing lua ...share/nvim-Lazyman/lazy/plenary.nvim/lua/plenary/job.lua:498: 'fdfind --hidden --case-sensitive --absolute-path --exec echo {//} ; ^\.git$' was unable to complete in 5000 ms
  stack traceback:
  [C]: in function 'error'
  ...share/nvim-Lazyman/lazy/plenary.nvim/lua/plenary/job.lua:498: in function 'wait'
  ...share/nvim-Lazyman/lazy/plenary.nvim/lua/plenary/job.lua:452: in function 'sync'
  ...cope-repo.nvim/lua/telescope/_extensions/repo/health.lua:25: in function 'find_repos'
  ...cope-repo.nvim/lua/telescope/_extensions/repo/health.lua:54: in function 'check_list_cmd'
  ...cope-repo.nvim/lua/telescope/_extensions/repo/health.lua:115: in function 'check'
  [string "luaeval()"]:1: in main chunk

--------
vim.lsp: require("vim.lsp.health").check()

- LSP log level : WARN
- Log path: /home/ronnie/.local/state/nvim-Lazyman/lsp.log
- Log size: 6 KB

vim.lsp: Active Clients ~
- No active clients

--------
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: astro      ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/astro.so
- OK Parser: bash       ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/bash.so
- OK Parser: css        ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/css.so
- OK Parser: dap_repl   ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/dap_repl.so
- OK Parser: gitcommit  ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/gitcommit.so
- OK Parser: graphql    ABI: 13, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/graphql.so
- OK Parser: html       ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/html.so
- OK Parser: javascript ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/javascript.so
- OK Parser: json       ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/json.so
- OK Parser: json5      ABI: 13, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/json5.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/lua.so
- OK Parser: markdown   ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/markdown.so
- OK Parser: markdown_inline ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/markdown_inline.so
- OK Parser: prisma     ABI: 13, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/prisma.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/query.so
- OK Parser: regex      ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/regex.so
- OK Parser: svelte     ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/svelte.so
- OK Parser: tsx        ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/tsx.so
- OK Parser: typescript ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/typescript.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/vimdoc.so
- OK Parser: vue        ABI: 13, path: /home/ronnie/.local/share/nvim-Lazyman/lazy/nvim-treesitter/parser/vue.so

--------
which-key: require("which-key.health").check()

WhichKey: checking conflicting keymaps ~
- WARNING conflicting keymap exists for mode **"n"**, lhs: **"yS"**
- rhs: `<Plug>(nvim-surround-normal-line)`
- WARNING conflicting keymap exists for mode **"n"**, lhs: **"ys"**
- rhs: `<Plug>(nvim-surround-normal)`
- WARNING conflicting keymap exists for mode **"n"**, lhs: **"="**
- rhs: ` `
- WARNING conflicting keymap exists for mode **"n"**, lhs: **"gb"**
- rhs: `<Plug>(comment_toggle_blockwise)`
- WARNING conflicting keymap exists for mode **"n"**, lhs: **"gc"**
- rhs: `<Plug>(comment_toggle_linewise)`


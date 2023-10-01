---
layout: post
title: SeniorMars Configuration Health Check
toc: true
post_style: page
---

# nvim-SeniorMars Neovim health check

--------
coc: health#coc#check

- OK nvim version satisfied
- OK Environment check passed
- OK Javascript bundle build/index.js found
- OK Service started

--------
lazy: require("lazy.health").check()

lazy.nvim ~
- OK Git installed
- OK no existing packages found by other package managers
- OK packer_compiled.lua not found

--------
nvim: require("nvim.health").check()

Configuration ~
- OK no issues found

Runtime ~
- OK $VIMRUNTIME: /home/ronnie/.local/share/bob/v0.9.2/nvim-linux64/share/nvim/runtime

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
- OK `node` found v20.7.0 (only needed for :TSInstallFromGrammar)
- OK `git` executable found.
- OK `cc` executable found. Selected from { vim.NIL, "cc", "gcc", "clang", "cl", "zig" }
  Version: cc (Ubuntu 10.5.0-1ubuntu1~20.04) 10.5.0
- OK Neovim was compiled with tree-sitter runtime ABI version 14 (required >=13). Parsers must be compatible with runtime ABI.

OS Info:
{
  machine = "x86_64",
  release = "5.4.0-163-generic",
  sysname = "Linux",
  version = "#180-Ubuntu SMP Tue Sep 5 13:21:23 UTC 2023"
} ~

Parser/Features         H L F I J
  - bash                ✓ ✓ ✓ . ✓
  - c                   ✓ ✓ ✓ ✓ ✓
  - lua                 ✓ ✓ ✓ ✓ ✓
  - markdown            ✓ . ✓ ✓ ✓
  - markdown_inline     ✓ . . . ✓
  - query               ✓ ✓ ✓ ✓ ✓
  - regex               ✓ . . . .
  - vim                 ✓ ✓ ✓ . ✓
  - vimdoc              ✓ . . . ✓

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
- Disabled (g:loaded_ruby_provider=0).

Node.js provider (optional) ~
- Node.js: v20.7.0
- Nvim node.js host: /home/ronnie/.nvm/versions/node/v20.7.0/lib/node_modules/neovim/bin/cli.js
- OK Latest "neovim" npm/yarn/pnpm package is installed: 4.10.1

Perl provider (optional) ~
- Disabled (g:loaded_perl_provider=0).

--------
targets: health#targets#check

- OK No conflicting mappings found

--------
telescope: require("telescope.health").check()

Checking for required plugins ~
- OK plenary installed.
- OK nvim-treesitter installed.

Checking external dependencies ~
- OK rg: found ripgrep 12.1.1 (rev 7cb211378a)
- OK fd: found fd 7.4.0

--------

Telescope Extension: `frecency` ~
- OK sqlite.lua installed.
- nvim-web-devicons is not installed.

--------
vim.lsp: require("vim.lsp.health").check()

- LSP log level : WARN
- Log path: /home/ronnie/.local/state/nvim-SeniorMars/lsp.log
- Log size: 1 KB

vim.lsp: Active Clients ~
- No active clients

--------
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: bash       ABI: 14, path: /home/ronnie/.local/share/nvim-SeniorMars/lazy/nvim-treesitter/parser/bash.so
- OK Parser: c          ABI: 14, path: /home/ronnie/.local/share/nvim-SeniorMars/lazy/nvim-treesitter/parser/c.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/nvim-SeniorMars/lazy/nvim-treesitter/parser/lua.so
- OK Parser: markdown   ABI: 14, path: /home/ronnie/.local/share/nvim-SeniorMars/lazy/nvim-treesitter/parser/markdown.so
- OK Parser: markdown_inline ABI: 14, path: /home/ronnie/.local/share/nvim-SeniorMars/lazy/nvim-treesitter/parser/markdown_inline.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/nvim-SeniorMars/lazy/nvim-treesitter/parser/query.so
- OK Parser: regex      ABI: 14, path: /home/ronnie/.local/share/nvim-SeniorMars/lazy/nvim-treesitter/parser/regex.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/nvim-SeniorMars/lazy/nvim-treesitter/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/nvim-SeniorMars/lazy/nvim-treesitter/parser/vimdoc.so
- OK Parser: c          ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.2/nvim-linux64/lib/nvim/parser/c.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.2/nvim-linux64/lib/nvim/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.2/nvim-linux64/lib/nvim/parser/query.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.2/nvim-linux64/lib/nvim/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.2/nvim-linux64/lib/nvim/parser/vimdoc.so

--------
vimtex: health#vimtex#check

VimTeX ~
- OK Vim version should have full support!
- WARNING biber is not executable!
  - ADVICE:
    - Biber is often required so this may give unexpected problems.
- OK General viewer should work properly!
- ERROR |g:vimtex_compiler_method| (`latexmk`) is not executable!


---
layout: post
title: Maddison Configuration Health Check
toc: true
post_style: page
---

# nvim-Maddison Neovim health check

--------
lazy: require("lazy.health").check()

lazy.nvim ~
- OK Git installed
- OK no existing packages found by other package managers
- OK packer_compiled.lua not found
- WARNING {nvim-window-picker}: unknown key <lazymod>
- WARNING {vCoolor.vim}: unknown key <conf>

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
  - bash                x ✓ ✓ . ✓
  - c                   ✓ ✓ ✓ ✓ ✓
  - capnp               ✓ ✓ ✓ ✓ ✓
  - cmake               ✓ . ✓ ✓ .
  - comment             ✓ . . . .
  - css                 ✓ . ✓ ✓ ✓
  - dockerfile          ✓ . . . ✓
  - glsl                ✓ ✓ ✓ ✓ ✓
  - go                  ✓ ✓ ✓ ✓ ✓
  - gomod               ✓ . . . ✓
  - graphql             ✓ . . ✓ ✓
  - hjson               ✓ ✓ ✓ ✓ ✓
  - html                ✓ ✓ ✓ ✓ ✓
  - javascript          ✓ ✓ ✓ ✓ ✓
  - jsdoc               ✓ . . . .
  - json                ✓ ✓ ✓ ✓ .
  - json5               ✓ . . . ✓
  - jsonc               ✓ ✓ ✓ ✓ ✓
  - lua                 ✓ ✓ ✓ ✓ ✓
  - make                ✓ . ✓ . ✓
  - markdown            ✓ . ✓ ✓ ✓
  - prisma              ✓ . . . .
  - query               ✓ ✓ ✓ ✓ ✓
  - regex               ✓ . . . .
  - tsx                 ✓ ✓ ✓ ✓ ✓
  - typescript          ✓ ✓ ✓ ✓ ✓
  - vim                 ✓ ✓ ✓ . ✓
  - vimdoc              ✓ . . . ✓
  - yaml                ✓ ✓ ✓ ✓ ✓

  Legend: H[ighlight], L[ocals], F[olds], I[ndents], In[j]ections
         +) multiple parsers found, only one will be used
         x) errors found in the query, try to run :TSUpdate {lang} ~

The following errors have been detected: ~
- ERROR bash(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 242 for language bash
  bash(highlights) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/queries/bash/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 242 for language bash

--------
ouroboros: require("ouroboros.health").check()

Required Dependencies ~
- OK plenary installed.

--------
provider: health#provider#check

- ERROR Failed to run healthcheck for "provider" plugin. Exception:
  command line..function health#check[25]..health#provider#check[4]..<SNR>116_check_ruby[38]..<SNR>116_system, line 11
  Vim(let):E475: Invalid value for argument cmd: '1' is not executable

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
- Log path: /home/ronnie/.local/state/nvim-Maddison/lsp.log
- Log size: 0 KB

vim.lsp: Active Clients ~
- No active clients

--------
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: bash       ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/bash.so
- OK Parser: c          ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/c.so
- OK Parser: capnp      ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/capnp.so
- OK Parser: cmake      ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/cmake.so
- OK Parser: comment    ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/comment.so
- OK Parser: css        ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/css.so
- OK Parser: dockerfile ABI: 13, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/dockerfile.so
- OK Parser: glsl       ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/glsl.so
- OK Parser: go         ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/go.so
- OK Parser: gomod      ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/gomod.so
- OK Parser: graphql    ABI: 13, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/graphql.so
- OK Parser: hjson      ABI: 13, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/hjson.so
- OK Parser: html       ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/html.so
- OK Parser: javascript ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/javascript.so
- OK Parser: jsdoc      ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/jsdoc.so
- OK Parser: json       ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/json.so
- OK Parser: json5      ABI: 13, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/json5.so
- OK Parser: jsonc      ABI: 13, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/jsonc.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/lua.so
- OK Parser: make       ABI: 13, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/make.so
- OK Parser: markdown   ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/markdown.so
- OK Parser: prisma     ABI: 13, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/prisma.so
- OK Parser: regex      ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/regex.so
- OK Parser: tsx        ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/tsx.so
- OK Parser: typescript ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/typescript.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/vimdoc.so
- OK Parser: yaml       ABI: 13, path: /home/ronnie/.local/share/nvim-Maddison/lazy/nvim-treesitter/parser/yaml.so
- OK Parser: c          ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/c.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/query.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vimdoc.so

--------
which-key: require("which-key.health").check()

WhichKey: checking conflicting keymaps ~
- OK No conflicting keymaps found

--------
zf-native: require("zf-native.health").check()

Installation ~
- libzf library path: /home/ronnie/.local/share/nvim-Maddison/lazy/telescope-zf-native.nvim/lua/../lib/libzf-linux-x64.so
- OK libzf path is valid

Configuration
  - zf telescope file sorter enabled
    - highlights: true
    - filename score priority: true
  - zf telescope generic sorter enabled
    - highlights: true
    - filename score priority: false ~


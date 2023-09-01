---
layout: post
title: Lazyman Configuration Health Check
toc: true
post_style: page
---

# nvim-Charles Neovim health check

==============================================================================
lazy: require("lazy.health").check()

lazy.nvim ~
- OK Git installed
- OK no existing packages found by other package managers
- OK packer_compiled.lua not found

==============================================================================
mkdp: health#mkdp#check

- Platform: linux
- Nvim Version: NVIM v0.9.1
- Pre build: /home/ronnie/.local/share/nvim-Charles/site/lazy/markdown-preview.nvim/app/bin/markdown-preview-linux
- Pre build version: 0.0.10
- OK Using pre build

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
  - bash                x ✓ ✓ . x
  - c                   x ✓ ✓ ✓ ✓
  - cpp                 x ✓ ✓ ✓ ✓
  - css                 ✓ . ✓ ✓ ✓
  - gitignore           ✓ . . . .
  - html                ✓ ✓ ✓ ✓ ✓
  - javascript          ✓ ✓ ✓ ✓ ✓
  - json                ✓ ✓ ✓ ✓ .
  - latex               ✓ . ✓ . ✓
  - lua                 ✓ ✓ ✓ ✓ ✓
  - make                ✓ . ✓ . ✓
  - markdown            ✓ . ✓ ✓ ✓
  - markdown_inline     ✓ . . . ✓
  - python              x ✓ ✓ ✓ ✓
  - query               ✓ ✓ ✓ ✓ ✓
  - regex               ✓ . . . .
  - rust                ✓ ✓ ✓ ✓ ✓
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
- ERROR bash(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 242 for language bash
  bash(highlights) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/queries/bash/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 242 for language bash
- ERROR bash(injections): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 195 for language bash
  bash(injections) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/queries/bash/injections.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 195 for language bash
- ERROR c(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 318 for language c
  c(highlights) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/queries/c/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 318 for language c
- ERROR cpp(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 2028 for language cpp
  cpp(highlights) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/queries/c/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 2028 for language cpp
  |    [OK]:"/home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/queries/cpp/highlights.scm"
- ERROR python(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 727 for language python
  python(highlights) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/queries/python/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 727 for language python

==============================================================================
provider: health#provider#check

- ERROR Failed to run healthcheck for "provider" plugin. Exception:
  command line..function health#check[25]..health#provider#check[4]..<SNR>75_check_ruby[38]..<SNR>75_system, line 11
  Vim(let):E475: Invalid value for argument cmd: '/home/ronnie/tools/ruby/bin/neovim-ruby-host' is not executable

==============================================================================
rainbow-delimiters: require("rainbow-delimiters.health").check()

Custom strategies ~
- OK Valid custom default strategy.
- OK Valid custom strategy for 'vimdoc'.
- OK Valid custom strategy for 'cpp'.
- OK Valid custom strategy for 'lua'.
- OK Valid custom strategy for 'vim'.
- OK Valid custom strategy for 'c'.

Custom queries ~

Custom highlight groups ~
- OK Highlight group 'RainbowDelimiterRed' defined.
- OK Highlight group 'RainbowDelimiterOrange' defined.
- OK Highlight group 'RainbowDelimiterYellow' defined.
- OK Highlight group 'RainbowDelimiterGreen' defined.
- OK Highlight group 'RainbowDelimiterBlue' defined.
- OK Highlight group 'RainbowDelimiterCyan' defined.
- OK Highlight group 'RainbowDelimiterViolet' defined.

==============================================================================
vim.lsp: require("vim.lsp.health").check()

- LSP log level : WARN
- Log path: /home/ronnie/.local/state/nvim-Charles/lsp.log
- Log size: 0 KB

vim.lsp: Active Clients ~
- No active clients

==============================================================================
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: bash       ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/bash.so
- OK Parser: c          ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/c.so
- OK Parser: cpp        ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/cpp.so
- OK Parser: css        ABI: 13, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/css.so
- OK Parser: gitignore  ABI: 13, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/gitignore.so
- OK Parser: html       ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/html.so
- OK Parser: javascript ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/javascript.so
- OK Parser: json       ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/json.so
- OK Parser: latex      ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/latex.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/lua.so
- OK Parser: make       ABI: 13, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/make.so
- OK Parser: markdown   ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/markdown.so
- OK Parser: markdown_inline ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/markdown_inline.so
- OK Parser: python     ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/python.so
- OK Parser: regex      ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/regex.so
- OK Parser: rust       ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/rust.so
- OK Parser: toml       ABI: 13, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/toml.so
- OK Parser: tsx        ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/tsx.so
- OK Parser: typescript ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/typescript.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/vimdoc.so
- OK Parser: yaml       ABI: 13, path: /home/ronnie/.local/share/nvim-Charles/site/lazy/nvim-treesitter/parser/yaml.so
- OK Parser: c          ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/c.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/query.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vimdoc.so


# nvim-Allaman Neovim health check

==============================================================================
core: require("core.health").check()

System configuration ~
- WARNING This config probably won't work very well with Neovim < 0.10
- OK Running on supported OS: Linux
- WARNING No or wrong (check :messages) user configuration provided (this is optional)
- OK 'fzf' executable found
- OK 'fd' executable found
- OK 'node' executable found
- OK 'rg' executable found
- OK 'cargo' executable found
- OK 'trash' executable found
- OK 'go' executable found
- OK 'tectonic' executable found
- WARNING 'skim' executable not found - to view compiled LaTex files (PDFs)
- OK 'sed' executable found

==============================================================================
lazy: require("lazy.health").check()

lazy.nvim ~
- OK Git installed
- OK no existing packages found by other package managers
- OK packer_compiled.lua not found
- WARNING {kustomize.nvim}: unknown key <requires>

==============================================================================
null-ls: require("null-ls.health").check()

- OK stylua: the command "stylua" is executable.
- OK eslint_d: the command "eslint_d" is executable.
- ERROR prettier: the command "prettier" is not executable.
- ERROR terraform_fmt: the command "terraform" is not executable.
- OK black: the command "black" is executable.
- OK goimports: the command "goimports" is executable.
- OK gofumpt: the command "gofumpt" is executable.
- ERROR latexindent: the command "latexindent" is not executable.
- ERROR shellcheck: the command "shellcheck" is not executable.
- OK gitsigns: the source "gitsigns" can be ran.
- ERROR shfmt: the command "shfmt" is not executable.
- OK ruff: the command "ruff" is executable.
- OK rustfmt: the command "rustfmt" is executable.

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
  - cmake               ✓ . ✓ ✓ .
  - css                 ✓ . ✓ ✓ ✓
  - dockerfile          ✓ . . . ✓
  - go                  ✓ ✓ ✓ ✓ ✓
  - hcl                 ✓ . ✓ ✓ ✓
  - html                ✓ ✓ ✓ ✓ ✓
  - java                ✓ ✓ ✓ ✓ ✓
  - json                ✓ ✓ ✓ ✓ .
  - kotlin              ✓ ✓ ✓ . ✓
  - ledger              ✓ . ✓ ✓ ✓
  - lua                 ✓ ✓ ✓ ✓ ✓
  - markdown            ✓ . ✓ ✓ ✓
  - markdown_inline     ✓ . . . ✓
  - python              ✓ ✓ ✓ ✓ ✓
  - query               ✓ ✓ ✓ ✓ ✓
  - regex               ✓ . . . .
  - rust                ✓ ✓ ✓ ✓ ✓
  - terraform           ✓ . ✓ ✓ ✓
  - toml                ✓ ✓ ✓ ✓ ✓
  - vim                 ✓ ✓ ✓ . ✓
  - vimdoc              ✓ . . . ✓

  Legend: H[ighlight], L[ocals], F[olds], I[ndents], In[j]ections
         +) multiple parsers found, only one will be used
         x) errors found in the query, try to run :TSUpdate {lang} ~

The following errors have been detected: ~
- ERROR c(highlights): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 242 for language c
  c(highlights) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/queries/c/highlights.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 242 for language c
- ERROR c(folds): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 249 for language c
  c(folds) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/queries/c/folds.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 249 for language c
- ERROR c(indents): ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1109 for language c
  c(indents) is concatenated from the following files:
  | [ERROR]:"/home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/queries/c/indents.scm", failed to load: ...-linux64/share/nvim/runtime/lua/vim/treesitter/query.lua:259: query: invalid node type at position 1109 for language c

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
- Log path: /home/ronnie/.local/state/nvim-Allaman/lsp.log
- Log size: 0 KB

vim.lsp: Active Clients ~
- No active clients

==============================================================================
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: bash       ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/bash.so
- OK Parser: cmake      ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/cmake.so
- OK Parser: css        ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/css.so
- OK Parser: dockerfile ABI: 13, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/dockerfile.so
- OK Parser: go         ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/go.so
- OK Parser: hcl        ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/hcl.so
- OK Parser: html       ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/html.so
- OK Parser: java       ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/java.so
- OK Parser: json       ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/json.so
- OK Parser: kotlin     ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/kotlin.so
- OK Parser: ledger     ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/ledger.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/lua.so
- OK Parser: markdown   ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/markdown.so
- OK Parser: markdown_inline ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/markdown_inline.so
- OK Parser: python     ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/python.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/query.so
- OK Parser: regex      ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/regex.so
- OK Parser: rust       ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/rust.so
- OK Parser: terraform  ABI: 14, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/terraform.so
- OK Parser: toml       ABI: 13, path: /home/ronnie/.local/share/nvim-Allaman/lazy/nvim-treesitter/parser/toml.so
- OK Parser: c          ABI: 13, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/c.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/query.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vimdoc.so

==============================================================================
vimtex: health#vimtex#check

VimTeX ~
- OK Vim version should have full support!
- WARNING bibtex is not executable!
  - ADVICE:
    - bibtex is required for cite completions.
- WARNING biber is not executable!
  - ADVICE:
    - Biber is often required so this may give unexpected problems.
- ERROR Skim is not installed!
- OK Compiler should work!

==============================================================================
which-key: require("which-key.health").check()

WhichKey: checking conflicting keymaps ~
- OK No conflicting keymaps found


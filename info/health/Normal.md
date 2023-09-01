---
layout: post
title: Lazyman Configuration Health Check
toc: true
post_style: page
---

# nvim-Normal Neovim health check

--------
base: require("base.health").check()

NormalNvim ~
- NormalNvim Version: unknown
- Neovim Version: v0.9.1
- OK Using stable Neovim >= 0.8.0
- OK `git` is installed: Used for core functionality such as updater and plugin management
- OK `node` is installed: Used for core functionality such as updater and plugin management
- ERROR `yarn` is not installed: Used for core functionality such as updater and plugin management.
- OK `cargo` is installed: Used by nvim-spectre to install oxi. Also by dooku.nvim to generate rust html docs.
- OK `rg` is installed: Used for nvim-spectre to find using ripgrep.
- OK `lazygit` is installed: Used for mappings to pull up git TUI (Optional)
- WARNING `gitui` is not installed: Used for mappings to pull up git TUI (Optional)
- WARNING `pynvim` is not installed: Used to enable ranger file browser (optional)
  NOTE: checkhealth won't detect this correctly, but you can ensure it is installed with 'pip list | grep pynvim'.
- OK `ranger` is installed: Used to enable ranger file browser (Optional)
- WARNING `delta` is not installed: Used by undotree to show a diff (Optional)
- WARNING `grcov` is not installed: Used to show code coverage (Optional)
- WARNING `grcov` is not installed: Used to show code coverage (Optional)
- WARNING `jest` is not installed: Used to run typescript and javascript tests (Optional)
- WARNING `pytest` is not installed: Used to run python tests (Optional)
- WARNING `cargo nextest` is not installed: Used to run rust tests (optional)
  NOTE: checkhealth won't detect this correctly, but you can confirm it works correctly with 'cargo nextest'.
- WARNING `nunit` is not installed: Used to run C# tests (optional)
  NOTE: There is no way to install this system wide. To use it you must add it to your dotnet C# project: 'dotnet add package NUnit NUnit3TestAdapter'.
- WARNING `csc` is not installed: Used by compiler.nvim to compile non dotnet C# files (Optional)
- WARNING `mono` is not installed: Used by compiler.nvim to run non dotnet C# files. (Optional)
- WARNING `dotnet` is not installed: Used by compiler.nvim and DAP to operate with dotnet projects (opitonal)
  NOTE: Make sure you also have the system package dotnet-sdk installed.
- OK `java` is installed: Used by compiler.nvim and dap to operate with java (Optional)
- OK `javac` is installed: Used by compiler.nvim to compile java (Optional)
- WARNING `nasm` is not installed: Used by compiler.nvim to compile assembly x86_64 (Optional)
- OK `gcc` is installed: Used by compiler.nvim to compile C (Optional)
- OK `g++` is installed: Used by compiler.nvim to compile C++ (Optional)
- WARNING `Rscript` is not installed: Used by compiler.nvim to interpretate R (Optional)
- WARNING `python` is not installed: Used by compiler.nvim to interpretate python (Optional)
- WARNING `nuitka3` is not installed: Used by compiler.nvim to compile python to machine code (Optional)
- WARNING `pyinstaller` is not installed: Used by compiler.nvim to compile python to bytecode (Optional)
- OK `ruby` is installed: Used by compiler.nvim to interpretate ruby (optional)
- OK `perl` is installed: Used by compiler.nvim to interpretate perl (optional)
- OK `go` is installed: Used by compiler.nvim to compile go (optional)
- WARNING `godoc` is not installed: Used by dooku.nvim to generate go html docs
  NOTE: If you have it installed but you can run it on the terminal, ensure you have added 'go' to your OS path (optional)
- WARNING `doxygen` is not installed: Used by dooku.nvim to generate c/c++/python/java html docs (optional)
- 
- Write `:bw` to close `:checkhealth` gracefuly.

--------
lazy: require("lazy.health").check()

lazy.nvim ~
- OK Git installed
- OK no existing packages found by other package managers
- OK packer_compiled.lua not found
- WARNING {nvim-coverage}: unknown key <requires>
- WARNING {nvim-neoclip.lua}: unknown key <requires>

--------
mkdp: health#mkdp#check

- Platform: linux
- Nvim Version: NVIM v0.9.1
- Node version: v18.16.0

- Script: /home/ronnie/.local/share/nvim-Normal/lazy/markdown-preview.nvim/app/server.js
- Script exists: 1
- OK Using node

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
vim.lsp: require("vim.lsp.health").check()

- LSP log level : WARN
- Log path: /home/ronnie/.local/state/nvim-Normal/lsp.log
- Log size: 0 KB

vim.lsp: Active Clients ~
- No active clients

--------
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: c          ABI: 13, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/c.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/query.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vimdoc.so


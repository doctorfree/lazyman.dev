---
layout: post
title: Jdhao Configuration Health Check
toc: true
post_style: page
---

# nvim-Jdhao Neovim health check

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
- Disabled (g:loaded_node_provider=0).

Perl provider (optional) ~
- Disabled (g:loaded_perl_provider=0).

--------
vim.lsp: require("vim.lsp.health").check()

- LSP log level : WARN
- Log path: /home/ronnie/.local/state/nvim-Jdhao/lsp.log
- Log size: 0 KB

vim.lsp: Active Clients ~
- No active clients

--------
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: c          ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.2/nvim-linux64/lib/nvim/parser/c.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.2/nvim-linux64/lib/nvim/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.2/nvim-linux64/lib/nvim/parser/query.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.2/nvim-linux64/lib/nvim/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.2/nvim-linux64/lib/nvim/parser/vimdoc.so


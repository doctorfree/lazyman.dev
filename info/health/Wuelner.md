# nvim-Wuelner Neovim health check

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
- Disabled (g:loaded_ruby_provider=0).

Node.js provider (optional) ~
- Disabled (g:loaded_node_provider=0).

Perl provider (optional) ~
- Disabled (g:loaded_perl_provider=0).

==============================================================================
vim.lsp: require("vim.lsp.health").check()

- LSP log level : WARN
- Log path: /home/ronnie/.local/state/nvim-Wuelner/lsp.log
- Log size: 0 KB

vim.lsp: Active Clients ~
- No active clients

==============================================================================
vim.treesitter: require("vim.treesitter.health").check()

- Nvim runtime ABI version: 14
- OK Parser: c          ABI: 13, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/c.so
- OK Parser: lua        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/lua.so
- OK Parser: query      ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/query.so
- OK Parser: vim        ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vim.so
- OK Parser: vimdoc     ABI: 14, path: /home/ronnie/.local/share/bob/v0.9.1/nvim-linux64/lib/nvim/parser/vimdoc.so


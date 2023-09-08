---
layout: post
title: Lazyman Configuration Info
toc: true
post_style: page
---

# Lazyman Neovim Configuration Information

The Lazyman Neovim configuration serves as a reference implementation of a configuration with multiple namespaces and managed via a command line menu interface. Currently the Lazyman Neovim configuration provides three separate and distinct namespaces ('ecovim', 'free' and 'onno'). To switch between namespaces, set the 'namespace' value in 'lua/configuration.lua'.

- Install and initialize: **`Installed and initialized by default`**
- Configuration category: [Default](https://lazyman.dev/features)
- Base configuration:     Custom
- Plugin manager:         [Lazy](https://github.com/folke/lazy.nvim)
- Installation location:  **`~/.config/nvim-Lazyman`**

## Git repository

[https://github.com/doctorfree/nvim-lazyman](https://github.com/doctorfree/nvim-lazyman)

## Neovimcraft entry

[http://neovimcraft.com/plugin/doctorfree/nvim-lazyman](http://neovimcraft.com/plugin/doctorfree/nvim-lazyman)

## Dotfyle entry

[https://dotfyle.com/doctorfree/nvim-lazyman](https://dotfyle.com/doctorfree/nvim-lazyman)

## Website

[https://lazyman.dev](https://lazyman.dev)

## YouTube channel

[https://www.youtube.com/@doctorfree](https://www.youtube.com/@doctorfree)

|  Jump  |   to   | Keymaps |
| :----: | :----: | :-----: |
| [Normal mode keymaps](#normal-mode-keymaps) | [Visual mode keymaps](#visual-mode-keymaps) | [Operator mode keymaps](#operator-mode-keymaps) |

## Lazy managed plugins

- [numToStr/Comment.nvim](https://github.com/numToStr/Comment.nvim)
- [antoinemadec/FixCursorHold.nvim](https://github.com/antoinemadec/FixCursorHold.nvim)
- [L3MON4D3/LuaSnip](https://github.com/L3MON4D3/LuaSnip)
- [goolord/alpha-nvim](https://github.com/goolord/alpha-nvim)
- [utilyre/barbecue.nvim](https://github.com/utilyre/barbecue.nvim.git)
- [alanfortlink/blackjack.nvim](https://github.com/alanfortlink/blackjack.nvim)
- [akinsho/bufferline.nvim](https://github.com/akinsho/bufferline.nvim)
- [catppuccin/nvim](https://github.com/catppuccin/nvim)
- [eandrju/cellular-automaton.nvim](https://github.com/eandrju/cellular-automaton.nvim)
- [doctorfree/cheatsheet.nvim](https://github.com/doctorfree/cheatsheet.nvim)
- [hrsh7th/cmp-buffer](https://github.com/hrsh7th/cmp-buffer)
- [hrsh7th/cmp-calc](https://github.com/hrsh7th/cmp-calc)
- [hrsh7th/cmp-cmdline](https://github.com/hrsh7th/cmp-cmdline)
- [David-Kunz/cmp-npm](https://github.com/David-Kunz/cmp-npm)
- [hrsh7th/cmp-nvim-lsp](https://github.com/hrsh7th/cmp-nvim-lsp)
- [hrsh7th/cmp-nvim-lua](https://github.com/hrsh7th/cmp-nvim-lua)
- [hrsh7th/cmp-path](https://github.com/hrsh7th/cmp-path)
- [js-everts/cmp-tailwind-colors](https://github.com/js-everts/cmp-tailwind-colors.git)
- [saadparwaiz1/cmp_luasnip](https://github.com/saadparwaiz1/cmp_luasnip)
- [LudoPinelli/comment-box.nvim](https://github.com/LudoPinelli/comment-box.nvim.git)
- [sindrets/diffview.nvim](https://github.com/sindrets/diffview.nvim.git)
- [Mofiqul/dracula.nvim](https://github.com/Mofiqul/dracula.nvim)
- [stevearc/dressing.nvim](https://github.com/stevearc/dressing.nvim)
- [tamton-aquib/duck.nvim](https://github.com/tamton-aquib/duck.nvim.git)
- [neanias/everforest-nvim](https://github.com/neanias/everforest-nvim)
- [folke/flash.nvim](https://github.com/folke/flash.nvim.git)
- [tamton-aquib/flirt.nvim](https://github.com/tamton-aquib/flirt.nvim.git)
- [rafamadriz/friendly-snippets](https://github.com/rafamadriz/friendly-snippets)
- [nvimdev/galaxyline.nvim](https://github.com/nvimdev/galaxyline.nvim.git)
- [akinsho/git-conflict.nvim](https://github.com/akinsho/git-conflict.nvim.git)
- [ThePrimeagen/git-worktree.nvim](https://github.com/ThePrimeagen/git-worktree.nvim.git)
- [lewis6991/gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim)
- [dnlhc/glance.nvim](https://github.com/dnlhc/glance.nvim.git)
- [letieu/hacker.nvim](https://github.com/letieu/hacker.nvim)
- [smoka7/hydra.nvim](https://github.com/smoka7/hydra.nvim.git)
- [lukas-reineke/indent-blankline.nvim](https://github.com/lukas-reineke/indent-blankline.nvim)
- [rebelot/kanagawa.nvim](https://github.com/rebelot/kanagawa.nvim)
- [folke/lazy.nvim](https://github.com/folke/lazy.nvim)
- [kdheepak/lazygit.nvim](https://github.com/kdheepak/lazygit.nvim.git)
- [onsails/lspkind-nvim](https://github.com/onsails/lspkind-nvim)
- [iamcco/markdown-preview.nvim](https://github.com/iamcco/markdown-preview.nvim)
- [williamboman/mason-lspconfig.nvim](https://github.com/williamboman/mason-lspconfig.nvim)
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim)
- [echasnovski/mini.ai](https://github.com/echasnovski/mini.ai.git)
- [echasnovski/mini.align](https://github.com/echasnovski/mini.align.git)
- [echasnovski/mini.animate](https://github.com/echasnovski/mini.animate.git)
- [echasnovski/mini.bufremove](https://github.com/echasnovski/mini.bufremove.git)
- [loctvl842/monokai-pro.nvim](https://github.com/loctvl842/monokai-pro.nvim)
- [smoka7/multicursors.nvim](https://github.com/smoka7/multicursors.nvim.git)
- [karb94/neoscroll.nvim](https://github.com/karb94/neoscroll.nvim)
- [nvim-neotest/neotest](https://github.com/nvim-neotest/neotest)
- [haydenmeade/neotest-jest](https://github.com/haydenmeade/neotest-jest.git)
- [Shatur/neovim-session-manager](https://github.com/Shatur/neovim-session-manager)
- [EdenEast/nightfox.nvim](https://github.com/EdenEast/nightfox.nvim)
- [folke/noice.nvim](https://github.com/folke/noice.nvim)
- [MunifTanjim/nui.nvim](https://github.com/MunifTanjim/nui.nvim)
- [nacro90/numb.nvim](https://github.com/nacro90/numb.nvim.git)
- [windwp/nvim-autopairs](https://github.com/windwp/nvim-autopairs)
- [hrsh7th/nvim-cmp](https://github.com/hrsh7th/nvim-cmp)
- [norcalli/nvim-colorizer.lua](https://github.com/norcalli/nvim-colorizer.lua)
- [andythigpen/nvim-coverage](https://github.com/andythigpen/nvim-coverage.git)
- [jay-babu/mason-nvim-dap.nvim](https://github.com/jay-babu/mason-nvim-dap.nvim)
- [LiadOz/nvim-dap-repl-highlights](https://github.com/LiadOz/nvim-dap-repl-highlights.git)
- [rcarriga/nvim-dap-ui](https://github.com/rcarriga/nvim-dap-ui)
- [theHamsta/nvim-dap-virtual-text](https://github.com/theHamsta/nvim-dap-virtual-text)
- [mxsdev/nvim-dap-vscode-js](https://github.com/mxsdev/nvim-dap-vscode-js.git)
- [antosha417/nvim-lsp-file-operations](https://github.com/antosha417/nvim-lsp-file-operations)
- [neovim/nvim-lspconfig](https://github.com/neovim/nvim-lspconfig)
- [SmiteshP/nvim-navic](https://github.com/SmiteshP/nvim-navic)
- [rcarriga/nvim-notify](https://github.com/rcarriga/nvim-notify)
- [nvim-pack/nvim-spectre](https://github.com/nvim-pack/nvim-spectre.git)
- [kylechui/nvim-surround](https://github.com/kylechui/nvim-surround)
- [akinsho/nvim-toggleterm.lua](https://github.com/akinsho/nvim-toggleterm.lua)
- [kyazdani42/nvim-tree.lua](https://github.com/kyazdani42/nvim-tree.lua)
- [nvim-treesitter/nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
- [nvim-treesitter/nvim-treesitter-textobjects](https://github.com/nvim-treesitter/nvim-treesitter-textobjects)
- [RRethy/nvim-treesitter-textsubjects](https://github.com/RRethy/nvim-treesitter-textsubjects.git)
- [JoosepAlviste/nvim-ts-context-commentstring](https://github.com/JoosepAlviste/nvim-ts-context-commentstring)
- [sam4llis/nvim-tundra](https://github.com/sam4llis/nvim-tundra)
- [kevinhwang91/nvim-ufo](https://github.com/kevinhwang91/nvim-ufo)
- [kyazdani42/nvim-web-devicons](https://github.com/kyazdani42/nvim-web-devicons)
- [olimorris/onedarkpro.nvim](https://github.com/olimorris/onedarkpro.nvim)
- [vuki656/package-info.nvim](https://github.com/vuki656/package-info.nvim.git)
- [nvim-lua/plenary.nvim](https://github.com/nvim-lua/plenary.nvim)
- [nvim-lua/popup.nvim](https://github.com/nvim-lua/popup.nvim)
- [rareitems/printer.nvim](https://github.com/rareitems/printer.nvim.git)
- [kevinhwang91/promise-async](https://github.com/kevinhwang91/promise-async)
- [hiphish/rainbow-delimiters.nvim](https://github.com/hiphish/rainbow-delimiters.nvim.git)
- [sunjon/shade.nvim](https://github.com/sunjon/shade.nvim)
- [gbprod/stay-in-place.nvim](https://github.com/gbprod/stay-in-place.nvim.git)
- [jim-fx/sudoku.nvim](https://github.com/jim-fx/sudoku.nvim)
- [AndrewRadev/switch.vim](https://github.com/AndrewRadev/switch.vim.git)
- [razak17/tailwind-fold.nvim](https://github.com/razak17/tailwind-fold.nvim.git)
- [nvim-telescope/telescope-fzf-native.nvim](https://github.com/nvim-telescope/telescope-fzf-native.nvim)
- [cljoly/telescope-repo.nvim](https://github.com/cljoly/telescope-repo.nvim)
- [nvim-telescope/telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)
- [axelvc/template-string.nvim](https://github.com/axelvc/template-string.nvim.git)
- [rebelot/terminal.nvim](https://github.com/rebelot/terminal.nvim)
- [folke/todo-comments.nvim](https://github.com/folke/todo-comments.nvim)
- [folke/tokyonight.nvim](https://github.com/folke/tokyonight.nvim)
- [Wansmer/treesj](https://github.com/Wansmer/treesj)
- [folke/trouble.nvim](https://github.com/folke/trouble.nvim)
- [dmmulroy/tsc.nvim](https://github.com/dmmulroy/tsc.nvim)
- [folke/twilight.nvim](https://github.com/folke/twilight.nvim)
- [pmizio/typescript-tools.nvim](https://github.com/pmizio/typescript-tools.nvim.git)
- [ThePrimeagen/vim-be-good](https://github.com/ThePrimeagen/vim-be-good)
- [tpope/vim-repeat](https://github.com/tpope/vim-repeat)
- [airblade/vim-rooter](https://github.com/airblade/vim-rooter)
- [tpope/vim-speeddating](https://github.com/tpope/vim-speeddating.git)
- [dhruvasagar/vim-table-mode](https://github.com/dhruvasagar/vim-table-mode.git)
- [wakatime/vim-wakatime](https://github.com/wakatime/vim-wakatime.git)
- [folke/which-key.nvim](https://github.com/folke/which-key.nvim)
- [folke/zen-mode.nvim](https://github.com/folke/zen-mode.nvim)

## Lazyman Keymaps

### Normal mode keymaps

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Tab&gt;</pre> |
| **Right hand side** | <pre>:BufferLineCycleNext&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;CR&gt;</pre> |
| **Right hand side** | <pre>:noh&lt;CR&gt;&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>%</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(MatchitNormalForward)</pre> |

| **Description** | Nvim builtin |
| :---- | :---- |
| **Left hand side** | <pre>&</pre> |
| **Right hand side** | <pre>:&&&lt;CR&gt;</pre> |

| **Description** | Previous Tab |
| :---- | :---- |
| **Left hand side** | <pre>,&lt;Tab&gt;[</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;tabprevious&lt;CR&gt;</pre> |

| **Description** | Close Tab |
| :---- | :---- |
| **Left hand side** | <pre>,&lt;Tab&gt;d</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;tabclose&lt;CR&gt;</pre> |

| **Description** | Next Tab |
| :---- | :---- |
| **Left hand side** | <pre>,&lt;Tab&gt;]</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;tabnext&lt;CR&gt;</pre> |

| **Description** | New Tab |
| :---- | :---- |
| **Left hand side** | <pre>,&lt;Tab&gt;&lt;Tab&gt;</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;tabnew&lt;CR&gt;</pre> |

| **Description** | First Tab |
| :---- | :---- |
| **Left hand side** | <pre>,&lt;Tab&gt;f</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;tabfirst&lt;CR&gt;</pre> |

| **Description** | Last Tab |
| :---- | :---- |
| **Left hand side** | <pre>,&lt;Tab&gt;l</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;tablast&lt;CR&gt;</pre> |

| **Description** | Split window right |
| :---- | :---- |
| **Left hand side** | <pre>,&#124;</pre> |
| **Right hand side** | <pre>&lt;C-W&gt;v</pre> |

| **Description** | Split window below |
| :---- | :---- |
| **Left hand side** | <pre>,-</pre> |
| **Right hand side** | <pre>&lt;C-W&gt;s</pre> |

| **Description** | Split window right |
| :---- | :---- |
| **Left hand side** | <pre>,w&#124;</pre> |
| **Right hand side** | <pre>&lt;C-W&gt;v</pre> |

| **Description** | Split window below |
| :---- | :---- |
| **Left hand side** | <pre>,w-</pre> |
| **Right hand side** | <pre>&lt;C-W&gt;s</pre> |

| **Description** | Delete window |
| :---- | :---- |
| **Left hand side** | <pre>,wd</pre> |
| **Right hand side** | <pre>&lt;C-W&gt;c</pre> |

| **Description** | Other window |
| :---- | :---- |
| **Left hand side** | <pre>,ww</pre> |
| **Right hand side** | <pre>&lt;C-W&gt;p</pre> |

| **Description** | Terminal (cwd) |
| :---- | :---- |
| **Left hand side** | <pre>,fT</pre> |
| **Right hand side** | |

| **Description** | Terminal (root dir) |
| :---- | :---- |
| **Left hand side** | <pre>,ft</pre> |
| **Right hand side** | |

| **Description** | Inspect Pos |
| :---- | :---- |
| **Left hand side** | <pre>,ui</pre> |
| **Right hand side** | |

| **Description** | Toggle number |
| :---- | :---- |
| **Left hand side** | <pre>,uN</pre> |
| **Right hand side** | |

| **Description** | Toggle mouse |
| :---- | :---- |
| **Left hand side** | <pre>,um</pre> |
| **Right hand side** | |

| **Description** | Toggle statusline |
| :---- | :---- |
| **Left hand side** | <pre>,uS</pre> |
| **Right hand side** | |

| **Description** | Toggle tabline |
| :---- | :---- |
| **Left hand side** | <pre>,uT</pre> |
| **Right hand side** | |

| **Description** | Toggle signcolumn |
| :---- | :---- |
| **Left hand side** | <pre>,ug</pre> |
| **Right hand side** | |

| **Description** | Toggle Conceal |
| :---- | :---- |
| **Left hand side** | <pre>,uc</pre> |
| **Right hand side** | |

| **Description** | Toggle Line Numbers |
| :---- | :---- |
| **Left hand side** | <pre>,ul</pre> |
| **Right hand side** | |

| **Description** | Toggle Word Wrap |
| :---- | :---- |
| **Left hand side** | <pre>,uw</pre> |
| **Right hand side** | |

| **Description** | Toggle Spelling |
| :---- | :---- |
| **Left hand side** | <pre>,us</pre> |
| **Right hand side** | |

| **Description** | Toggle format on Save |
| :---- | :---- |
| **Left hand side** | <pre>,uf</pre> |
| **Right hand side** | |

| **Description** | Toggle barbecue winbar |
| :---- | :---- |
| **Left hand side** | <pre>,ub</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,cl</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua vim.diagnostic.open_float({ border = 'rounded', max_width = 100 })&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,cf</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua vim.lsp.buf.format({ async = true })&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,cr</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua vim.lsp.buf.rename()&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,ca</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua vim.lsp.buf.code_action()&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,q</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua require('ecovim.utils').toggle_quicklist()&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,.</pre> |
| **Right hand side** | <pre>:cn&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,,</pre> |
| **Right hand side** | <pre>:cp&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,pw</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua require('telescope.builtin').grep_string({ initial_mode = 'normal' })&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,pf</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua require('ecovim.plugins.telescope').project_files({ default_text = vim.fn.expand('&lt;lt&gt;cword&gt;'), initial_mode = 'normal' })&lt;CR&gt;</pre> |

| **Description** | Asciiville |
| :---- | :---- |
| **Left hand side** | <pre>,av</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;Asciiville&lt;CR&gt;</pre> |

| **Description** | Lazyman plugins |
| :---- | :---- |
| **Left hand side** | <pre>,lp</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;Lazyplug&lt;CR&gt;</pre> |

| **Description** | Lazyman configuration |
| :---- | :---- |
| **Left hand side** | <pre>,lc</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;Lazyconf&lt;CR&gt;</pre> |

| **Description** | Lazyman menu |
| :---- | :---- |
| **Left hand side** | <pre>,lm</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;Lazyman&lt;CR&gt;</pre> |

| **Description** | Htop command |
| :---- | :---- |
| **Left hand side** | <pre>,H</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;Htop&lt;CR&gt;</pre> |

| **Description** | Toggle colorcolumn |
| :---- | :---- |
| **Left hand side** | <pre>,C</pre> |
| **Right hand side** | |

| **Description** | Lazyman Keymaps |
| :---- | :---- |
| **Left hand side** | <pre>,hk</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;help Lazyman-Keymaps&lt;CR&gt;</pre> |

| **Description** | Nvims Help |
| :---- | :---- |
| **Left hand side** | <pre>,hn</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;help Nvims&lt;CR&gt;</pre> |

| **Description** | Lazyman Help |
| :---- | :---- |
| **Left hand side** | <pre>,hl</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;help Lazyman&lt;CR&gt;</pre> |

| **Description** | Options |
| :---- | :---- |
| **Left hand side** | <pre>,o</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;options&lt;CR&gt;</pre> |

| **Description** | Lazy Update |
| :---- | :---- |
| **Left hand side** | <pre>,U</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;Lazy update&lt;CR&gt;</pre> |

| **Description** | Lazy Menu |
| :---- | :---- |
| **Left hand side** | <pre>,L</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;Lazy&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,/l</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;:Lazy&lt;CR&gt;</pre> |

| **Description** | choose theirs |
| :---- | :---- |
| **Left hand side** | <pre>,gct</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;GitConflictChooseTheirs&lt;CR&gt;</pre> |

| **Description** | move to prev conflict |
| :---- | :---- |
| **Left hand side** | <pre>,gcp</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;GitConflictPrevConflict&lt;CR&gt;</pre> |

| **Description** | choose ours |
| :---- | :---- |
| **Left hand side** | <pre>,gco</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;GitConflictChooseOurs&lt;CR&gt;</pre> |

| **Description** | move to next conflict |
| :---- | :---- |
| **Left hand side** | <pre>,gcn</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;GitConflictNextConflict&lt;CR&gt;</pre> |

| **Description** | choose both |
| :---- | :---- |
| **Left hand side** | <pre>,gcb</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;GitConflictChooseBoth&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,gwc</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua require('telescope').extensions.git_worktree.create_git_worktree()&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,gww</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua require('telescope').extensions.git_worktree.git_worktrees()&lt;CR&gt;</pre> |

| **Description** | load last session |
| :---- | :---- |
| **Left hand side** | <pre>,/sl</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;SessionManager load_last_session&lt;CR&gt;</pre> |

| **Description** | load current dir session |
| :---- | :---- |
| **Left hand side** | <pre>,/sd</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;SessionManager load_current_dir_session&lt;CR&gt;</pre> |

| **Description** | remove session |
| :---- | :---- |
| **Left hand side** | <pre>,/sr</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;SessionManager delete_session&lt;CR&gt;</pre> |

| **Description** | choose session |
| :---- | :---- |
| **Left hand side** | <pre>,/sc</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;SessionManager load_session&lt;CR&gt;</pre> |

| **Description** | save session |
| :---- | :---- |
| **Left hand side** | <pre>,/ss</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;SessionManager save_current_session&lt;CR&gt;</pre> |

| **Description** | terminal float |
| :---- | :---- |
| **Left hand side** | <pre>,at</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;ToggleTerm direction=float&lt;CR&gt;</pre> |

| **Description** | comment box |
| :---- | :---- |
| **Left hand side** | <pre>,ac</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua require('comment-box').lbox()&lt;CR&gt;</pre> |

| **Description** | Mason |
| :---- | :---- |
| **Left hand side** | <pre>,cm</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;Mason&lt;CR&gt;</pre> |

| **Description** | Move Float |
| :---- | :---- |
| **Left hand side** | <pre>,tf</pre> |
| **Right hand side** | |

| **Description** | Move Bottom Right New |
| :---- | :---- |
| **Left hand side** | <pre>,tH</pre> |
| **Right hand side** | |

| **Description** | Move Below Right New |
| :---- | :---- |
| **Left hand side** | <pre>,th</pre> |
| **Right hand side** | |

| **Description** | Move Bottom Right |
| :---- | :---- |
| **Left hand side** | <pre>,tL</pre> |
| **Right hand side** | |

| **Description** | Move Below Right |
| :---- | :---- |
| **Left hand side** | <pre>,tl</pre> |
| **Right hand side** | |

| **Description** | Terminal Prev |
| :---- | :---- |
| **Left hand side** | <pre>,t[</pre> |
| **Right hand side** | |

| **Description** | Terminal Next |
| :---- | :---- |
| **Left hand side** | <pre>,t]</pre> |
| **Right hand side** | |

| **Description** | Terminal Kill |
| :---- | :---- |
| **Left hand side** | <pre>,tk</pre> |
| **Right hand side** | |

| **Description** | New Terminal Run |
| :---- | :---- |
| **Left hand side** | <pre>,tR</pre> |
| **Right hand side** | |

| **Description** | Terminal Run |
| :---- | :---- |
| **Left hand side** | <pre>,tr</pre> |
| **Right hand side** | |

| **Description** | New Terminal Toggle |
| :---- | :---- |
| **Left hand side** | <pre>,tO</pre> |
| **Right hand side** | |

| **Description** | Terminal Toggle |
| :---- | :---- |
| **Left hand side** | <pre>,to</pre> |
| **Right hand side** | |

| **Description** | Terminal Send |
| :---- | :---- |
| **Left hand side** | <pre>,ts</pre> |
| **Right hand side** | |

| **Description** | Toggle Transparency |
| :---- | :---- |
| **Left hand side** | <pre>,ut</pre> |
| **Right hand side** | |

| **Description** | Select Moonokai pro filter |
| :---- | :---- |
| **Left hand side** | <pre>,up</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;MonokaiProSelect&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,DK</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,Dk</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,Dt</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,Dh</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,Dg</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,Ds</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,Dd</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,Dc</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,Di</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,Da</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,DA</pre> |
| **Right hand side** | |

| **Description** | Move next |
| :---- | :---- |
| **Left hand side** | <pre>,bn</pre> |
| **Right hand side** | |

| **Description** | Pick Buffer |
| :---- | :---- |
| **Left hand side** | <pre>,bp</pre> |
| **Right hand side** | |

| **Description** | Pin/Unpin Buffer |
| :---- | :---- |
| **Left hand side** | <pre>,bP</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 1 |
| :---- | :---- |
| **Left hand side** | <pre>,1</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 2 |
| :---- | :---- |
| **Left hand side** | <pre>,2</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 3 |
| :---- | :---- |
| **Left hand side** | <pre>,3</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 4 |
| :---- | :---- |
| **Left hand side** | <pre>,4</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 5 |
| :---- | :---- |
| **Left hand side** | <pre>,5</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 6 |
| :---- | :---- |
| **Left hand side** | <pre>,6</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 7 |
| :---- | :---- |
| **Left hand side** | <pre>,7</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 8 |
| :---- | :---- |
| **Left hand side** | <pre>,8</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 9 |
| :---- | :---- |
| **Left hand side** | <pre>,9</pre> |
| **Right hand side** | |

| **Description** | Close Right |
| :---- | :---- |
| **Left hand side** | <pre>,br</pre> |
| **Right hand side** | |

| **Description** | Close Left |
| :---- | :---- |
| **Left hand side** | <pre>,bl</pre> |
| **Right hand side** | |

| **Description** | Move back |
| :---- | :---- |
| **Left hand side** | <pre>,bb</pre> |
| **Right hand side** | |

| **Description** | Sort by directory |
| :---- | :---- |
| **Left hand side** | <pre>,bsd</pre> |
| **Right hand side** | |

| **Description** | Sort by extension |
| :---- | :---- |
| **Left hand side** | <pre>,bse</pre> |
| **Right hand side** | |

| **Description** | Sort by relative dir |
| :---- | :---- |
| **Left hand side** | <pre>,bsr</pre> |
| **Right hand side** | |

| **Description** | stage hunk |
| :---- | :---- |
| **Left hand side** | <pre>,ghs</pre> |
| **Right hand side** | |

| **Description** | reset hunk |
| :---- | :---- |
| **Left hand side** | <pre>,ghr</pre> |
| **Right hand side** | |

| **Description** | reset buffer |
| :---- | :---- |
| **Left hand side** | <pre>,ghR</pre> |
| **Right hand side** | |

| **Description** | preview |
| :---- | :---- |
| **Left hand side** | <pre>,ghp</pre> |
| **Right hand side** | |

| **Description** | diff hunk |
| :---- | :---- |
| **Left hand side** | <pre>,ghd</pre> |
| **Right hand side** | |

| **Description** | undo stage |
| :---- | :---- |
| **Left hand side** | <pre>,ghu</pre> |
| **Right hand side** | |

| **Description** | toggle deleted |
| :---- | :---- |
| **Left hand side** | <pre>,ght</pre> |
| **Right hand side** | |

| **Description** | stage buffer |
| :---- | :---- |
| **Left hand side** | <pre>,ghS</pre> |
| **Right hand side** | |

| **Description** | diff file |
| :---- | :---- |
| **Left hand side** | <pre>,gd</pre> |
| **Right hand side** | |

| **Description** | status |
| :---- | :---- |
| **Left hand side** | <pre>,gs</pre> |
| **Right hand side** | |

| **Description** | refactor |
| :---- | :---- |
| **Left hand side** | <pre>,pr</pre> |
| **Right hand side** | |

| **Description** | lazygit |
| :---- | :---- |
| **Left hand side** | <pre>,gg</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,dt</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,dO</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,do</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,di</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,dh</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,dd</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,dc</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,db</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,da</pre> |
| **Right hand side** | |

| **Description** | multicursor |
| :---- | :---- |
| **Left hand side** | <pre>,M</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;lt&gt;&lt;lt&gt;</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;lt&gt;</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>==</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>=</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&gt;&gt;</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&gt;</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>H</pre> |
| **Right hand side** | <pre>^</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>K</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>L</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua vim.lsp.buf.signature_help()&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>P</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua require('ecovim.plugins.telescope.pickers.multi-rg')()&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>Q</pre> |
| **Right hand side** | <pre>:lua require('mini.bufremove').delete(0, false)&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>X</pre> |
| **Right hand side** | <pre>"_X</pre> |

| **Description** | Nvim builtin |
| :---- | :---- |
| **Left hand side** | <pre>Y</pre> |
| **Right hand side** | <pre>y$</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>[g</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua vim.diagnostic.goto_prev({ float = { border = 'rounded', max_width = 100 }})&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>[%</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(MatchitNormalMultiBackward)</pre> |

| **Description** | Previous todo comment |
| :---- | :---- |
| **Left hand side** | <pre>[t</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>]g</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua vim.diagnostic.goto_next({ float = { border = 'rounded', max_width = 100 }})&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>]%</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(MatchitNormalMultiForward)</pre> |

| **Description** | Next todo comment |
| :---- | :---- |
| **Left hand side** | <pre>]t</pre> |
| **Right hand side** | |

| **Description** | Change a surrounding pair, putting replacements on new lines |
| :---- | :---- |
| **Left hand side** | <pre>cS</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(nvim-surround-change-line)</pre> |

| **Description** | Change a surrounding pair |
| :---- | :---- |
| **Left hand side** | <pre>cs</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(nvim-surround-change)</pre> |

| **Description** | Delete a surrounding pair |
| :---- | :---- |
| **Left hand side** | <pre>ds</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(nvim-surround-delete)</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>gP</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(printer_print)iw</pre> |

| **Description** | Open URL |
| :---- | :---- |
| **Left hand side** | <pre>gh</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;OpenRepo&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>gl</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua vim.diagnostic.open_float({ border = 'rounded', max_width = 100 })&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>gx</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;silent execute '!xdg-open ' . shellescape('&lt;lt&gt;cWORD&gt;')&lt;CR&gt;</pre> |

| **Description** | Operator keymap for printer.nvim |
| :---- | :---- |
| **Left hand side** | <pre>gp</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>gn</pre> |
| **Right hand side** | <pre>:bn&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>g%</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(MatchitNormalBackward)</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>gs</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(Switch)</pre> |

| **Description** | Comment insert end of line |
| :---- | :---- |
| **Left hand side** | <pre>gcA</pre> |
| **Right hand side** | |

| **Description** | Comment insert above |
| :---- | :---- |
| **Left hand side** | <pre>gcO</pre> |
| **Right hand side** | |

| **Description** | Comment insert below |
| :---- | :---- |
| **Left hand side** | <pre>gco</pre> |
| **Right hand side** | |

| **Description** | Comment toggle current block |
| :---- | :---- |
| **Left hand side** | <pre>gbc</pre> |
| **Right hand side** | |

| **Description** | Comment toggle current line |
| :---- | :---- |
| **Left hand side** | <pre>gcc</pre> |
| **Right hand side** | |

| **Description** | Comment toggle blockwise |
| :---- | :---- |
| **Left hand side** | <pre>gb</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(comment_toggle_blockwise)</pre> |

| **Description** | Comment toggle linewise |
| :---- | :---- |
| **Left hand side** | <pre>gc</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(comment_toggle_linewise)</pre> |

| **Description** | Align with preview |
| :---- | :---- |
| **Left hand side** | <pre>gA</pre> |
| **Right hand side** | |

| **Description** | Align |
| :---- | :---- |
| **Left hand side** | <pre>ga</pre> |
| **Right hand side** | |

| **Description** | Move to right "around" |
| :---- | :---- |
| **Left hand side** | <pre>g]</pre> |
| **Right hand side** | |

| **Description** | Move to left "around" |
| :---- | :---- |
| **Left hand side** | <pre>g[</pre> |
| **Right hand side** | |

| **Description** | Toggle Split/Join |
| :---- | :---- |
| **Left hand side** | <pre>gJ</pre> |
| **Right hand side** | |

| **Description** | LSP References |
| :---- | :---- |
| **Left hand side** | <pre>gr</pre> |
| **Right hand side** | |

| **Description** | LSP Definition |
| :---- | :---- |
| **Left hand side** | <pre>gd</pre> |
| **Right hand side** | |

| **Description** | LSP Implementations |
| :---- | :---- |
| **Left hand side** | <pre>gm</pre> |
| **Right hand side** | |

| **Description** | LSP Type Definitions |
| :---- | :---- |
| **Left hand side** | <pre>gy</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>s</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>x</pre> |
| **Right hand side** | <pre>"_x</pre> |

| **Description** | Add a surrounding pair around the current line, on new lines (normal mode) |
| :---- | :---- |
| **Left hand side** | <pre>ySS</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(nvim-surround-normal-cur-line)</pre> |

| **Description** | Add a surrounding pair around a motion, on new lines (normal mode) |
| :---- | :---- |
| **Left hand side** | <pre>yS</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(nvim-surround-normal-line)</pre> |

| **Description** | Add a surrounding pair around the current line (normal mode) |
| :---- | :---- |
| **Left hand side** | <pre>yss</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(nvim-surround-normal-cur)</pre> |

| **Description** | Add a surrounding pair around a motion (normal mode) |
| :---- | :---- |
| **Left hand side** | <pre>ys</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(nvim-surround-normal)</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>zr</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>zM</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>zR</pre> |
| **Right hand side** | |

| **Description** | Get text out of textobject formatted for debug printing |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(printer_print)</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;luasnip-expand-repeat</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;luasnip-delete-check</pre> |
| **Right hand side** | |

| **Description** | Increase window width |
| :---- | :---- |
| **Left hand side** | <pre>&lt;C-Right&gt;</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;vertical resize +2&lt;CR&gt;</pre> |

| **Description** | Decrease window width |
| :---- | :---- |
| **Left hand side** | <pre>&lt;C-Left&gt;</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;vertical resize -2&lt;CR&gt;</pre> |

| **Description** | Increase window height |
| :---- | :---- |
| **Left hand side** | <pre>&lt;C-Up&gt;</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;resize +2&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;C-Space&gt;</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua vim.lsp.buf.code_action()&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;C-X&gt;</pre> |
| **Right hand side** | <pre>:if !switch#Switch({'reverse': 1}) &#124; call speeddating#increment(-v:count1) | endif&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;C-A&gt;</pre> |
| **Right hand side** | <pre>:if !switch#Switch() &#124; call speeddating#increment(v:count1) | endif&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;S-Tab&gt;</pre> |
| **Right hand side** | <pre>:BufferLineCyclePrev&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;C-P&gt;</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua require('ecovim.plugins.telescope').project_files()&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;C-S&gt;</pre> |
| **Right hand side** | <pre>:w&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;C-K&gt;</pre> |
| **Right hand side** | <pre>&lt;C-W&gt;k</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;C-J&gt;</pre> |
| **Right hand side** | <pre>&lt;C-W&gt;j</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;C-H&gt;</pre> |
| **Right hand side** | <pre>&lt;C-W&gt;h</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(MatchitNormalMultiForward)</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(MatchitNormalMultiBackward)</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(MatchitNormalBackward)</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'n')&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(MatchitNormalForward)</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'n')&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;SpeedDatingFallbackDown</pre> |
| **Right hand side** | <pre>&lt;C-X&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;SpeedDatingFallbackUp</pre> |
| **Right hand side** | <pre>&lt;C-A&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;SpeedDatingNowUTC</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call speeddating#timestamp(1,v:count)&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;SpeedDatingNowLocal</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call speeddating#timestamp(0,v:count)&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;SpeedDatingDown</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call speeddating#increment(-v:count1)&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;SpeedDatingUp</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call speeddating#increment(v:count1)&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(SwitchReverse)</pre> |
| **Right hand side** | <pre>:set opfunc=switch#OpfuncReverse&lt;CR&gt;g@l</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(Switch)</pre> |
| **Right hand side** | <pre>:set opfunc=switch#OpfuncForward&lt;CR&gt;g@l</pre> |

| **Description** | Git Conflict: Previous Conflict |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(git-conflict-prev-conflict)</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;GitConflictPrevConflict&lt;CR&gt;</pre> |

| **Description** | Git Conflict: Next Conflict |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(git-conflict-next-conflict)</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;GitConflictNextConflict&lt;CR&gt;</pre> |

| **Description** | Git Conflict: Choose Theirs |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(git-conflict-theirs)</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;GitConflictChooseTheirs&lt;CR&gt;</pre> |

| **Description** | Git Conflict: Choose None |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(git-conflict-none)</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;GitConflictChooseNone&lt;CR&gt;</pre> |

| **Description** | Git Conflict: Choose Both |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(git-conflict-both)</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;GitConflictChooseBoth&lt;CR&gt;</pre> |

| **Description** | Git Conflict: Choose Ours |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(git-conflict-ours)</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;GitConflictChooseOurs&lt;CR&gt;</pre> |

| **Description** | Comment toggle blockwise with count |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(comment_toggle_blockwise_count)</pre> |
| **Right hand side** | |

| **Description** | Comment toggle linewise with count |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(comment_toggle_linewise_count)</pre> |
| **Right hand side** | |

| **Description** | Comment toggle current block |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(comment_toggle_blockwise_current)</pre> |
| **Right hand side** | |

| **Description** | Comment toggle current line |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(comment_toggle_linewise_current)</pre> |
| **Right hand side** | |

| **Description** | Comment toggle blockwise |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(comment_toggle_blockwise)</pre> |
| **Right hand side** | |

| **Description** | Comment toggle linewise |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(comment_toggle_linewise)</pre> |
| **Right hand side** | |

| **Description** | Change a surrounding pair, putting replacements on new lines |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(nvim-surround-change-line)</pre> |
| **Right hand side** | |

| **Description** | Change a surrounding pair |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(nvim-surround-change)</pre> |
| **Right hand side** | |

| **Description** | Delete a surrounding pair |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(nvim-surround-delete)</pre> |
| **Right hand side** | |

| **Description** | Add a surrounding pair around the current line, on new lines (normal mode) |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(nvim-surround-normal-cur-line)</pre> |
| **Right hand side** | |

| **Description** | Add a surrounding pair around a motion, on new lines (normal mode) |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(nvim-surround-normal-line)</pre> |
| **Right hand side** | |

| **Description** | Add a surrounding pair around the current line (normal mode) |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(nvim-surround-normal-cur)</pre> |
| **Right hand side** | |

| **Description** | Add a surrounding pair around a motion (normal mode) |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(nvim-surround-normal)</pre> |
| **Right hand side** | |

| **Description** | Toggle Terminal |
| :---- | :---- |
| **Left hand side** | <pre>&lt;F12&gt;</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;execute v:count . "ToggleTerm"&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;PlenaryTestFile</pre> |
| **Right hand side** | <pre>:lua require('plenary.test_harness').test_directory(vim.fn.expand("%:p"))&lt;CR&gt;</pre> |

| **Description** | Go to buffer 9 |
| :---- | :---- |
| **Left hand side** | <pre>&lt;M-9&gt;</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 8 |
| :---- | :---- |
| **Left hand side** | <pre>&lt;M-8&gt;</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 7 |
| :---- | :---- |
| **Left hand side** | <pre>&lt;M-7&gt;</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 6 |
| :---- | :---- |
| **Left hand side** | <pre>&lt;M-6&gt;</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 5 |
| :---- | :---- |
| **Left hand side** | <pre>&lt;M-5&gt;</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 4 |
| :---- | :---- |
| **Left hand side** | <pre>&lt;M-4&gt;</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 3 |
| :---- | :---- |
| **Left hand side** | <pre>&lt;M-3&gt;</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 2 |
| :---- | :---- |
| **Left hand side** | <pre>&lt;M-2&gt;</pre> |
| **Right hand side** | |

| **Description** | Go to buffer 1 |
| :---- | :---- |
| **Left hand side** | <pre>&lt;M-1&gt;</pre> |
| **Right hand side** | |

| **Description** | NvimTree |
| :---- | :---- |
| **Left hand side** | <pre>&lt;C-E&gt;</pre> |
| **Right hand side** | |

| **Description** | multicursor down |
| :---- | :---- |
| **Left hand side** | <pre>&lt;C-Down&gt;</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;C-L&gt;</pre> |
| **Right hand side** | <pre>&lt;C-W&gt;l</pre> |


### Visual mode keymaps

| **Description** | Nvim builtin |
| :---- | :---- |
| **Left hand side** | <pre>#</pre> |
| **Right hand side** | <pre>y?\V&lt;C-R&gt;"&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>%</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(MatchitVisualForward)</pre> |

| **Description** | Nvim builtin |
| :---- | :---- |
| **Left hand side** | <pre>*</pre> |
| **Right hand side** | <pre>y/\V&lt;C-R&gt;"&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,cf</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>,ca</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;'&lt;lt&gt;,'&gt;lua vim.lsp.buf.code_action()&lt;CR&gt;</pre> |

| **Description** | comment box |
| :---- | :---- |
| **Left hand side** | <pre>,ac</pre> |
| **Right hand side** | <pre>&lt;Cmd&gt;lua require('comment-box').lbox()&lt;CR&gt;</pre> |

| **Description** | Terminal Send |
| :---- | :---- |
| **Left hand side** | <pre>,ts</pre> |
| **Right hand side** | |

| **Description** | multicursor |
| :---- | :---- |
| **Left hand side** | <pre>,M</pre> |
| **Right hand side** | |

| **Description** | refactor |
| :---- | :---- |
| **Left hand side** | <pre>,pr</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;lt&gt;</pre> |
| **Right hand side** | <pre>&lt;lt&gt;gv</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>=</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&gt;</pre> |
| **Right hand side** | <pre>&gt;gv</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>J</pre> |
| **Right hand side** | <pre>:move '&gt;+1&lt;CR&gt;gv-gv</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>K</pre> |
| **Right hand side** | <pre>:move '&lt;lt&gt;-2&lt;CR&gt;gv-gv</pre> |

| **Description** | Add a surrounding pair around a visual selection |
| :---- | :---- |
| **Left hand side** | <pre>S</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(nvim-surround-visual)</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>X</pre> |
| **Right hand side** | <pre>"_X</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>[%</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(MatchitVisualMultiBackward)</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>]%</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(MatchitVisualMultiForward)</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>`</pre> |
| **Right hand side** | <pre>u</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>a%</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(MatchitVisualTextObject)</pre> |

| **Description** | Around last textobject |
| :---- | :---- |
| **Left hand side** | <pre>al</pre> |
| **Right hand side** | |

| **Description** | Around next textobject |
| :---- | :---- |
| **Left hand side** | <pre>an</pre> |
| **Right hand side** | |

| **Description** | Around textobject |
| :---- | :---- |
| **Left hand side** | <pre>a</pre> |
| **Right hand side** | |

| **Description** | Operator keymap for printer.nvim |
| :---- | :---- |
| **Left hand side** | <pre>gp</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>g%</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(MatchitVisualBackward)</pre> |

| **Description** | Add a surrounding pair around a visual selection, on new lines |
| :---- | :---- |
| **Left hand side** | <pre>gS</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(nvim-surround-visual-line)</pre> |

| **Description** | Align with preview |
| :---- | :---- |
| **Left hand side** | <pre>gA</pre> |
| **Right hand side** | |

| **Description** | Align |
| :---- | :---- |
| **Left hand side** | <pre>ga</pre> |
| **Right hand side** | |

| **Description** | Comment toggle blockwise (visual) |
| :---- | :---- |
| **Left hand side** | <pre>gb</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(comment_toggle_blockwise_visual)</pre> |

| **Description** | Comment toggle linewise (visual) |
| :---- | :---- |
| **Left hand side** | <pre>gc</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(comment_toggle_linewise_visual)</pre> |

| **Description** | Move to right "around" |
| :---- | :---- |
| **Left hand side** | <pre>g]</pre> |
| **Right hand side** | |

| **Description** | Move to left "around" |
| :---- | :---- |
| **Left hand side** | <pre>g[</pre> |
| **Right hand side** | |

| **Description** | Inside last textobject |
| :---- | :---- |
| **Left hand side** | <pre>il</pre> |
| **Right hand side** | |

| **Description** | Inside next textobject |
| :---- | :---- |
| **Left hand side** | <pre>in</pre> |
| **Right hand side** | |

| **Description** | Inside textobject |
| :---- | :---- |
| **Left hand side** | <pre>i</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>p</pre> |
| **Right hand side** | <pre>"_dP</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>s</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>x</pre> |
| **Right hand side** | <pre>"_x</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;luasnip-expand-repeat</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;M-`&gt;</pre> |
| **Right hand side** | <pre>U</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(MatchitVisualTextObject)</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(MatchitVisualMultiBackward)o&lt;Plug&gt;(MatchitVisualMultiForward)</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(MatchitVisualMultiForward)</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;m'gv``</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(MatchitVisualMultiBackward)</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;m'gv``</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(MatchitVisualBackward)</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'v')&lt;CR&gt;m'gv``</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(MatchitVisualForward)</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'v')&lt;CR&gt;:if col("''") != col("$") &#124; exe ":normal! m'" | endif&lt;CR&gt;gv``</pre> |

| **Description** | Add a surrounding pair around a visual selection, on new lines |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(nvim-surround-visual-line)</pre> |
| **Right hand side** | <pre>&lt;Esc&gt;&lt;Cmd&gt;lua require'nvim-surround'.visual_surround({ line_mode = true })&lt;CR&gt;</pre> |

| **Description** | Add a surrounding pair around a visual selection |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(nvim-surround-visual)</pre> |
| **Right hand side** | <pre>&lt;Esc&gt;&lt;Cmd&gt;lua require'nvim-surround'.visual_surround({ line_mode = false })&lt;CR&gt;</pre> |

| **Description** | Comment toggle blockwise (visual) |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(comment_toggle_blockwise_visual)</pre> |
| **Right hand side** | <pre>&lt;Esc&gt;&lt;Cmd&gt;lua require("Comment.api").locked("toggle.blockwise")(vim.fn.visualmode())&lt;CR&gt;</pre> |

| **Description** | Comment toggle linewise (visual) |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(comment_toggle_linewise_visual)</pre> |
| **Right hand side** | <pre>&lt;Esc&gt;&lt;Cmd&gt;lua require("Comment.api").locked("toggle.linewise")(vim.fn.visualmode())&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;SpeedDatingDown</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call speeddating#incrementvisual(-v:count1)&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;SpeedDatingUp</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call speeddating#incrementvisual(v:count1)&lt;CR&gt;</pre> |


### Operator mode keymaps

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>%</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(MatchitOperationForward)</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>[%</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(MatchitOperationMultiBackward)</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>]%</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(MatchitOperationMultiForward)</pre> |

| **Description** | Around last textobject |
| :---- | :---- |
| **Left hand side** | <pre>al</pre> |
| **Right hand side** | |

| **Description** | Around next textobject |
| :---- | :---- |
| **Left hand side** | <pre>an</pre> |
| **Right hand side** | |

| **Description** | Around textobject |
| :---- | :---- |
| **Left hand side** | <pre>a</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>g%</pre> |
| **Right hand side** | <pre>&lt;Plug&gt;(MatchitOperationBackward)</pre> |

| **Description** | Move to right "around" |
| :---- | :---- |
| **Left hand side** | <pre>g]</pre> |
| **Right hand side** | |

| **Description** | Move to left "around" |
| :---- | :---- |
| **Left hand side** | <pre>g[</pre> |
| **Right hand side** | |

| **Description** | Inside last textobject |
| :---- | :---- |
| **Left hand side** | <pre>il</pre> |
| **Right hand side** | |

| **Description** | Inside next textobject |
| :---- | :---- |
| **Left hand side** | <pre>in</pre> |
| **Right hand side** | |

| **Description** | Inside textobject |
| :---- | :---- |
| **Left hand side** | <pre>i</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>s</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;luasnip-expand-repeat</pre> |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(MatchitOperationMultiForward)</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call matchit#MultiMatch("W",  "o")&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(MatchitOperationMultiBackward)</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call matchit#MultiMatch("bW", "o")&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(MatchitOperationBackward)</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'o')&lt;CR&gt;</pre> |

| **Description** | |
| :---- | :---- |
| **Left hand side** | <pre>&lt;Plug&gt;(MatchitOperationForward)</pre> |
| **Right hand side** | <pre>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'o')&lt;CR&gt;</pre> |


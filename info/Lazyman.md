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

| :---- | :---- |
| **Left hand side** | <code>&lt;Tab&gt;</code> |
| **Right hand side** | <code>:BufferLineCycleNext&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;CR&gt;</code> |
| **Right hand side** | <code>:noh&lt;CR&gt;&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>%</code> |
| **Right hand side** | <code>&lt;Plug&gt;(MatchitNormalForward)</code> |

| **Description** | Nvim builtin |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&</code> |
| **Right hand side** | <code>:&&&lt;CR&gt;</code> |

| **Description** | Previous Tab |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,&lt;Tab&gt;[</code> |
| **Right hand side** | <code>&lt;Cmd&gt;tabprevious&lt;CR&gt;</code> |

| **Description** | Close Tab |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,&lt;Tab&gt;d</code> |
| **Right hand side** | <code>&lt;Cmd&gt;tabclose&lt;CR&gt;</code> |

| **Description** | Next Tab |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,&lt;Tab&gt;]</code> |
| **Right hand side** | <code>&lt;Cmd&gt;tabnext&lt;CR&gt;</code> |

| **Description** | New Tab |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,&lt;Tab&gt;&lt;Tab&gt;</code> |
| **Right hand side** | <code>&lt;Cmd&gt;tabnew&lt;CR&gt;</code> |

| **Description** | First Tab |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,&lt;Tab&gt;f</code> |
| **Right hand side** | <code>&lt;Cmd&gt;tabfirst&lt;CR&gt;</code> |

| **Description** | Last Tab |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,&lt;Tab&gt;l</code> |
| **Right hand side** | <code>&lt;Cmd&gt;tablast&lt;CR&gt;</code> |

| **Description** | Split window right |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,&#124;</code> |
| **Right hand side** | <code>&lt;C-W&gt;v</code> |

| **Description** | Split window below |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,-</code> |
| **Right hand side** | <code>&lt;C-W&gt;s</code> |

| **Description** | Split window right |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,w&#124;</code> |
| **Right hand side** | <code>&lt;C-W&gt;v</code> |

| **Description** | Split window below |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,w-</code> |
| **Right hand side** | <code>&lt;C-W&gt;s</code> |

| **Description** | Delete window |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,wd</code> |
| **Right hand side** | <code>&lt;C-W&gt;c</code> |

| **Description** | Other window |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ww</code> |
| **Right hand side** | <code>&lt;C-W&gt;p</code> |

| **Description** | Terminal (cwd) |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,fT</code> |
| **Right hand side** | |

| **Description** | Terminal (root dir) |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ft</code> |
| **Right hand side** | |

| **Description** | Inspect Pos |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ui</code> |
| **Right hand side** | |

| **Description** | Toggle number |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,uN</code> |
| **Right hand side** | |

| **Description** | Toggle mouse |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,um</code> |
| **Right hand side** | |

| **Description** | Toggle statusline |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,uS</code> |
| **Right hand side** | |

| **Description** | Toggle tabline |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,uT</code> |
| **Right hand side** | |

| **Description** | Toggle signcolumn |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ug</code> |
| **Right hand side** | |

| **Description** | Toggle Conceal |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,uc</code> |
| **Right hand side** | |

| **Description** | Toggle Line Numbers |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ul</code> |
| **Right hand side** | |

| **Description** | Toggle Word Wrap |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,uw</code> |
| **Right hand side** | |

| **Description** | Toggle Spelling |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,us</code> |
| **Right hand side** | |

| **Description** | Toggle format on Save |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,uf</code> |
| **Right hand side** | |

| **Description** | Toggle barbecue winbar |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ub</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,cl</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua vim.diagnostic.open_float({ border = 'rounded', max_width = 100 })&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>,cf</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua vim.lsp.buf.format({ async = true })&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>,cr</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua vim.lsp.buf.rename()&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>,ca</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua vim.lsp.buf.code_action()&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>,q</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua require('ecovim.utils').toggle_quicklist()&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>,.</code> |
| **Right hand side** | <code>:cn&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>,,</code> |
| **Right hand side** | <code>:cp&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>,pw</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua require('telescope.builtin').grep_string({ initial_mode = 'normal' })&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>,pf</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua require('ecovim.plugins.telescope').project_files({ default_text = vim.fn.expand('&lt;lt&gt;cword&gt;'), initial_mode = 'normal' })&lt;CR&gt;</code> |

| **Description** | Asciiville |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,av</code> |
| **Right hand side** | <code>&lt;Cmd&gt;Asciiville&lt;CR&gt;</code> |

| **Description** | Lazyman plugins |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,lp</code> |
| **Right hand side** | <code>&lt;Cmd&gt;Lazyplug&lt;CR&gt;</code> |

| **Description** | Lazyman configuration |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,lc</code> |
| **Right hand side** | <code>&lt;Cmd&gt;Lazyconf&lt;CR&gt;</code> |

| **Description** | Lazyman menu |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,lm</code> |
| **Right hand side** | <code>&lt;Cmd&gt;Lazyman&lt;CR&gt;</code> |

| **Description** | Htop command |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,H</code> |
| **Right hand side** | <code>&lt;Cmd&gt;Htop&lt;CR&gt;</code> |

| **Description** | Toggle colorcolumn |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,C</code> |
| **Right hand side** | |

| **Description** | Lazyman Keymaps |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,hk</code> |
| **Right hand side** | <code>&lt;Cmd&gt;help Lazyman-Keymaps&lt;CR&gt;</code> |

| **Description** | Nvims Help |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,hn</code> |
| **Right hand side** | <code>&lt;Cmd&gt;help Nvims&lt;CR&gt;</code> |

| **Description** | Lazyman Help |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,hl</code> |
| **Right hand side** | <code>&lt;Cmd&gt;help Lazyman&lt;CR&gt;</code> |

| **Description** | Options |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,o</code> |
| **Right hand side** | <code>&lt;Cmd&gt;options&lt;CR&gt;</code> |

| **Description** | Lazy Update |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,U</code> |
| **Right hand side** | <code>&lt;Cmd&gt;Lazy update&lt;CR&gt;</code> |

| **Description** | Lazy Menu |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,L</code> |
| **Right hand side** | <code>&lt;Cmd&gt;Lazy&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>,/l</code> |
| **Right hand side** | <code>&lt;Cmd&gt;:Lazy&lt;CR&gt;</code> |

| **Description** | terminal float |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,at</code> |
| **Right hand side** | <code>&lt;Cmd&gt;ToggleTerm direction=float&lt;CR&gt;</code> |

| **Description** | comment box |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ac</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua require('comment-box').lbox()&lt;CR&gt;</code> |

| **Description** | Move Float |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,tf</code> |
| **Right hand side** | |

| **Description** | Move Bottom Right New |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,tH</code> |
| **Right hand side** | |

| **Description** | Move Below Right New |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,th</code> |
| **Right hand side** | |

| **Description** | Move Bottom Right |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,tL</code> |
| **Right hand side** | |

| **Description** | Move Below Right |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,tl</code> |
| **Right hand side** | |

| **Description** | Terminal Prev |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,t[</code> |
| **Right hand side** | |

| **Description** | Terminal Next |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,t]</code> |
| **Right hand side** | |

| **Description** | Terminal Kill |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,tk</code> |
| **Right hand side** | |

| **Description** | New Terminal Run |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,tR</code> |
| **Right hand side** | |

| **Description** | Terminal Run |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,tr</code> |
| **Right hand side** | |

| **Description** | New Terminal Toggle |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,tO</code> |
| **Right hand side** | |

| **Description** | Terminal Toggle |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,to</code> |
| **Right hand side** | |

| **Description** | Terminal Send |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ts</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,gwc</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua require('telescope').extensions.git_worktree.create_git_worktree()&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>,gww</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua require('telescope').extensions.git_worktree.git_worktrees()&lt;CR&gt;</code> |

| **Description** | move to prev conflict |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,gcp</code> |
| **Right hand side** | <code>&lt;Cmd&gt;GitConflictPrevConflict&lt;CR&gt;</code> |

| **Description** | choose ours |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,gco</code> |
| **Right hand side** | <code>&lt;Cmd&gt;GitConflictChooseOurs&lt;CR&gt;</code> |

| **Description** | move to next conflict |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,gcn</code> |
| **Right hand side** | <code>&lt;Cmd&gt;GitConflictNextConflict&lt;CR&gt;</code> |

| **Description** | choose both |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,gcb</code> |
| **Right hand side** | <code>&lt;Cmd&gt;GitConflictChooseBoth&lt;CR&gt;</code> |

| **Description** | choose theirs |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,gct</code> |
| **Right hand side** | <code>&lt;Cmd&gt;GitConflictChooseTheirs&lt;CR&gt;</code> |

| **Description** | remove session |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,/sr</code> |
| **Right hand side** | <code>&lt;Cmd&gt;SessionManager delete_session&lt;CR&gt;</code> |

| **Description** | choose session |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,/sc</code> |
| **Right hand side** | <code>&lt;Cmd&gt;SessionManager load_session&lt;CR&gt;</code> |

| **Description** | save session |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,/ss</code> |
| **Right hand side** | <code>&lt;Cmd&gt;SessionManager save_current_session&lt;CR&gt;</code> |

| **Description** | load last session |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,/sl</code> |
| **Right hand side** | <code>&lt;Cmd&gt;SessionManager load_last_session&lt;CR&gt;</code> |

| **Description** | load current dir session |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,/sd</code> |
| **Right hand side** | <code>&lt;Cmd&gt;SessionManager load_current_dir_session&lt;CR&gt;</code> |

| **Description** | Mason |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,cm</code> |
| **Right hand side** | <code>&lt;Cmd&gt;Mason&lt;CR&gt;</code> |

| **Description** | Select Moonokai pro filter |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,up</code> |
| **Right hand side** | <code>&lt;Cmd&gt;MonokaiProSelect&lt;CR&gt;</code> |

| **Description** | Toggle Transparency |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ut</code> |
| **Right hand side** | |

| **Description** | Sort by relative dir |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,bsr</code> |
| **Right hand side** | |

| **Description** | Sort by extension |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,bse</code> |
| **Right hand side** | |

| **Description** | Sort by directory |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,bsd</code> |
| **Right hand side** | |

| **Description** | Pin/Unpin Buffer |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,bP</code> |
| **Right hand side** | |

| **Description** | Pick Buffer |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,bp</code> |
| **Right hand side** | |

| **Description** | Move next |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,bn</code> |
| **Right hand side** | |

| **Description** | Close Right |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,br</code> |
| **Right hand side** | |

| **Description** | Close Left |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,bl</code> |
| **Right hand side** | |

| **Description** | Go to buffer 1 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,1</code> |
| **Right hand side** | |

| **Description** | Go to buffer 2 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,2</code> |
| **Right hand side** | |

| **Description** | Go to buffer 3 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,3</code> |
| **Right hand side** | |

| **Description** | Go to buffer 4 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,4</code> |
| **Right hand side** | |

| **Description** | Go to buffer 5 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,5</code> |
| **Right hand side** | |

| **Description** | Go to buffer 6 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,6</code> |
| **Right hand side** | |

| **Description** | Move back |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,bb</code> |
| **Right hand side** | |

| **Description** | Go to buffer 7 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,7</code> |
| **Right hand side** | |

| **Description** | Go to buffer 8 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,8</code> |
| **Right hand side** | |

| **Description** | Go to buffer 9 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,9</code> |
| **Right hand side** | |

| **Description** | refactor |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,pr</code> |
| **Right hand side** | |

| **Description** | multicursor |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,M</code> |
| **Right hand side** | |

| **Description** | reset hunk |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ghr</code> |
| **Right hand side** | |

| **Description** | reset buffer |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ghR</code> |
| **Right hand side** | |

| **Description** | preview |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ghp</code> |
| **Right hand side** | |

| **Description** | diff hunk |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ghd</code> |
| **Right hand side** | |

| **Description** | undo stage |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ghu</code> |
| **Right hand side** | |

| **Description** | toggle deleted |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ght</code> |
| **Right hand side** | |

| **Description** | stage buffer |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ghS</code> |
| **Right hand side** | |

| **Description** | stage hunk |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ghs</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,di</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,dh</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,dd</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,dc</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,db</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,da</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,dt</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,dO</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,do</code> |
| **Right hand side** | |

| **Description** | lazygit |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,gg</code> |
| **Right hand side** | |

| **Description** | diff file |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,gd</code> |
| **Right hand side** | |

| **Description** | status |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,gs</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,DK</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,Dk</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,Dt</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,Dh</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,Dg</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,Ds</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,Dd</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,Dc</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,Di</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,Da</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,DA</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>&lt;lt&gt;&lt;lt&gt;</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>&lt;lt&gt;</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>==</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>=</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>&gt;&gt;</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>&gt;</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>H</code> |
| **Right hand side** | <code>^</code> |

| :---- | :---- |
| **Left hand side** | <code>K</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>L</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua vim.lsp.buf.signature_help()&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>P</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua require('ecovim.plugins.telescope.pickers.multi-rg')()&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>Q</code> |
| **Right hand side** | <code>:lua require('mini.bufremove').delete(0, false)&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>X</code> |
| **Right hand side** | <code>"_X</code> |

| **Description** | Nvim builtin |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>Y</code> |
| **Right hand side** | <code>y$</code> |

| :---- | :---- |
| **Left hand side** | <code>[g</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua vim.diagnostic.goto_prev({ float = { border = 'rounded', max_width = 100 }})&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>[%</code> |
| **Right hand side** | <code>&lt;Plug&gt;(MatchitNormalMultiBackward)</code> |

| **Description** | Previous todo comment |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>[t</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>]g</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua vim.diagnostic.goto_next({ float = { border = 'rounded', max_width = 100 }})&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>]%</code> |
| **Right hand side** | <code>&lt;Plug&gt;(MatchitNormalMultiForward)</code> |

| **Description** | Next todo comment |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>]t</code> |
| **Right hand side** | |

| **Description** | Change a surrounding pair, putting replacements on new lines |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>cS</code> |
| **Right hand side** | <code>&lt;Plug&gt;(nvim-surround-change-line)</code> |

| **Description** | Change a surrounding pair |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>cs</code> |
| **Right hand side** | <code>&lt;Plug&gt;(nvim-surround-change)</code> |

| **Description** | Delete a surrounding pair |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>ds</code> |
| **Right hand side** | <code>&lt;Plug&gt;(nvim-surround-delete)</code> |

| :---- | :---- |
| **Left hand side** | <code>gP</code> |
| **Right hand side** | <code>&lt;Plug&gt;(printer_print)iw</code> |

| **Description** | Open URL |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gh</code> |
| **Right hand side** | <code>&lt;Cmd&gt;OpenRepo&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>gl</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua vim.diagnostic.open_float({ border = 'rounded', max_width = 100 })&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>gx</code> |
| **Right hand side** | <code>&lt;Cmd&gt;silent execute '!xdg-open ' . shellescape('&lt;lt&gt;cWORD&gt;')&lt;CR&gt;</code> |

| **Description** | Operator keymap for printer.nvim |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gp</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>gn</code> |
| **Right hand side** | <code>:bn&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>g%</code> |
| **Right hand side** | <code>&lt;Plug&gt;(MatchitNormalBackward)</code> |

| :---- | :---- |
| **Left hand side** | <code>gs</code> |
| **Right hand side** | <code>&lt;Plug&gt;(Switch)</code> |

| **Description** | Comment insert end of line |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gcA</code> |
| **Right hand side** | |

| **Description** | Comment insert above |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gcO</code> |
| **Right hand side** | |

| **Description** | Comment insert below |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gco</code> |
| **Right hand side** | |

| **Description** | Comment toggle current block |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gbc</code> |
| **Right hand side** | |

| **Description** | Comment toggle current line |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gcc</code> |
| **Right hand side** | |

| **Description** | Comment toggle blockwise |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gb</code> |
| **Right hand side** | <code>&lt;Plug&gt;(comment_toggle_blockwise)</code> |

| **Description** | Comment toggle linewise |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gc</code> |
| **Right hand side** | <code>&lt;Plug&gt;(comment_toggle_linewise)</code> |

| **Description** | Move to right "around" |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>g]</code> |
| **Right hand side** | |

| **Description** | Move to left "around" |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>g[</code> |
| **Right hand side** | |

| **Description** | Align with preview |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gA</code> |
| **Right hand side** | |

| **Description** | Align |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>ga</code> |
| **Right hand side** | |

| **Description** | Toggle Split/Join |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gJ</code> |
| **Right hand side** | |

| **Description** | LSP Definition |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gd</code> |
| **Right hand side** | |

| **Description** | LSP Implementations |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gm</code> |
| **Right hand side** | |

| **Description** | LSP References |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gr</code> |
| **Right hand side** | |

| **Description** | LSP Type Definitions |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gy</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>s</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>x</code> |
| **Right hand side** | <code>"_x</code> |

| **Description** | Add a surrounding pair around the current line, on new lines (normal mode) |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>ySS</code> |
| **Right hand side** | <code>&lt;Plug&gt;(nvim-surround-normal-cur-line)</code> |

| **Description** | Add a surrounding pair around a motion, on new lines (normal mode) |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>yS</code> |
| **Right hand side** | <code>&lt;Plug&gt;(nvim-surround-normal-line)</code> |

| **Description** | Add a surrounding pair around the current line (normal mode) |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>yss</code> |
| **Right hand side** | <code>&lt;Plug&gt;(nvim-surround-normal-cur)</code> |

| **Description** | Add a surrounding pair around a motion (normal mode) |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>ys</code> |
| **Right hand side** | <code>&lt;Plug&gt;(nvim-surround-normal)</code> |

| :---- | :---- |
| **Left hand side** | <code>zr</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>zM</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>zR</code> |
| **Right hand side** | |

| **Description** | Get text out of textobject formatted for debug printing |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(printer_print)</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;luasnip-expand-repeat</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;luasnip-delete-check</code> |
| **Right hand side** | |

| **Description** | Increase window width |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;C-Right&gt;</code> |
| **Right hand side** | <code>&lt;Cmd&gt;vertical resize +2&lt;CR&gt;</code> |

| **Description** | Decrease window width |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;C-Left&gt;</code> |
| **Right hand side** | <code>&lt;Cmd&gt;vertical resize -2&lt;CR&gt;</code> |

| **Description** | Increase window height |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;C-Up&gt;</code> |
| **Right hand side** | <code>&lt;Cmd&gt;resize +2&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;C-Space&gt;</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua vim.lsp.buf.code_action()&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;C-X&gt;</code> |
| **Right hand side** | <code>:if !switch#Switch({'reverse': 1}) &#124; call speeddating#increment(-v:count1) | endif&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;C-A&gt;</code> |
| **Right hand side** | <code>:if !switch#Switch() &#124; call speeddating#increment(v:count1) | endif&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;S-Tab&gt;</code> |
| **Right hand side** | <code>:BufferLineCyclePrev&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;C-P&gt;</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua require('ecovim.plugins.telescope').project_files()&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;C-S&gt;</code> |
| **Right hand side** | <code>:w&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;C-K&gt;</code> |
| **Right hand side** | <code>&lt;C-W&gt;k</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;C-J&gt;</code> |
| **Right hand side** | <code>&lt;C-W&gt;j</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;C-H&gt;</code> |
| **Right hand side** | <code>&lt;C-W&gt;h</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(MatchitNormalMultiForward)</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(MatchitNormalMultiBackward)</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(MatchitNormalBackward)</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'n')&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(MatchitNormalForward)</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'n')&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(SwitchReverse)</code> |
| **Right hand side** | <code>:set opfunc=switch#OpfuncReverse&lt;CR&gt;g@l</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(Switch)</code> |
| **Right hand side** | <code>:set opfunc=switch#OpfuncForward&lt;CR&gt;g@l</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;SpeedDatingFallbackDown</code> |
| **Right hand side** | <code>&lt;C-X&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;SpeedDatingFallbackUp</code> |
| **Right hand side** | <code>&lt;C-A&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;SpeedDatingNowUTC</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call speeddating#timestamp(1,v:count)&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;SpeedDatingNowLocal</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call speeddating#timestamp(0,v:count)&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;SpeedDatingDown</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call speeddating#increment(-v:count1)&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;SpeedDatingUp</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call speeddating#increment(v:count1)&lt;CR&gt;</code> |

| **Description** | Change a surrounding pair, putting replacements on new lines |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(nvim-surround-change-line)</code> |
| **Right hand side** | |

| **Description** | Change a surrounding pair |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(nvim-surround-change)</code> |
| **Right hand side** | |

| **Description** | Delete a surrounding pair |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(nvim-surround-delete)</code> |
| **Right hand side** | |

| **Description** | Add a surrounding pair around the current line, on new lines (normal mode) |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(nvim-surround-normal-cur-line)</code> |
| **Right hand side** | |

| **Description** | Add a surrounding pair around a motion, on new lines (normal mode) |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(nvim-surround-normal-line)</code> |
| **Right hand side** | |

| **Description** | Add a surrounding pair around the current line (normal mode) |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(nvim-surround-normal-cur)</code> |
| **Right hand side** | |

| **Description** | Add a surrounding pair around a motion (normal mode) |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(nvim-surround-normal)</code> |
| **Right hand side** | |

| **Description** | Toggle Terminal |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;F12&gt;</code> |
| **Right hand side** | <code>&lt;Cmd&gt;execute v:count . "ToggleTerm"&lt;CR&gt;</code> |

| **Description** | Comment toggle blockwise with count |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(comment_toggle_blockwise_count)</code> |
| **Right hand side** | |

| **Description** | Comment toggle linewise with count |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(comment_toggle_linewise_count)</code> |
| **Right hand side** | |

| **Description** | Comment toggle current block |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(comment_toggle_blockwise_current)</code> |
| **Right hand side** | |

| **Description** | Comment toggle current line |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(comment_toggle_linewise_current)</code> |
| **Right hand side** | |

| **Description** | Comment toggle blockwise |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(comment_toggle_blockwise)</code> |
| **Right hand side** | |

| **Description** | Comment toggle linewise |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(comment_toggle_linewise)</code> |
| **Right hand side** | |

| **Description** | Git Conflict: Previous Conflict |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(git-conflict-prev-conflict)</code> |
| **Right hand side** | <code>&lt;Cmd&gt;GitConflictPrevConflict&lt;CR&gt;</code> |

| **Description** | Git Conflict: Next Conflict |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(git-conflict-next-conflict)</code> |
| **Right hand side** | <code>&lt;Cmd&gt;GitConflictNextConflict&lt;CR&gt;</code> |

| **Description** | Git Conflict: Choose Theirs |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(git-conflict-theirs)</code> |
| **Right hand side** | <code>&lt;Cmd&gt;GitConflictChooseTheirs&lt;CR&gt;</code> |

| **Description** | Git Conflict: Choose None |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(git-conflict-none)</code> |
| **Right hand side** | <code>&lt;Cmd&gt;GitConflictChooseNone&lt;CR&gt;</code> |

| **Description** | Git Conflict: Choose Both |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(git-conflict-both)</code> |
| **Right hand side** | <code>&lt;Cmd&gt;GitConflictChooseBoth&lt;CR&gt;</code> |

| **Description** | Git Conflict: Choose Ours |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(git-conflict-ours)</code> |
| **Right hand side** | <code>&lt;Cmd&gt;GitConflictChooseOurs&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;PlenaryTestFile</code> |
| **Right hand side** | <code>:lua require('plenary.test_harness').test_directory(vim.fn.expand("%:p"))&lt;CR&gt;</code> |

| **Description** | Go to buffer 7 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;M-7&gt;</code> |
| **Right hand side** | |

| **Description** | Go to buffer 6 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;M-6&gt;</code> |
| **Right hand side** | |

| **Description** | Go to buffer 4 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;M-4&gt;</code> |
| **Right hand side** | |

| **Description** | Go to buffer 3 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;M-3&gt;</code> |
| **Right hand side** | |

| **Description** | Go to buffer 2 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;M-2&gt;</code> |
| **Right hand side** | |

| **Description** | Go to buffer 1 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;M-1&gt;</code> |
| **Right hand side** | |

| **Description** | Go to buffer 9 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;M-9&gt;</code> |
| **Right hand side** | |

| **Description** | Go to buffer 8 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;M-8&gt;</code> |
| **Right hand side** | |

| **Description** | Go to buffer 5 |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;M-5&gt;</code> |
| **Right hand side** | |

| **Description** | NvimTree |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;C-E&gt;</code> |
| **Right hand side** | |

| **Description** | multicursor down |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;C-Down&gt;</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>&lt;C-L&gt;</code> |
| **Right hand side** | <code>&lt;C-W&gt;l</code> |


### Visual mode keymaps

| **Description** | Nvim builtin |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>#</code> |
| **Right hand side** | <code>y?\V&lt;C-R&gt;"&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>%</code> |
| **Right hand side** | <code>&lt;Plug&gt;(MatchitVisualForward)</code> |

| **Description** | Nvim builtin |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>*</code> |
| **Right hand side** | <code>y/\V&lt;C-R&gt;"&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>,cf</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>,ca</code> |
| **Right hand side** | <code>&lt;Cmd&gt;'&lt;lt&gt;,'&gt;lua vim.lsp.buf.code_action()&lt;CR&gt;</code> |

| **Description** | Terminal Send |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ts</code> |
| **Right hand side** | |

| **Description** | comment box |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,ac</code> |
| **Right hand side** | <code>&lt;Cmd&gt;lua require('comment-box').lbox()&lt;CR&gt;</code> |

| **Description** | refactor |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,pr</code> |
| **Right hand side** | |

| **Description** | multicursor |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>,M</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>&lt;lt&gt;</code> |
| **Right hand side** | <code>&lt;lt&gt;gv</code> |

| :---- | :---- |
| **Left hand side** | <code>=</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>&gt;</code> |
| **Right hand side** | <code>&gt;gv</code> |

| :---- | :---- |
| **Left hand side** | <code>J</code> |
| **Right hand side** | <code>:move '&gt;+1&lt;CR&gt;gv-gv</code> |

| :---- | :---- |
| **Left hand side** | <code>K</code> |
| **Right hand side** | <code>:move '&lt;lt&gt;-2&lt;CR&gt;gv-gv</code> |

| **Description** | Add a surrounding pair around a visual selection |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>S</code> |
| **Right hand side** | <code>&lt;Plug&gt;(nvim-surround-visual)</code> |

| :---- | :---- |
| **Left hand side** | <code>X</code> |
| **Right hand side** | <code>"_X</code> |

| :---- | :---- |
| **Left hand side** | <code>[%</code> |
| **Right hand side** | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)</code> |

| :---- | :---- |
| **Left hand side** | <code>]%</code> |
| **Right hand side** | <code>&lt;Plug&gt;(MatchitVisualMultiForward)</code> |

| :---- | :---- |
| **Left hand side** | <code>`</code> |
| **Right hand side** | <code>u</code> |

| :---- | :---- |
| **Left hand side** | <code>a%</code> |
| **Right hand side** | <code>&lt;Plug&gt;(MatchitVisualTextObject)</code> |

| **Description** | Around last textobject |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>al</code> |
| **Right hand side** | |

| **Description** | Around next textobject |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>an</code> |
| **Right hand side** | |

| **Description** | Around textobject |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>a</code> |
| **Right hand side** | |

| **Description** | Operator keymap for printer.nvim |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gp</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>g%</code> |
| **Right hand side** | <code>&lt;Plug&gt;(MatchitVisualBackward)</code> |

| **Description** | Comment toggle blockwise (visual) |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gb</code> |
| **Right hand side** | <code>&lt;Plug&gt;(comment_toggle_blockwise_visual)</code> |

| **Description** | Comment toggle linewise (visual) |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gc</code> |
| **Right hand side** | <code>&lt;Plug&gt;(comment_toggle_linewise_visual)</code> |

| **Description** | Move to right "around" |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>g]</code> |
| **Right hand side** | |

| **Description** | Move to left "around" |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>g[</code> |
| **Right hand side** | |

| **Description** | Add a surrounding pair around a visual selection, on new lines |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gS</code> |
| **Right hand side** | <code>&lt;Plug&gt;(nvim-surround-visual-line)</code> |

| **Description** | Align with preview |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>gA</code> |
| **Right hand side** | |

| **Description** | Align |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>ga</code> |
| **Right hand side** | |

| **Description** | Inside last textobject |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>il</code> |
| **Right hand side** | |

| **Description** | Inside next textobject |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>in</code> |
| **Right hand side** | |

| **Description** | Inside textobject |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>i</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>p</code> |
| **Right hand side** | <code>"_dP</code> |

| :---- | :---- |
| **Left hand side** | <code>s</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>x</code> |
| **Right hand side** | <code>"_x</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;luasnip-expand-repeat</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>&lt;M-`&gt;</code> |
| **Right hand side** | <code>U</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(MatchitVisualTextObject)</code> |
| **Right hand side** | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)o&lt;Plug&gt;(MatchitVisualMultiForward)</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(MatchitVisualMultiForward)</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;m'gv``</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(MatchitVisualMultiBackward)</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;m'gv``</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(MatchitVisualBackward)</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'v')&lt;CR&gt;m'gv``</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(MatchitVisualForward)</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'v')&lt;CR&gt;:if col("''") != col("$") &#124; exe ":normal! m'" | endif&lt;CR&gt;gv``</code> |

| **Description** | Comment toggle blockwise (visual) |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(comment_toggle_blockwise_visual)</code> |
| **Right hand side** | <code>&lt;Esc&gt;&lt;Cmd&gt;lua require("Comment.api").locked("toggle.blockwise")(vim.fn.visualmode())&lt;CR&gt;</code> |

| **Description** | Comment toggle linewise (visual) |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(comment_toggle_linewise_visual)</code> |
| **Right hand side** | <code>&lt;Esc&gt;&lt;Cmd&gt;lua require("Comment.api").locked("toggle.linewise")(vim.fn.visualmode())&lt;CR&gt;</code> |

| **Description** | Add a surrounding pair around a visual selection, on new lines |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(nvim-surround-visual-line)</code> |
| **Right hand side** | <code>&lt;Esc&gt;&lt;Cmd&gt;lua require'nvim-surround'.visual_surround({ line_mode = true })&lt;CR&gt;</code> |

| **Description** | Add a surrounding pair around a visual selection |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(nvim-surround-visual)</code> |
| **Right hand side** | <code>&lt;Esc&gt;&lt;Cmd&gt;lua require'nvim-surround'.visual_surround({ line_mode = false })&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;SpeedDatingDown</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call speeddating#incrementvisual(-v:count1)&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;SpeedDatingUp</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call speeddating#incrementvisual(v:count1)&lt;CR&gt;</code> |


### Operator mode keymaps

| :---- | :---- |
| **Left hand side** | <code>%</code> |
| **Right hand side** | <code>&lt;Plug&gt;(MatchitOperationForward)</code> |

| :---- | :---- |
| **Left hand side** | <code>[%</code> |
| **Right hand side** | <code>&lt;Plug&gt;(MatchitOperationMultiBackward)</code> |

| :---- | :---- |
| **Left hand side** | <code>]%</code> |
| **Right hand side** | <code>&lt;Plug&gt;(MatchitOperationMultiForward)</code> |

| **Description** | Around last textobject |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>al</code> |
| **Right hand side** | |

| **Description** | Around next textobject |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>an</code> |
| **Right hand side** | |

| **Description** | Around textobject |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>a</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>g%</code> |
| **Right hand side** | <code>&lt;Plug&gt;(MatchitOperationBackward)</code> |

| **Description** | Move to right "around" |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>g]</code> |
| **Right hand side** | |

| **Description** | Move to left "around" |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>g[</code> |
| **Right hand side** | |

| **Description** | Inside last textobject |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>il</code> |
| **Right hand side** | |

| **Description** | Inside next textobject |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>in</code> |
| **Right hand side** | |

| **Description** | Inside textobject |
| **Description** | |
| :---- | :---- |
| **Left hand side** | <code>i</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>s</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;luasnip-expand-repeat</code> |
| **Right hand side** | |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(MatchitOperationMultiForward)</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call matchit#MultiMatch("W",  "o")&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(MatchitOperationMultiBackward)</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call matchit#MultiMatch("bW", "o")&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(MatchitOperationBackward)</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',0,'o')&lt;CR&gt;</code> |

| :---- | :---- |
| **Left hand side** | <code>&lt;Plug&gt;(MatchitOperationForward)</code> |
| **Right hand side** | <code>:&lt;C-U&gt;call matchit#Match_wrapper('',1,'o')&lt;CR&gt;</code> |


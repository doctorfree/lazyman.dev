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
| **Left hand side** | &lt;Tab&gt; |
| **Right hand side** | :BufferLineCycleNext&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;CR&gt; |
| **Right hand side** | :noh&lt;CR&gt;&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | % |
| **Right hand side** | &lt;Plug&gt;(MatchitNormalForward) |

| **Description** | Nvim builtin |
| :---- | :---- |
| **Left hand side** | & |
| **Right hand side** | :&&&lt;CR&gt; |

| **Description** | Previous Tab |
| :---- | :---- |
| **Left hand side** | ,&lt;Tab&gt;[ |
| **Right hand side** | &lt;Cmd&gt;tabprevious&lt;CR&gt; |

| **Description** | Close Tab |
| :---- | :---- |
| **Left hand side** | ,&lt;Tab&gt;d |
| **Right hand side** | &lt;Cmd&gt;tabclose&lt;CR&gt; |

| **Description** | Next Tab |
| :---- | :---- |
| **Left hand side** | ,&lt;Tab&gt;] |
| **Right hand side** | &lt;Cmd&gt;tabnext&lt;CR&gt; |

| **Description** | New Tab |
| :---- | :---- |
| **Left hand side** | ,&lt;Tab&gt;&lt;Tab&gt; |
| **Right hand side** | &lt;Cmd&gt;tabnew&lt;CR&gt; |

| **Description** | First Tab |
| :---- | :---- |
| **Left hand side** | ,&lt;Tab&gt;f |
| **Right hand side** | &lt;Cmd&gt;tabfirst&lt;CR&gt; |

| **Description** | Last Tab |
| :---- | :---- |
| **Left hand side** | ,&lt;Tab&gt;l |
| **Right hand side** | &lt;Cmd&gt;tablast&lt;CR&gt; |

| **Description** | Split window right |
| :---- | :---- |
| **Left hand side** | ,&#124; |
| **Right hand side** | &lt;C-W&gt;v |

| **Description** | Split window below |
| :---- | :---- |
| **Left hand side** | ,- |
| **Right hand side** | &lt;C-W&gt;s |

| **Description** | Split window right |
| :---- | :---- |
| **Left hand side** | ,w&#124; |
| **Right hand side** | &lt;C-W&gt;v |

| **Description** | Split window below |
| :---- | :---- |
| **Left hand side** | ,w- |
| **Right hand side** | &lt;C-W&gt;s |

| **Description** | Delete window |
| :---- | :---- |
| **Left hand side** | ,wd |
| **Right hand side** | &lt;C-W&gt;c |

| **Description** | Other window |
| :---- | :---- |
| **Left hand side** | ,ww |
| **Right hand side** | &lt;C-W&gt;p |

| **Description** | Terminal (cwd) |
| :---- | :---- |
| **Left hand side** | ,fT |
| **Right hand side** | |

| **Description** | Terminal (root dir) |
| :---- | :---- |
| **Left hand side** | ,ft |
| **Right hand side** | |

| **Description** | Inspect Pos |
| :---- | :---- |
| **Left hand side** | ,ui |
| **Right hand side** | |

| **Description** | Toggle number |
| :---- | :---- |
| **Left hand side** | ,uN |
| **Right hand side** | |

| **Description** | Toggle mouse |
| :---- | :---- |
| **Left hand side** | ,um |
| **Right hand side** | |

| **Description** | Toggle statusline |
| :---- | :---- |
| **Left hand side** | ,uS |
| **Right hand side** | |

| **Description** | Toggle tabline |
| :---- | :---- |
| **Left hand side** | ,uT |
| **Right hand side** | |

| **Description** | Toggle signcolumn |
| :---- | :---- |
| **Left hand side** | ,ug |
| **Right hand side** | |

| **Description** | Toggle Conceal |
| :---- | :---- |
| **Left hand side** | ,uc |
| **Right hand side** | |

| **Description** | Toggle Line Numbers |
| :---- | :---- |
| **Left hand side** | ,ul |
| **Right hand side** | |

| **Description** | Toggle Word Wrap |
| :---- | :---- |
| **Left hand side** | ,uw |
| **Right hand side** | |

| **Description** | Toggle Spelling |
| :---- | :---- |
| **Left hand side** | ,us |
| **Right hand side** | |

| **Description** | Toggle format on Save |
| :---- | :---- |
| **Left hand side** | ,uf |
| **Right hand side** | |

| **Description** | Toggle barbecue winbar |
| :---- | :---- |
| **Left hand side** | ,ub |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,cl |
| **Right hand side** | &lt;Cmd&gt;lua vim.diagnostic.open_float({ border = 'rounded', max_width = 100 })&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,cf |
| **Right hand side** | &lt;Cmd&gt;lua vim.lsp.buf.format({ async = true })&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,cr |
| **Right hand side** | &lt;Cmd&gt;lua vim.lsp.buf.rename()&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,ca |
| **Right hand side** | &lt;Cmd&gt;lua vim.lsp.buf.code_action()&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,q |
| **Right hand side** | &lt;Cmd&gt;lua require('ecovim.utils').toggle_quicklist()&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,. |
| **Right hand side** | :cn&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,, |
| **Right hand side** | :cp&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,pw |
| **Right hand side** | &lt;Cmd&gt;lua require('telescope.builtin').grep_string({ initial_mode = 'normal' })&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,pf |
| **Right hand side** | &lt;Cmd&gt;lua require('ecovim.plugins.telescope').project_files({ default_text = vim.fn.expand('&lt;lt&gt;cword&gt;'), initial_mode = 'normal' })&lt;CR&gt; |

| **Description** | Asciiville |
| :---- | :---- |
| **Left hand side** | ,av |
| **Right hand side** | &lt;Cmd&gt;Asciiville&lt;CR&gt; |

| **Description** | Lazyman plugins |
| :---- | :---- |
| **Left hand side** | ,lp |
| **Right hand side** | &lt;Cmd&gt;Lazyplug&lt;CR&gt; |

| **Description** | Lazyman configuration |
| :---- | :---- |
| **Left hand side** | ,lc |
| **Right hand side** | &lt;Cmd&gt;Lazyconf&lt;CR&gt; |

| **Description** | Lazyman menu |
| :---- | :---- |
| **Left hand side** | ,lm |
| **Right hand side** | &lt;Cmd&gt;Lazyman&lt;CR&gt; |

| **Description** | Htop command |
| :---- | :---- |
| **Left hand side** | ,H |
| **Right hand side** | &lt;Cmd&gt;Htop&lt;CR&gt; |

| **Description** | Toggle colorcolumn |
| :---- | :---- |
| **Left hand side** | ,C |
| **Right hand side** | |

| **Description** | Lazyman Keymaps |
| :---- | :---- |
| **Left hand side** | ,hk |
| **Right hand side** | &lt;Cmd&gt;help Lazyman-Keymaps&lt;CR&gt; |

| **Description** | Nvims Help |
| :---- | :---- |
| **Left hand side** | ,hn |
| **Right hand side** | &lt;Cmd&gt;help Nvims&lt;CR&gt; |

| **Description** | Lazyman Help |
| :---- | :---- |
| **Left hand side** | ,hl |
| **Right hand side** | &lt;Cmd&gt;help Lazyman&lt;CR&gt; |

| **Description** | Options |
| :---- | :---- |
| **Left hand side** | ,o |
| **Right hand side** | &lt;Cmd&gt;options&lt;CR&gt; |

| **Description** | Lazy Update |
| :---- | :---- |
| **Left hand side** | ,U |
| **Right hand side** | &lt;Cmd&gt;Lazy update&lt;CR&gt; |

| **Description** | Lazy Menu |
| :---- | :---- |
| **Left hand side** | ,L |
| **Right hand side** | &lt;Cmd&gt;Lazy&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,/l |
| **Right hand side** | &lt;Cmd&gt;:Lazy&lt;CR&gt; |

| **Description** | comment box |
| :---- | :---- |
| **Left hand side** | ,ac |
| **Right hand side** | &lt;Cmd&gt;lua require('comment-box').lbox()&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,gwc |
| **Right hand side** | &lt;Cmd&gt;lua require('telescope').extensions.git_worktree.create_git_worktree()&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,gww |
| **Right hand side** | &lt;Cmd&gt;lua require('telescope').extensions.git_worktree.git_worktrees()&lt;CR&gt; |

| **Description** | Mason |
| :---- | :---- |
| **Left hand side** | ,cm |
| **Right hand side** | &lt;Cmd&gt;Mason&lt;CR&gt; |

| **Description** | choose theirs |
| :---- | :---- |
| **Left hand side** | ,gct |
| **Right hand side** | &lt;Cmd&gt;GitConflictChooseTheirs&lt;CR&gt; |

| **Description** | move to prev conflict |
| :---- | :---- |
| **Left hand side** | ,gcp |
| **Right hand side** | &lt;Cmd&gt;GitConflictPrevConflict&lt;CR&gt; |

| **Description** | choose ours |
| :---- | :---- |
| **Left hand side** | ,gco |
| **Right hand side** | &lt;Cmd&gt;GitConflictChooseOurs&lt;CR&gt; |

| **Description** | move to next conflict |
| :---- | :---- |
| **Left hand side** | ,gcn |
| **Right hand side** | &lt;Cmd&gt;GitConflictNextConflict&lt;CR&gt; |

| **Description** | choose both |
| :---- | :---- |
| **Left hand side** | ,gcb |
| **Right hand side** | &lt;Cmd&gt;GitConflictChooseBoth&lt;CR&gt; |

| **Description** | Move Float |
| :---- | :---- |
| **Left hand side** | ,tf |
| **Right hand side** | |

| **Description** | Move Bottom Right New |
| :---- | :---- |
| **Left hand side** | ,tH |
| **Right hand side** | |

| **Description** | Move Below Right New |
| :---- | :---- |
| **Left hand side** | ,th |
| **Right hand side** | |

| **Description** | Move Bottom Right |
| :---- | :---- |
| **Left hand side** | ,tL |
| **Right hand side** | |

| **Description** | Move Below Right |
| :---- | :---- |
| **Left hand side** | ,tl |
| **Right hand side** | |

| **Description** | Terminal Prev |
| :---- | :---- |
| **Left hand side** | ,t[ |
| **Right hand side** | |

| **Description** | Terminal Next |
| :---- | :---- |
| **Left hand side** | ,t] |
| **Right hand side** | |

| **Description** | Terminal Kill |
| :---- | :---- |
| **Left hand side** | ,tk |
| **Right hand side** | |

| **Description** | New Terminal Run |
| :---- | :---- |
| **Left hand side** | ,tR |
| **Right hand side** | |

| **Description** | Terminal Run |
| :---- | :---- |
| **Left hand side** | ,tr |
| **Right hand side** | |

| **Description** | New Terminal Toggle |
| :---- | :---- |
| **Left hand side** | ,tO |
| **Right hand side** | |

| **Description** | Terminal Toggle |
| :---- | :---- |
| **Left hand side** | ,to |
| **Right hand side** | |

| **Description** | Terminal Send |
| :---- | :---- |
| **Left hand side** | ,ts |
| **Right hand side** | |

| **Description** | terminal float |
| :---- | :---- |
| **Left hand side** | ,at |
| **Right hand side** | &lt;Cmd&gt;ToggleTerm direction=float&lt;CR&gt; |

| **Description** | choose session |
| :---- | :---- |
| **Left hand side** | ,/sc |
| **Right hand side** | &lt;Cmd&gt;SessionManager load_session&lt;CR&gt; |

| **Description** | save session |
| :---- | :---- |
| **Left hand side** | ,/ss |
| **Right hand side** | &lt;Cmd&gt;SessionManager save_current_session&lt;CR&gt; |

| **Description** | load last session |
| :---- | :---- |
| **Left hand side** | ,/sl |
| **Right hand side** | &lt;Cmd&gt;SessionManager load_last_session&lt;CR&gt; |

| **Description** | load current dir session |
| :---- | :---- |
| **Left hand side** | ,/sd |
| **Right hand side** | &lt;Cmd&gt;SessionManager load_current_dir_session&lt;CR&gt; |

| **Description** | remove session |
| :---- | :---- |
| **Left hand side** | ,/sr |
| **Right hand side** | &lt;Cmd&gt;SessionManager delete_session&lt;CR&gt; |

| **Description** | Select Moonokai pro filter |
| :---- | :---- |
| **Left hand side** | ,up |
| **Right hand side** | &lt;Cmd&gt;MonokaiProSelect&lt;CR&gt; |

| **Description** | Toggle Transparency |
| :---- | :---- |
| **Left hand side** | ,ut |
| **Right hand side** | |

| **Description** | refactor |
| :---- | :---- |
| **Left hand side** | ,pr |
| **Right hand side** | |

| **Description** | Move back |
| :---- | :---- |
| **Left hand side** | ,bb |
| **Right hand side** | |

| **Description** | Go to buffer 3 |
| :---- | :---- |
| **Left hand side** | ,3 |
| **Right hand side** | |

| **Description** | Go to buffer 4 |
| :---- | :---- |
| **Left hand side** | ,4 |
| **Right hand side** | |

| **Description** | Go to buffer 5 |
| :---- | :---- |
| **Left hand side** | ,5 |
| **Right hand side** | |

| **Description** | Go to buffer 6 |
| :---- | :---- |
| **Left hand side** | ,6 |
| **Right hand side** | |

| **Description** | Go to buffer 7 |
| :---- | :---- |
| **Left hand side** | ,7 |
| **Right hand side** | |

| **Description** | Go to buffer 8 |
| :---- | :---- |
| **Left hand side** | ,8 |
| **Right hand side** | |

| **Description** | Go to buffer 9 |
| :---- | :---- |
| **Left hand side** | ,9 |
| **Right hand side** | |

| **Description** | Go to buffer 1 |
| :---- | :---- |
| **Left hand side** | ,1 |
| **Right hand side** | |

| **Description** | Go to buffer 2 |
| :---- | :---- |
| **Left hand side** | ,2 |
| **Right hand side** | |

| **Description** | Sort by relative dir |
| :---- | :---- |
| **Left hand side** | ,bsr |
| **Right hand side** | |

| **Description** | Sort by extension |
| :---- | :---- |
| **Left hand side** | ,bse |
| **Right hand side** | |

| **Description** | Sort by directory |
| :---- | :---- |
| **Left hand side** | ,bsd |
| **Right hand side** | |

| **Description** | Pin/Unpin Buffer |
| :---- | :---- |
| **Left hand side** | ,bP |
| **Right hand side** | |

| **Description** | Pick Buffer |
| :---- | :---- |
| **Left hand side** | ,bp |
| **Right hand side** | |

| **Description** | Move next |
| :---- | :---- |
| **Left hand side** | ,bn |
| **Right hand side** | |

| **Description** | Close Right |
| :---- | :---- |
| **Left hand side** | ,br |
| **Right hand side** | |

| **Description** | Close Left |
| :---- | :---- |
| **Left hand side** | ,bl |
| **Right hand side** | |

| **Description** | diff file |
| :---- | :---- |
| **Left hand side** | ,gd |
| **Right hand side** | |

| **Description** | status |
| :---- | :---- |
| **Left hand side** | ,gs |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,dt |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,dO |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,do |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,di |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,dh |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,dd |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,dc |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,db |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,da |
| **Right hand side** | |

| **Description** | multicursor |
| :---- | :---- |
| **Left hand side** | ,M |
| **Right hand side** | |

| **Description** | lazygit |
| :---- | :---- |
| **Left hand side** | ,gg |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,Dd |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,Dc |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,Di |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,Da |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,DA |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,DK |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,Dk |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,Dt |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,Dh |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,Dg |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,Ds |
| **Right hand side** | |

| **Description** | diff hunk |
| :---- | :---- |
| **Left hand side** | ,ghd |
| **Right hand side** | |

| **Description** | undo stage |
| :---- | :---- |
| **Left hand side** | ,ghu |
| **Right hand side** | |

| **Description** | toggle deleted |
| :---- | :---- |
| **Left hand side** | ,ght |
| **Right hand side** | |

| **Description** | stage buffer |
| :---- | :---- |
| **Left hand side** | ,ghS |
| **Right hand side** | |

| **Description** | stage hunk |
| :---- | :---- |
| **Left hand side** | ,ghs |
| **Right hand side** | |

| **Description** | reset hunk |
| :---- | :---- |
| **Left hand side** | ,ghr |
| **Right hand side** | |

| **Description** | reset buffer |
| :---- | :---- |
| **Left hand side** | ,ghR |
| **Right hand side** | |

| **Description** | preview |
| :---- | :---- |
| **Left hand side** | ,ghp |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;lt&gt;&lt;lt&gt; |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;lt&gt; |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | == |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | = |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &gt;&gt; |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &gt; |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | H |
| **Right hand side** | ^ |

| **Description** | |
| :---- | :---- |
| **Left hand side** | K |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | L |
| **Right hand side** | &lt;Cmd&gt;lua vim.lsp.buf.signature_help()&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | P |
| **Right hand side** | &lt;Cmd&gt;lua require('ecovim.plugins.telescope.pickers.multi-rg')()&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | Q |
| **Right hand side** | :lua require('mini.bufremove').delete(0, false)&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | X |
| **Right hand side** | "_X |

| **Description** | Nvim builtin |
| :---- | :---- |
| **Left hand side** | Y |
| **Right hand side** | y$ |

| **Description** | |
| :---- | :---- |
| **Left hand side** | [g |
| **Right hand side** | &lt;Cmd&gt;lua vim.diagnostic.goto_prev({ float = { border = 'rounded', max_width = 100 }})&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | [% |
| **Right hand side** | &lt;Plug&gt;(MatchitNormalMultiBackward) |

| **Description** | Previous todo comment |
| :---- | :---- |
| **Left hand side** | [t |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ]g |
| **Right hand side** | &lt;Cmd&gt;lua vim.diagnostic.goto_next({ float = { border = 'rounded', max_width = 100 }})&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ]% |
| **Right hand side** | &lt;Plug&gt;(MatchitNormalMultiForward) |

| **Description** | Next todo comment |
| :---- | :---- |
| **Left hand side** | ]t |
| **Right hand side** | |

| **Description** | Change a surrounding pair, putting replacements on new lines |
| :---- | :---- |
| **Left hand side** | cS |
| **Right hand side** | &lt;Plug&gt;(nvim-surround-change-line) |

| **Description** | Change a surrounding pair |
| :---- | :---- |
| **Left hand side** | cs |
| **Right hand side** | &lt;Plug&gt;(nvim-surround-change) |

| **Description** | Delete a surrounding pair |
| :---- | :---- |
| **Left hand side** | ds |
| **Right hand side** | &lt;Plug&gt;(nvim-surround-delete) |

| **Description** | |
| :---- | :---- |
| **Left hand side** | gP |
| **Right hand side** | &lt;Plug&gt;(printer_print)iw |

| **Description** | Open URL |
| :---- | :---- |
| **Left hand side** | gh |
| **Right hand side** | &lt;Cmd&gt;OpenRepo&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | gl |
| **Right hand side** | &lt;Cmd&gt;lua vim.diagnostic.open_float({ border = 'rounded', max_width = 100 })&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | gx |
| **Right hand side** | &lt;Cmd&gt;silent execute '!xdg-open ' . shellescape('&lt;lt&gt;cWORD&gt;')&lt;CR&gt; |

| **Description** | Operator keymap for printer.nvim |
| :---- | :---- |
| **Left hand side** | gp |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | gn |
| **Right hand side** | :bn&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | g% |
| **Right hand side** | &lt;Plug&gt;(MatchitNormalBackward) |

| **Description** | |
| :---- | :---- |
| **Left hand side** | gs |
| **Right hand side** | &lt;Plug&gt;(Switch) |

| **Description** | Comment insert end of line |
| :---- | :---- |
| **Left hand side** | gcA |
| **Right hand side** | |

| **Description** | Comment insert above |
| :---- | :---- |
| **Left hand side** | gcO |
| **Right hand side** | |

| **Description** | Comment insert below |
| :---- | :---- |
| **Left hand side** | gco |
| **Right hand side** | |

| **Description** | Comment toggle current block |
| :---- | :---- |
| **Left hand side** | gbc |
| **Right hand side** | |

| **Description** | Comment toggle current line |
| :---- | :---- |
| **Left hand side** | gcc |
| **Right hand side** | |

| **Description** | Comment toggle blockwise |
| :---- | :---- |
| **Left hand side** | gb |
| **Right hand side** | &lt;Plug&gt;(comment_toggle_blockwise) |

| **Description** | Comment toggle linewise |
| :---- | :---- |
| **Left hand side** | gc |
| **Right hand side** | &lt;Plug&gt;(comment_toggle_linewise) |

| **Description** | Align with preview |
| :---- | :---- |
| **Left hand side** | gA |
| **Right hand side** | |

| **Description** | Align |
| :---- | :---- |
| **Left hand side** | ga |
| **Right hand side** | |

| **Description** | Move to right "around" |
| :---- | :---- |
| **Left hand side** | g] |
| **Right hand side** | |

| **Description** | Move to left "around" |
| :---- | :---- |
| **Left hand side** | g[ |
| **Right hand side** | |

| **Description** | Toggle Split/Join |
| :---- | :---- |
| **Left hand side** | gJ |
| **Right hand side** | |

| **Description** | LSP Implementations |
| :---- | :---- |
| **Left hand side** | gm |
| **Right hand side** | |

| **Description** | LSP Definition |
| :---- | :---- |
| **Left hand side** | gd |
| **Right hand side** | |

| **Description** | LSP References |
| :---- | :---- |
| **Left hand side** | gr |
| **Right hand side** | |

| **Description** | LSP Type Definitions |
| :---- | :---- |
| **Left hand side** | gy |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | s |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | x |
| **Right hand side** | "_x |

| **Description** | Add a surrounding pair around the current line, on new lines (normal mode) |
| :---- | :---- |
| **Left hand side** | ySS |
| **Right hand side** | &lt;Plug&gt;(nvim-surround-normal-cur-line) |

| **Description** | Add a surrounding pair around a motion, on new lines (normal mode) |
| :---- | :---- |
| **Left hand side** | yS |
| **Right hand side** | &lt;Plug&gt;(nvim-surround-normal-line) |

| **Description** | Add a surrounding pair around the current line (normal mode) |
| :---- | :---- |
| **Left hand side** | yss |
| **Right hand side** | &lt;Plug&gt;(nvim-surround-normal-cur) |

| **Description** | Add a surrounding pair around a motion (normal mode) |
| :---- | :---- |
| **Left hand side** | ys |
| **Right hand side** | &lt;Plug&gt;(nvim-surround-normal) |

| **Description** | |
| :---- | :---- |
| **Left hand side** | zr |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | zM |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | zR |
| **Right hand side** | |

| **Description** | Get text out of textobject formatted for debug printing |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(printer_print) |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;luasnip-expand-repeat |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;luasnip-delete-check |
| **Right hand side** | |

| **Description** | Increase window width |
| :---- | :---- |
| **Left hand side** | &lt;C-Right&gt; |
| **Right hand side** | &lt;Cmd&gt;vertical resize +2&lt;CR&gt; |

| **Description** | Decrease window width |
| :---- | :---- |
| **Left hand side** | &lt;C-Left&gt; |
| **Right hand side** | &lt;Cmd&gt;vertical resize -2&lt;CR&gt; |

| **Description** | Increase window height |
| :---- | :---- |
| **Left hand side** | &lt;C-Up&gt; |
| **Right hand side** | &lt;Cmd&gt;resize +2&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;C-Space&gt; |
| **Right hand side** | &lt;Cmd&gt;lua vim.lsp.buf.code_action()&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;C-X&gt; |
| **Right hand side** | :if !switch#Switch({'reverse': 1}) &#124; call speeddating#increment(-v:count1) | endif&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;C-A&gt; |
| **Right hand side** | :if !switch#Switch() &#124; call speeddating#increment(v:count1) | endif&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;S-Tab&gt; |
| **Right hand side** | :BufferLineCyclePrev&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;C-P&gt; |
| **Right hand side** | &lt;Cmd&gt;lua require('ecovim.plugins.telescope').project_files()&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;C-S&gt; |
| **Right hand side** | :w&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;C-K&gt; |
| **Right hand side** | &lt;C-W&gt;k |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;C-J&gt; |
| **Right hand side** | &lt;C-W&gt;j |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;C-H&gt; |
| **Right hand side** | &lt;C-W&gt;h |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(MatchitNormalMultiForward) |
| **Right hand side** | :&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(MatchitNormalMultiBackward) |
| **Right hand side** | :&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(MatchitNormalBackward) |
| **Right hand side** | :&lt;C-U&gt;call matchit#Match_wrapper('',0,'n')&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(MatchitNormalForward) |
| **Right hand side** | :&lt;C-U&gt;call matchit#Match_wrapper('',1,'n')&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(SwitchReverse) |
| **Right hand side** | :set opfunc=switch#OpfuncReverse&lt;CR&gt;g@l |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(Switch) |
| **Right hand side** | :set opfunc=switch#OpfuncForward&lt;CR&gt;g@l |

| **Description** | Comment toggle blockwise with count |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(comment_toggle_blockwise_count) |
| **Right hand side** | |

| **Description** | Comment toggle linewise with count |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(comment_toggle_linewise_count) |
| **Right hand side** | |

| **Description** | Comment toggle current block |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(comment_toggle_blockwise_current) |
| **Right hand side** | |

| **Description** | Comment toggle current line |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(comment_toggle_linewise_current) |
| **Right hand side** | |

| **Description** | Comment toggle blockwise |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(comment_toggle_blockwise) |
| **Right hand side** | |

| **Description** | Comment toggle linewise |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(comment_toggle_linewise) |
| **Right hand side** | |

| **Description** | Git Conflict: Previous Conflict |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(git-conflict-prev-conflict) |
| **Right hand side** | &lt;Cmd&gt;GitConflictPrevConflict&lt;CR&gt; |

| **Description** | Git Conflict: Next Conflict |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(git-conflict-next-conflict) |
| **Right hand side** | &lt;Cmd&gt;GitConflictNextConflict&lt;CR&gt; |

| **Description** | Git Conflict: Choose Theirs |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(git-conflict-theirs) |
| **Right hand side** | &lt;Cmd&gt;GitConflictChooseTheirs&lt;CR&gt; |

| **Description** | Git Conflict: Choose None |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(git-conflict-none) |
| **Right hand side** | &lt;Cmd&gt;GitConflictChooseNone&lt;CR&gt; |

| **Description** | Git Conflict: Choose Both |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(git-conflict-both) |
| **Right hand side** | &lt;Cmd&gt;GitConflictChooseBoth&lt;CR&gt; |

| **Description** | Git Conflict: Choose Ours |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(git-conflict-ours) |
| **Right hand side** | &lt;Cmd&gt;GitConflictChooseOurs&lt;CR&gt; |

| **Description** | Toggle Terminal |
| :---- | :---- |
| **Left hand side** | &lt;F12&gt; |
| **Right hand side** | &lt;Cmd&gt;execute v:count . "ToggleTerm"&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;PlenaryTestFile |
| **Right hand side** | :lua require('plenary.test_harness').test_directory(vim.fn.expand("%:p"))&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;SpeedDatingFallbackDown |
| **Right hand side** | &lt;C-X&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;SpeedDatingFallbackUp |
| **Right hand side** | &lt;C-A&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;SpeedDatingNowUTC |
| **Right hand side** | :&lt;C-U&gt;call speeddating#timestamp(1,v:count)&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;SpeedDatingNowLocal |
| **Right hand side** | :&lt;C-U&gt;call speeddating#timestamp(0,v:count)&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;SpeedDatingDown |
| **Right hand side** | :&lt;C-U&gt;call speeddating#increment(-v:count1)&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;SpeedDatingUp |
| **Right hand side** | :&lt;C-U&gt;call speeddating#increment(v:count1)&lt;CR&gt; |

| **Description** | Change a surrounding pair, putting replacements on new lines |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(nvim-surround-change-line) |
| **Right hand side** | |

| **Description** | Change a surrounding pair |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(nvim-surround-change) |
| **Right hand side** | |

| **Description** | Delete a surrounding pair |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(nvim-surround-delete) |
| **Right hand side** | |

| **Description** | Add a surrounding pair around the current line, on new lines (normal mode) |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(nvim-surround-normal-cur-line) |
| **Right hand side** | |

| **Description** | Add a surrounding pair around a motion, on new lines (normal mode) |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(nvim-surround-normal-line) |
| **Right hand side** | |

| **Description** | Add a surrounding pair around the current line (normal mode) |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(nvim-surround-normal-cur) |
| **Right hand side** | |

| **Description** | Add a surrounding pair around a motion (normal mode) |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(nvim-surround-normal) |
| **Right hand side** | |

| **Description** | Go to buffer 9 |
| :---- | :---- |
| **Left hand side** | &lt;M-9&gt; |
| **Right hand side** | |

| **Description** | Go to buffer 8 |
| :---- | :---- |
| **Left hand side** | &lt;M-8&gt; |
| **Right hand side** | |

| **Description** | Go to buffer 7 |
| :---- | :---- |
| **Left hand side** | &lt;M-7&gt; |
| **Right hand side** | |

| **Description** | Go to buffer 6 |
| :---- | :---- |
| **Left hand side** | &lt;M-6&gt; |
| **Right hand side** | |

| **Description** | Go to buffer 5 |
| :---- | :---- |
| **Left hand side** | &lt;M-5&gt; |
| **Right hand side** | |

| **Description** | Go to buffer 4 |
| :---- | :---- |
| **Left hand side** | &lt;M-4&gt; |
| **Right hand side** | |

| **Description** | Go to buffer 2 |
| :---- | :---- |
| **Left hand side** | &lt;M-2&gt; |
| **Right hand side** | |

| **Description** | Go to buffer 1 |
| :---- | :---- |
| **Left hand side** | &lt;M-1&gt; |
| **Right hand side** | |

| **Description** | Go to buffer 3 |
| :---- | :---- |
| **Left hand side** | &lt;M-3&gt; |
| **Right hand side** | |

| **Description** | multicursor down |
| :---- | :---- |
| **Left hand side** | &lt;C-Down&gt; |
| **Right hand side** | |

| **Description** | NvimTree |
| :---- | :---- |
| **Left hand side** | &lt;C-E&gt; |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;C-L&gt; |
| **Right hand side** | &lt;C-W&gt;l |


### Visual mode keymaps

| **Description** | Nvim builtin |
| :---- | :---- |
| **Left hand side** | # |
| **Right hand side** | y?\V&lt;C-R&gt;"&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | % |
| **Right hand side** | &lt;Plug&gt;(MatchitVisualForward) |

| **Description** | Nvim builtin |
| :---- | :---- |
| **Left hand side** | * |
| **Right hand side** | y/\V&lt;C-R&gt;"&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,cf |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ,ca |
| **Right hand side** | &lt;Cmd&gt;'&lt;lt&gt;,'&gt;lua vim.lsp.buf.code_action()&lt;CR&gt; |

| **Description** | Terminal Send |
| :---- | :---- |
| **Left hand side** | ,ts |
| **Right hand side** | |

| **Description** | comment box |
| :---- | :---- |
| **Left hand side** | ,ac |
| **Right hand side** | &lt;Cmd&gt;lua require('comment-box').lbox()&lt;CR&gt; |

| **Description** | refactor |
| :---- | :---- |
| **Left hand side** | ,pr |
| **Right hand side** | |

| **Description** | multicursor |
| :---- | :---- |
| **Left hand side** | ,M |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;lt&gt; |
| **Right hand side** | &lt;lt&gt;gv |

| **Description** | |
| :---- | :---- |
| **Left hand side** | = |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &gt; |
| **Right hand side** | &gt;gv |

| **Description** | |
| :---- | :---- |
| **Left hand side** | J |
| **Right hand side** | :move '&gt;+1&lt;CR&gt;gv-gv |

| **Description** | |
| :---- | :---- |
| **Left hand side** | K |
| **Right hand side** | :move '&lt;lt&gt;-2&lt;CR&gt;gv-gv |

| **Description** | Add a surrounding pair around a visual selection |
| :---- | :---- |
| **Left hand side** | S |
| **Right hand side** | &lt;Plug&gt;(nvim-surround-visual) |

| **Description** | |
| :---- | :---- |
| **Left hand side** | X |
| **Right hand side** | "_X |

| **Description** | |
| :---- | :---- |
| **Left hand side** | [% |
| **Right hand side** | &lt;Plug&gt;(MatchitVisualMultiBackward) |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ]% |
| **Right hand side** | &lt;Plug&gt;(MatchitVisualMultiForward) |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ` |
| **Right hand side** | u |

| **Description** | |
| :---- | :---- |
| **Left hand side** | a% |
| **Right hand side** | &lt;Plug&gt;(MatchitVisualTextObject) |

| **Description** | Around last textobject |
| :---- | :---- |
| **Left hand side** | al |
| **Right hand side** | |

| **Description** | Around next textobject |
| :---- | :---- |
| **Left hand side** | an |
| **Right hand side** | |

| **Description** | Around textobject |
| :---- | :---- |
| **Left hand side** | a |
| **Right hand side** | |

| **Description** | Operator keymap for printer.nvim |
| :---- | :---- |
| **Left hand side** | gp |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | g% |
| **Right hand side** | &lt;Plug&gt;(MatchitVisualBackward) |

| **Description** | Move to right "around" |
| :---- | :---- |
| **Left hand side** | g] |
| **Right hand side** | |

| **Description** | Move to left "around" |
| :---- | :---- |
| **Left hand side** | g[ |
| **Right hand side** | |

| **Description** | Align with preview |
| :---- | :---- |
| **Left hand side** | gA |
| **Right hand side** | |

| **Description** | Align |
| :---- | :---- |
| **Left hand side** | ga |
| **Right hand side** | |

| **Description** | Comment toggle blockwise (visual) |
| :---- | :---- |
| **Left hand side** | gb |
| **Right hand side** | &lt;Plug&gt;(comment_toggle_blockwise_visual) |

| **Description** | Comment toggle linewise (visual) |
| :---- | :---- |
| **Left hand side** | gc |
| **Right hand side** | &lt;Plug&gt;(comment_toggle_linewise_visual) |

| **Description** | Add a surrounding pair around a visual selection, on new lines |
| :---- | :---- |
| **Left hand side** | gS |
| **Right hand side** | &lt;Plug&gt;(nvim-surround-visual-line) |

| **Description** | Inside last textobject |
| :---- | :---- |
| **Left hand side** | il |
| **Right hand side** | |

| **Description** | Inside next textobject |
| :---- | :---- |
| **Left hand side** | in |
| **Right hand side** | |

| **Description** | Inside textobject |
| :---- | :---- |
| **Left hand side** | i |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | p |
| **Right hand side** | "_dP |

| **Description** | |
| :---- | :---- |
| **Left hand side** | s |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | x |
| **Right hand side** | "_x |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;luasnip-expand-repeat |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;M-`&gt; |
| **Right hand side** | U |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(MatchitVisualTextObject) |
| **Right hand side** | &lt;Plug&gt;(MatchitVisualMultiBackward)o&lt;Plug&gt;(MatchitVisualMultiForward) |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(MatchitVisualMultiForward) |
| **Right hand side** | :&lt;C-U&gt;call matchit#MultiMatch("W",  "n")&lt;CR&gt;m'gv`` |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(MatchitVisualMultiBackward) |
| **Right hand side** | :&lt;C-U&gt;call matchit#MultiMatch("bW", "n")&lt;CR&gt;m'gv`` |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(MatchitVisualBackward) |
| **Right hand side** | :&lt;C-U&gt;call matchit#Match_wrapper('',0,'v')&lt;CR&gt;m'gv`` |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(MatchitVisualForward) |
| **Right hand side** | :&lt;C-U&gt;call matchit#Match_wrapper('',1,'v')&lt;CR&gt;:if col("''") != col("$") &#124; exe ":normal! m'" | endif&lt;CR&gt;gv`` |

| **Description** | Comment toggle blockwise (visual) |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(comment_toggle_blockwise_visual) |
| **Right hand side** | &lt;Esc&gt;&lt;Cmd&gt;lua require("Comment.api").locked("toggle.blockwise")(vim.fn.visualmode())&lt;CR&gt; |

| **Description** | Comment toggle linewise (visual) |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(comment_toggle_linewise_visual) |
| **Right hand side** | &lt;Esc&gt;&lt;Cmd&gt;lua require("Comment.api").locked("toggle.linewise")(vim.fn.visualmode())&lt;CR&gt; |

| **Description** | Add a surrounding pair around a visual selection, on new lines |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(nvim-surround-visual-line) |
| **Right hand side** | &lt;Esc&gt;&lt;Cmd&gt;lua require'nvim-surround'.visual_surround({ line_mode = true })&lt;CR&gt; |

| **Description** | Add a surrounding pair around a visual selection |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(nvim-surround-visual) |
| **Right hand side** | &lt;Esc&gt;&lt;Cmd&gt;lua require'nvim-surround'.visual_surround({ line_mode = false })&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;SpeedDatingDown |
| **Right hand side** | :&lt;C-U&gt;call speeddating#incrementvisual(-v:count1)&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;SpeedDatingUp |
| **Right hand side** | :&lt;C-U&gt;call speeddating#incrementvisual(v:count1)&lt;CR&gt; |


### Operator mode keymaps

| **Description** | |
| :---- | :---- |
| **Left hand side** | % |
| **Right hand side** | &lt;Plug&gt;(MatchitOperationForward) |

| **Description** | |
| :---- | :---- |
| **Left hand side** | [% |
| **Right hand side** | &lt;Plug&gt;(MatchitOperationMultiBackward) |

| **Description** | |
| :---- | :---- |
| **Left hand side** | ]% |
| **Right hand side** | &lt;Plug&gt;(MatchitOperationMultiForward) |

| **Description** | Around last textobject |
| :---- | :---- |
| **Left hand side** | al |
| **Right hand side** | |

| **Description** | Around next textobject |
| :---- | :---- |
| **Left hand side** | an |
| **Right hand side** | |

| **Description** | Around textobject |
| :---- | :---- |
| **Left hand side** | a |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | g% |
| **Right hand side** | &lt;Plug&gt;(MatchitOperationBackward) |

| **Description** | Move to right "around" |
| :---- | :---- |
| **Left hand side** | g] |
| **Right hand side** | |

| **Description** | Move to left "around" |
| :---- | :---- |
| **Left hand side** | g[ |
| **Right hand side** | |

| **Description** | Inside last textobject |
| :---- | :---- |
| **Left hand side** | il |
| **Right hand side** | |

| **Description** | Inside next textobject |
| :---- | :---- |
| **Left hand side** | in |
| **Right hand side** | |

| **Description** | Inside textobject |
| :---- | :---- |
| **Left hand side** | i |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | s |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;luasnip-expand-repeat |
| **Right hand side** | |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(MatchitOperationMultiForward) |
| **Right hand side** | :&lt;C-U&gt;call matchit#MultiMatch("W",  "o")&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(MatchitOperationMultiBackward) |
| **Right hand side** | :&lt;C-U&gt;call matchit#MultiMatch("bW", "o")&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(MatchitOperationBackward) |
| **Right hand side** | :&lt;C-U&gt;call matchit#Match_wrapper('',0,'o')&lt;CR&gt; |

| **Description** | |
| :---- | :---- |
| **Left hand side** | &lt;Plug&gt;(MatchitOperationForward) |
| **Right hand side** | :&lt;C-U&gt;call matchit#Match_wrapper('',1,'o')&lt;CR&gt; |


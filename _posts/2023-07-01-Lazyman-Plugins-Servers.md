---
title: Lazyman Neovim Configuration Plugins and Language Servers
author: doctorfree
date: 2023-07-01 15:25:00 +0800
tags: [neovim, config, configuration, features, lazyman, plugins, servers, language]
pin: false
img_path: "/posts/20230701"
---

## Language Servers supported in the Lazyman Neovim configuration

| **Lazyman** | **Neovim** | **Configuration** | **Language** | **Servers** |
| :---------- | :--------: | :---------------: | :----------: | ----------: |
| `ansiblels` | `astro` | `awk_ls` | `bashls` | `ccls` |
| `clangd` | `cmake` | `cssmodules_ls` | `denols` | `dockerls` |
| `eslint` | `gopls` | `graphql` | `html` | `jdtls` |
| `jsonls` | `julials` | `ltex` | `lua_ls` | `marksman` |
| `pylsp` | `pyright` | `rust_analyzer` | `sqlls` | `svelte` |
| `tailwindcss` | `taplo` | `texlab` | `tflint` | `tsserver` |
| `vimls` | `yamlls` | `zk` | | |

## Plugins used in the Lazyman Neovim configuration

### AI

- [jackMort/ChatGPT.nvim](https://dotfyle.com/plugins/jackMort/ChatGPT.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### bars-and-lines

- [m4xshen/smartcolumn.nvim](https://dotfyle.com/plugins/m4xshen/smartcolumn.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [utilyre/barbecue.nvim](https://dotfyle.com/plugins/utilyre/barbecue.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [SmiteshP/nvim-navic](https://dotfyle.com/plugins/SmiteshP/nvim-navic){:target="_blank"}{:rel="noopener noreferrer"}
- [luukvbaal/statuscol.nvim](https://dotfyle.com/plugins/luukvbaal/statuscol.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### code-runner

- [michaelb/sniprun](https://dotfyle.com/plugins/michaelb/sniprun){:target="_blank"}{:rel="noopener noreferrer"}

### color

- [NvChad/nvim-colorizer.lua](https://dotfyle.com/plugins/NvChad/nvim-colorizer.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/twilight.nvim](https://dotfyle.com/plugins/folke/twilight.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [xiyaowong/nvim-transparent](https://dotfyle.com/plugins/xiyaowong/nvim-transparent){:target="_blank"}{:rel="noopener noreferrer"}
- [uga-rosa/ccc.nvim](https://dotfyle.com/plugins/uga-rosa/ccc.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### colorscheme

- [folke/tokyonight.nvim](https://dotfyle.com/plugins/folke/tokyonight.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [catppuccin/nvim](https://dotfyle.com/plugins/catppuccin/nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [olimorris/onedarkpro.nvim](https://dotfyle.com/plugins/olimorris/onedarkpro.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [rebelot/kanagawa.nvim](https://dotfyle.com/plugins/rebelot/kanagawa.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [Mofiqul/dracula.nvim](https://dotfyle.com/plugins/Mofiqul/dracula.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [EdenEast/nightfox.nvim](https://dotfyle.com/plugins/EdenEast/nightfox.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [neanias/everforest-nvim](https://dotfyle.com/plugins/neanias/everforest-nvim){:target="_blank"}{:rel="noopener noreferrer"}

### command-line

- [gelguy/wilder.nvim](https://dotfyle.com/plugins/gelguy/wilder.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### comment

- [echasnovski/mini.comment](https://dotfyle.com/plugins/echasnovski/mini.comment){:target="_blank"}{:rel="noopener noreferrer"}
- [JoosepAlviste/nvim-ts-context-commentstring](https://dotfyle.com/plugins/JoosepAlviste/nvim-ts-context-commentstring){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/todo-comments.nvim](https://dotfyle.com/plugins/folke/todo-comments.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### completion

- [zbirenbaum/copilot.lua](https://dotfyle.com/plugins/zbirenbaum/copilot.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [simrat39/rust-tools.nvim](https://dotfyle.com/plugins/simrat39/rust-tools.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [hrsh7th/nvim-cmp](https://dotfyle.com/plugins/hrsh7th/nvim-cmp){:target="_blank"}{:rel="noopener noreferrer"}

### cursorline

- [RRethy/vim-illuminate](https://dotfyle.com/plugins/RRethy/vim-illuminate){:target="_blank"}{:rel="noopener noreferrer"}

### debugging

- [rcarriga/nvim-dap-ui](https://dotfyle.com/plugins/rcarriga/nvim-dap-ui){:target="_blank"}{:rel="noopener noreferrer"}
- [mfussenegger/nvim-dap](https://dotfyle.com/plugins/mfussenegger/nvim-dap){:target="_blank"}{:rel="noopener noreferrer"}

### diagnostics

- [folke/trouble.nvim](https://dotfyle.com/plugins/folke/trouble.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### editing-support

- [echasnovski/mini.pairs](https://dotfyle.com/plugins/echasnovski/mini.pairs){:target="_blank"}{:rel="noopener noreferrer"}
- [filipdutescu/renamer.nvim](https://dotfyle.com/plugins/filipdutescu/renamer.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/zen-mode.nvim](https://dotfyle.com/plugins/folke/zen-mode.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [windwp/nvim-autopairs](https://dotfyle.com/plugins/windwp/nvim-autopairs){:target="_blank"}{:rel="noopener noreferrer"}
- [windwp/nvim-ts-autotag](https://dotfyle.com/plugins/windwp/nvim-ts-autotag){:target="_blank"}{:rel="noopener noreferrer"}
- [Wansmer/treesj](https://dotfyle.com/plugins/Wansmer/treesj){:target="_blank"}{:rel="noopener noreferrer"}

### file-explorer

- [kevinhwang91/rnvimr](https://dotfyle.com/plugins/kevinhwang91/rnvimr){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-neo-tree/neo-tree.nvim](https://dotfyle.com/plugins/nvim-neo-tree/neo-tree.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### fuzzy-finder

- [jvgrootveld/telescope-zoxide](https://dotfyle.com/plugins/jvgrootveld/telescope-zoxide){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-telescope/telescope.nvim](https://dotfyle.com/plugins/nvim-telescope/telescope.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### game

- [alanfortlink/blackjack.nvim](https://dotfyle.com/plugins/alanfortlink/blackjack.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [ThePrimeagen/vim-be-good](https://dotfyle.com/plugins/ThePrimeagen/vim-be-good){:target="_blank"}{:rel="noopener noreferrer"}
- [jim-fx/sudoku.nvim](https://dotfyle.com/plugins/jim-fx/sudoku.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### git

- [lewis6991/gitsigns.nvim](https://dotfyle.com/plugins/lewis6991/gitsigns.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [NeogitOrg/neogit](https://dotfyle.com/plugins/NeogitOrg/neogit){:target="_blank"}{:rel="noopener noreferrer"}
- [sindrets/diffview.nvim](https://dotfyle.com/plugins/sindrets/diffview.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### github

- [pwntester/octo.nvim](https://dotfyle.com/plugins/pwntester/octo.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### golang

- [ray-x/go.nvim](https://dotfyle.com/plugins/ray-x/go.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### indent

- [echasnovski/mini.indentscope](https://dotfyle.com/plugins/echasnovski/mini.indentscope){:target="_blank"}{:rel="noopener noreferrer"}
- [lukas-reineke/indent-blankline.nvim](https://dotfyle.com/plugins/lukas-reineke/indent-blankline.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### keybinding

- [anuvyklack/hydra.nvim](https://dotfyle.com/plugins/anuvyklack/hydra.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/which-key.nvim](https://dotfyle.com/plugins/folke/which-key.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### lsp

- [simrat39/symbols-outline.nvim](https://dotfyle.com/plugins/simrat39/symbols-outline.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [jose-elias-alvarez/null-ls.nvim](https://dotfyle.com/plugins/jose-elias-alvarez/null-ls.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [neovim/nvim-lspconfig](https://dotfyle.com/plugins/neovim/nvim-lspconfig){:target="_blank"}{:rel="noopener noreferrer"}
- [mfussenegger/nvim-jdtls](https://dotfyle.com/plugins/mfussenegger/nvim-jdtls){:target="_blank"}{:rel="noopener noreferrer"}
- [weilbith/nvim-code-action-menu](https://dotfyle.com/plugins/weilbith/nvim-code-action-menu){:target="_blank"}{:rel="noopener noreferrer"}
- [ray-x/lsp_signature.nvim](https://dotfyle.com/plugins/ray-x/lsp_signature.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [kosayoda/nvim-lightbulb](https://dotfyle.com/plugins/kosayoda/nvim-lightbulb){:target="_blank"}{:rel="noopener noreferrer"}
- [b0o/SchemaStore.nvim](https://dotfyle.com/plugins/b0o/SchemaStore.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [stevearc/aerial.nvim](https://dotfyle.com/plugins/stevearc/aerial.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [jose-elias-alvarez/typescript.nvim](https://dotfyle.com/plugins/jose-elias-alvarez/typescript.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [glepnir/lspsaga.nvim](https://dotfyle.com/plugins/glepnir/lspsaga.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### lsp-installer

- [williamboman/mason.nvim](https://dotfyle.com/plugins/williamboman/mason.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### markdown-and-latex

- [AckslD/nvim-FeMaco.lua](https://dotfyle.com/plugins/AckslD/nvim-FeMaco.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [toppair/peek.nvim](https://dotfyle.com/plugins/toppair/peek.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [ellisonleao/glow.nvim](https://dotfyle.com/plugins/ellisonleao/glow.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [iamcco/markdown-preview.nvim](https://dotfyle.com/plugins/iamcco/markdown-preview.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [frabjous/knap](https://dotfyle.com/plugins/frabjous/knap){:target="_blank"}{:rel="noopener noreferrer"}

### marks

- [ThePrimeagen/harpoon](https://dotfyle.com/plugins/ThePrimeagen/harpoon){:target="_blank"}{:rel="noopener noreferrer"}

### motion

- [gen740/SmoothCursor.nvim](https://dotfyle.com/plugins/gen740/SmoothCursor.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [phaazon/hop.nvim](https://dotfyle.com/plugins/phaazon/hop.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [ggandor/leap.nvim](https://dotfyle.com/plugins/ggandor/leap.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### note-taking

- [nvim-orgmode/orgmode](https://dotfyle.com/plugins/nvim-orgmode/orgmode){:target="_blank"}{:rel="noopener noreferrer"}
- [jbyuki/nabla.nvim](https://dotfyle.com/plugins/jbyuki/nabla.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [jakewvincent/mkdnflow.nvim](https://dotfyle.com/plugins/jakewvincent/mkdnflow.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-neorg/neorg](https://dotfyle.com/plugins/nvim-neorg/neorg){:target="_blank"}{:rel="noopener noreferrer"}
- [renerocksai/telekasten.nvim](https://dotfyle.com/plugins/renerocksai/telekasten.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [epwalsh/obsidian.nvim](https://dotfyle.com/plugins/epwalsh/obsidian.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### nvim-dev

- [anuvyklack/animation.nvim](https://dotfyle.com/plugins/anuvyklack/animation.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [ray-x/guihua.lua](https://dotfyle.com/plugins/ray-x/guihua.lua){:target="_blank"}{:rel="noopener noreferrer"}
- [folke/neodev.nvim](https://dotfyle.com/plugins/folke/neodev.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lua/popup.nvim](https://dotfyle.com/plugins/nvim-lua/popup.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [MunifTanjim/nui.nvim](https://dotfyle.com/plugins/MunifTanjim/nui.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-lua/plenary.nvim](https://dotfyle.com/plugins/nvim-lua/plenary.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### plugin-manager

- [folke/lazy.nvim](https://dotfyle.com/plugins/folke/lazy.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### preconfigured

- [ldelossa/nvim-ide](https://dotfyle.com/plugins/ldelossa/nvim-ide){:target="_blank"}{:rel="noopener noreferrer"}

### programming-languages-support

- [AckslD/swenv.nvim](https://dotfyle.com/plugins/AckslD/swenv.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### project

- [ahmedkhalf/project.nvim](https://dotfyle.com/plugins/ahmedkhalf/project.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### quickfix

- [kevinhwang91/nvim-bqf](https://dotfyle.com/plugins/kevinhwang91/nvim-bqf){:target="_blank"}{:rel="noopener noreferrer"}

### scrollbar

- [petertriho/nvim-scrollbar](https://dotfyle.com/plugins/petertriho/nvim-scrollbar){:target="_blank"}{:rel="noopener noreferrer"}

### scrolling

- [declancm/cinnamon.nvim](https://dotfyle.com/plugins/declancm/cinnamon.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [karb94/neoscroll.nvim](https://dotfyle.com/plugins/karb94/neoscroll.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### search

- [kevinhwang91/nvim-hlslens](https://dotfyle.com/plugins/kevinhwang91/nvim-hlslens){:target="_blank"}{:rel="noopener noreferrer"}

### session

- [jedrzejboczar/possession.nvim](https://dotfyle.com/plugins/jedrzejboczar/possession.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### snippet

- [L3MON4D3/LuaSnip](https://dotfyle.com/plugins/L3MON4D3/LuaSnip){:target="_blank"}{:rel="noopener noreferrer"}

### split-and-window

- [anuvyklack/windows.nvim](https://dotfyle.com/plugins/anuvyklack/windows.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### startup

- [glepnir/dashboard-nvim](https://dotfyle.com/plugins/glepnir/dashboard-nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [goolord/alpha-nvim](https://dotfyle.com/plugins/goolord/alpha-nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [echasnovski/mini.starter](https://dotfyle.com/plugins/echasnovski/mini.starter){:target="_blank"}{:rel="noopener noreferrer"}

### statusline

- [nvim-lualine/lualine.nvim](https://dotfyle.com/plugins/nvim-lualine/lualine.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### syntax

- [m-demare/hlargs.nvim](https://dotfyle.com/plugins/m-demare/hlargs.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [kylechui/nvim-surround](https://dotfyle.com/plugins/kylechui/nvim-surround){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter-textobjects](https://dotfyle.com/plugins/nvim-treesitter/nvim-treesitter-textobjects){:target="_blank"}{:rel="noopener noreferrer"}
- [nvim-treesitter/nvim-treesitter](https://dotfyle.com/plugins/nvim-treesitter/nvim-treesitter){:target="_blank"}{:rel="noopener noreferrer"}

### tabline

- [akinsho/bufferline.nvim](https://dotfyle.com/plugins/akinsho/bufferline.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### test

- [nvim-neotest/neotest](https://dotfyle.com/plugins/nvim-neotest/neotest){:target="_blank"}{:rel="noopener noreferrer"}

### tmux

- [numToStr/Navigator.nvim](https://dotfyle.com/plugins/numToStr/Navigator.nvim){:target="_blank"}{:rel="noopener noreferrer"}

### treesitter-based

- [ziontee113/syntax-tree-surfer](https://dotfyle.com/plugins/ziontee113/syntax-tree-surfer){:target="_blank"}{:rel="noopener noreferrer"}
- [mfussenegger/nvim-ts-hint-textobject](https://dotfyle.com/plugins/mfussenegger/nvim-ts-hint-textobject){:target="_blank"}{:rel="noopener noreferrer"}

### utility

- [folke/noice.nvim](https://dotfyle.com/plugins/folke/noice.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [rcarriga/nvim-notify](https://dotfyle.com/plugins/rcarriga/nvim-notify){:target="_blank"}{:rel="noopener noreferrer"}
- [crusj/bookmarks.nvim](https://dotfyle.com/plugins/crusj/bookmarks.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [stevearc/dressing.nvim](https://dotfyle.com/plugins/stevearc/dressing.nvim){:target="_blank"}{:rel="noopener noreferrer"}
- [kevinhwang91/nvim-ufo](https://dotfyle.com/plugins/kevinhwang91/nvim-ufo){:target="_blank"}{:rel="noopener noreferrer"}

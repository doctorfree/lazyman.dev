---
title: Lazyman Install Location
author: doctorfree
date: 2023-08-28 15:25:00 +0800
tags: [neovim, config, install, lazyman, location]
pin: true
img_path: "/posts/20230828"
---

## Lazyman Version 4

The installation location of Lazyman changed with the release of
Lazyman v4.0.0r1 on August 28, 2023. Previous versions of Lazyman
were installed in `~/.config/nvim-Lazyman`. With version 4 the install
location changed to `~/.config/lazyman/Lazyman`.

For users installing Lazyman for the first time this change does not
present an issue. However, for users who have previously installed
Neovim configurations with Lazyman version 3 or earlier, the new
`lazyman` command would not recognize those configurations.

For this reason, Lazyman version 4 performs a configuration migration
for all Neovim configurations detected as having been installed with
a previous version of Lazyman.

## Lazyman Migration

Lazyman version 4 introduced a new location for Neovim configurations
installed using the `lazyman` command: `~/.config/lazyman/<configname>`.
After updating from a version 3 or earlier Lazyman installation, any
previously installed Neovim configurations can be migrated.

The first time the version 4 or later `lazyman` command is run it will
prompt for migration if any older location configurations are found.
If migration at that time is not selected, it can be performed at a later
date with the command `lazyman migrate`.

Migration preserves any changes to installed configurations except for the
Lazyman Neovim configuration which is freshly cloned and initialized.
Dependencies and tools are installed during initial migration.

**Note:** migration only effects those users who have previously installed
Lazyman version 3 or earlier, have installed one or more Lazyman supported
Neovim configuration, and have updated with `lazyman -U`.

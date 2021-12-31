---
author: Alexandre Lamberty
title: Neovim
category: Editor 
tags: ["linux", "editor", "vim", "lua"]
created: 2021-11-11T17:30:39+01:00
updated: 2021-11-11T17:30:39+01:00
---
# Neovim

## Structure

$HOME /.cache/nvim/

$HOME /.config/nvim/

## Settings

## Spelling

## Plugins

## LSP

Easily configure with [nvim-lspconfig](https://github.com/neovim/nvim-lspconfig)

You can automatically install the lsp you want this plugin
[nvim-lsp-installer](https://github.com/williamboman/nvim-lsp-installer)

Check these common [Server configurations](https://github.com/neovim/nvim-lspconfig/blob/master/doc/server_configurations.md)

## DAP

As for the Lsp's there is a neovim plugin that leverage the task of installing
yourself the DAP you need. Check out [DAPInstall]().

Or you can install manually each protocol. Refer to this page[^1].

## References

- [Neovim](https://neovim.io)
- [Documentation - Neovim](https://neovim.io/doc/general/)
- [Documentation Lua - Neovim](https://neovim.io/doc/user/lua.html)
- [Neovim - GitHub](https://github.com/neovim/neovim)
- [Neovim Lua Guide - Github](https://github.com/nanotee/nvim-lua-guide)
- [Nvim-Dap](https://github.com/mfussenegger/nvim-dap)
- [^1]: [Debug Adapter Installation](https://github.com/mfussenegger/nvim-dap/wiki/Debug-Adapter-installation)
- [Debug Adapters](https://microsoft.github.io/debug-adapter-protocol/implementors/adapters/)

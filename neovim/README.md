---
author: Alexandre Lamberty
title: Neovim
category: Editor
tags: [text, editor, vim, lua]
created: 2021-11-11T17:30:39+01:00
updated: 2021-11-11T17:30:39+01:00
---

# Neovim

## Lua

## Structure

## Plugins

## Spelling

## LSP

### Keybinds

gd Jumps to the declaration
gD Jumps to the definition
gi Lists all the implementations
gr Lists all the references
K Displays hover information
<C-k> Displays signature information
gl Show line diagnostic

## DAP

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

### PHP 

For neovim lsp and dap support you can check out this post [Neovim LSP and DAP]()

Install Php and Xdebug and vscode-php-debug 

Verify your configuration


#### Configuration

Specify your php config in an `php.ini` file

```ini
zend_extension = xdebug
xdebug.client_port = 9000
xdebug.mode = debug
xdebug.start_with_request = yes
```

Check php with your custom config

```bash
php -c php.ini -v
```

```bash
PHP 8.0.14 (cli) (built: Dec 17 2021 14:16:47) ( NTS )
Copyright (c) The PHP Group
Zend Engine v4.0.14, Copyright (c) Zend Technologies
    with Xdebug v3.1.2, Copyright (c) 2002-2021, by Derick Rethans
```

```bash
php -c php.ini -S localhost:9090
```

`info.php`
```php
<?php echo phpinfo(); ?>
```

```
php -c php.ini -S localhost:9090 -t info.php
```

#### Debug

Install [vscode-php-debug]() and point your php dap adapter executable to 

Point your DAP 

```lua
dap.adapters.php = {
    type = 'executable',
    command = 'node',
    args = {os.getenv("HOME") .. '/path/to/vscode-php-debug/out/phpDebug.js'}
}
```
## References

- [Neovim](https://neovim.io)
- [Documentation - Neovim](https://neovim.io/doc/general/)
- [Documentation Lua - Neovim](https://neovim.io/doc/user/lua.html)
- [Neovim - GitHub](https://github.com/neovim/neovim)
- [Neovim Lua Guide - Github](https://github.com/nanotee/nvim-lua-guide)
- [Nvim-Dap](https://github.com/mfussenegger/nvim-dap)
- [^1]: [Debug Adapter Installation](https://github.com/mfussenegger/nvim-dap/wiki/Debug-Adapter-installation)
- [Debug Adapters](https://microsoft.github.io/debug-adapter-protocol/implementors/adapters/)
## References

- [Neovim](https://neovim.io)
- [Documentation - Neovim](https://neovim.io/doc/general/)
- [Documentation Lua - Neovim](https://neovim.io/doc/user/lua.html)
- [Neovim - Github](https://github.com/neovim/neovim)
- [Neovim Lua Guide - Github](https://github.com/nanotee/nvim-lua-guide)

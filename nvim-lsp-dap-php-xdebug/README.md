# Nvim LSP DAP PHP Xdebug

## Nvim lsp and dap

For neovim lsp and dap support you can check out this post [Neovim LSP and DAP]()

## Php and Xdebug

Install Php and Xdebug for your operating system

### Configuration

Specify your php config in an `php.ini` file

```ini
zend_extension = Xdebug
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

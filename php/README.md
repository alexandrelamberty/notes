---
author: Alexandre Lamberty
title: PHP 
description: |
 General-purpose scripting language geared towards web
 development
category: Programming language
tags: ["php","web","server"]
created: 2021-10-23T20:38:59+02:00
updated: 2021-10-23T20:38:59+02:00
---
# PHP

## Installation

```bash
php -v

PHP 8.0.14 (cli) (built: Dec 17 2021 14:16:47) ( NTS )
Copyright (c) The PHP Group
Zend Engine v4.0.14, Copyright (c) Zend Technologies
    with Xdebug v3.1.2, Copyright (c) 2002-2021, by Derick Retha
```

## Configuration
`php.ini`

```bash
php -c php.ini -v
```

## Composer

```bash
composer --version

Composer version 2.2.1 2021-12-22 22:21:31
```

## Class Dockblock

```php
<?php
/**
 * {SHORT_DESCRIPTION}
 *
 * {LONG_DESCRIPTION}
 *
 * {PHP_VERSION}
 *
 * {LICENSE}
 *
 * @category   CategoryName
 * @package    PackageName
 * @author     Original Author <author@example.com>
 * @author     Another Author <another@example.com>
 * @copyright  1997-2005 The PHP Group
 * @license    http://www.php.net/license/3_01.txt  PHP License 3.01
 * @version    SVN: $Id$
 * @link       http://pear.php.net/package/PackageName
 * @see        NetOther, Net_Sample::Net_Sample()
 * @since      File available since Release 1.2.0
 * @deprecated File deprecated in Release 2.0.0
 */

/*
* Place includes, constant defines and $_GLOBAL settings here.
* Make sure they have appropriate docblocks to avoid phpDocumentor
* construing they are documented by the page-level docblock.
*/

/**
 * Short description for class
 *
 * Long description for class (if any)...
 *
 * @category   module
 * @package    Php\Zend\Module\Auth
 * @author     Original Author <author@example.com>
 * @author     Another Author <another@example.com>
 * @copyright  2008-2014 MasFuego Inc.
 * @license   http://www.opensource.org/licenses/mit-license.html  MIT License

 *@version    Release: @package_version@
 * @link       http://www.mas-fuego.com/package/php/zend/module/authentification
 *@see        NetOther, Net_Sample::Net_Sample()
 * @since      Class available since Release 1.0.0
 *@deprecated Class deprecated in Release 2.0.0
 */
class Foo_Bar
{
}
?>
```

## References

<http://manual.phpdoc.org/HTMLSmartyConverter/HandS/phpDocumentor/tutorial_tags.pkg.html>

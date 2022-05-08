---
slug: PHP Composer Github Private Repo
title: PHP Composer Github Private Repo
description: How to create and use a private Composer package hosted on Github.
category: Programming
tags: ["php","composer","github","repository","private"]
---
# PHP Composer Github Private Repo

How to create and use a private Composer package hosted on Github.

We will create a library package and a project

## Library Project File Structure

    common-utils-library
    ├── src
    └── composer.json

`composer.json`

```json
{
  "name": "acme/common-utils",
  "type": "library",
  "autoload": {
    "psr-4": {
      "Acme\\": "src/Acme/"
    }
  }
}
```

## Consumer Project File Structure

    common-project
    ├── src
    └── composer.json

`composer.json`

```json
{
  "name": "acme/",
  "type": "project",
  "require": {
    "acme/common-utils": "dev-master"
  },
  "autoload": {
    "psr-4": {
      "Acme\\": "src/Acme"
    }
  },
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/USERNAME/acme/common-util"
    }
  ]
}
```

# Composer Private Repository Library

How to create and use private composer package for you in-house development.

## Creating the package

This is how our project look likes.

composer-lib
| composer.json
|  
\---src
\---Acme
\---Foo
Hello.php

Creating the package composer.json
{
"name": "acme/composer-lib",
"autoload": {
"psr-4": {
"Acme\\Foo\\": "src/Acme/Foo/"
}
}
}

Creating the Hello.php class

<?php
namespace Acme\Foo;

class Hello
{
   public function hello()
   {
       return "Hello";
   }
}

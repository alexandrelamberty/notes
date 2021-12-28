---
author: Alexandre Lamberty
title: Symfony 
description: |
 Set of reusable PHP components and a PHP framework to build web applications,
 APIs, microservices and web services
category: Framework
tags: ["php"]
created: 2021-04-06T13:34:30+02:00
updated: 2021-04-06T13:34:30+02:00
---
# Symfony

## Commands

composer create-project symfony/framework-standard-edition path/

php app/check.php

php app/console generate:bundle --namespace=Eevos/CMSBundle -format=yml
php app/console server:run

php app/console generate:doctrine:crud
php app/console cache:clear --env=dev

$ php app/console doctrine:database:drop --force
$ php app/console doctrine:database:create

## Doctrine

Create Database
php app/console doctrine:database:create
Update Schema
php app/console doctrine:schema:update --force
Generate Entity
php app/console doctrine:generate;entity
Generate Entities
php app/console doctrine:generate:entities Acme
Load Fixture
php app/console doctrine:fixture:load

## References 

- [Symfony](https://symfony.com/)
- [Twig](http://twig.sensiolabs.org/)

---
author: Alexandre Lamberty
title: Apache
description: Free and open-source cross-platform web server
category: Software
tags: ["apache","http","server"]
created: 2021-11-11T17:30:39+01:00
updated: 2021-11-11T17:30:39+01:00
---
# Apache HTTP Server

## Configuration

## Virtual Host

Running several name-based web sites on a single IP address.

> **_NOTE:_** Creating virtual host configurations on your Apache server does not
> magically cause DNS entries to be created for those host names. You must
> have the names in DNS, resolving to your IP address, or nobody else will
> be able to see your web site. You can put entries in your `hosts` file for
> local testing, but that will work only from the machine with those hosts
> entries.

```apache
NameVirtualHost neo-ws.lan:80
<VirtualHost neo-ws.lan:80>
    DocumentRoot "/projects/developement/web/eevos.neo-ws.lan/"
    ServerName eevos.neo-ws.lan
    <Directory "/projects/developement/web/eevos.neo-ws.lan/">
        AllowOverride All
        Require local
    </Directory>
</VirtualHost>
```



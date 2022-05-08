#  Naming Conventions and Organisation Schemes  

## Project

Main project named 

alexandrelamberty.com
hortus

## 

[rd] Reverse DNS (com.adobe)
[name] Project / component name

[rd].[name]

SQLite Manager
sqlite-manager

SQLite Manager Application
sqlite-manager-application

SQLite Manager Library
sqlite-manager-library


Project Source Archetype

Project
    Component
	    src
	        bin

Langues / Technologies

Actionscript
Flash
Flex
Desktop
Mobile
Web


be.eevos.app.shippingmanager
be.eevos.as3.document.library
be.eevos.flex.document.library
Be.eevos.java.document.library


## Project Name Rules

Project must explicitely

Project
The name of the project can be

Name		Movie Project
ID		movie-project
Package	be.eevos.movie

Application
The name followed by Application

Name		Desktop Movie Application
ID		    movie-application
Package	    be.eevos.movie.desktop.application

Name		Browser Movie Application
ID		    movie-application
Package	    be.eevos.movie.browser.application

Name		Mobile Movie Application
ID		    movie-application
Package	    be.eevos.movie.mobile.application

Library
The name followed by Library

Name		Movie Library
ID		    movie-library
Package	    be.eevos.library


## Package Name Rules

Domain name reverse name.technology.project.component


## Class Name Rules

Domain name reverse name.technology.project.component


## Commons names

business
model
domain
service
ui
view
controller
components

## Samples

Eevos Movie Management
Eevos AIR Movie Library Application			    be.eevos.air.movie.application
Eevos AIR Movie Domain Library			        be.eevos.air.movie.domain
Eevos AIR Movie Domain Service SQL Library		be.eevos.air.movie.service.sql
Eevos AIR Movie Domain Service AMF Library		be.eevos.air.movie.service.amf
Eevos AIR Movie User Interface Library			be.eevos.air.movie.ui


be
    eevos
        air
            movie
                application
                    controller  
                    model
                    view
                domain
                    model
                        ValueObjectClass
                    service
                        Service Interface Class
                            amf
                            Service implementation
                            sql
                            Service implementation

Views naming

templates / views / …

category
- list_product
- create_product
- read_product
- update_product


product
- list_product
- create_product
- read_product
- update_product

user



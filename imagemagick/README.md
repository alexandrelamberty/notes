---
author: Alexandre Lamberty
title: ImageMagick 
description: |
 Free and open-source cross-platform software suite for displaying, creating,
 converting, modifying, and editing raster images
category: Images
tags: ["imagemagick","image","manipulation"]
created: 2021-04-06T13:34:30+02:00
updated: 2021-04-06T13:34:30+02:00
---
# ImageMagick

## Tests 

magick convert -resize 460x460 -gravity center -fill white _.jpg
magick convert -resize 256x256 -gravity center -extent 256x256 _.jpg
magick convert -resize 460x460 \*.jpg
magick convert -geometry x300 _.jpg
magick convert -resize 256x256 -gravity center -extent 256x256 _.jpg
magick convert -resize 300x300 _.jpg
magick convert -resize 50% /resizes/_.jpg
magick mogrify -resize 460x460 -gravity Center -fill white \*.jpg
magick convert -resize 256x256 -gravity Center \*.jpg
magick mogrify -resize 840x840 -gravity Center -fill white _.jpg
magick mogrify -extent 840x840 -gravity Center -fill white _.jpg

## References

- [Imagemagick](http://www.imagemagick.org/script/index.php)

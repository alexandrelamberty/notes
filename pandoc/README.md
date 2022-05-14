---
author: Alexandre Lamberty
title: Pandoc 
description: | Free and open-source document converter, widely used as a
writing tool and as a basis for publishing workflows
category: Markup language
tags: [writing,markdown,converter,writing,publication]
created: 2021-10-23T20:38:59+02:00
updated: 2021-10-23T20:38:59+02:00
---

# Pandoc

## Usages

Transform Markdown to HTML

```bash
pandoc --standalone --from markdown Pandoc.md --to html5 index.html
```

## Templates

Copy the default template to a file

```bash
pandoc -D latex > template.latex
```

Use the template

```bash
pandoc -s -N --template=template.latex doc.md -o doc.pdf
```

## References

- [Pandoc](https://pandoc.org/)
- [User's Guide | Pandoc](https://pandoc.org/MANUAL.html)
- [Templates](https://pandoc.org/MANUAL.html#templates)

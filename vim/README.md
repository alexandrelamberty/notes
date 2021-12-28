---
author: Alexandre Lamberty
title: Vim 
description: Free and open-source, screen-based text editor program for Unix
category: Software
tags: ["vim","editor","text","cli","linux"]
created: 2021-04-06T13:34:31+02:00
updated: 2021-04-06T13:34:31+02:00
---
# Vim

## Config

set splitbelow splitright

## Modes

* Normal
* Insert
* Visual
* X

## Keybinds

## Functions

## Operators

{operator}{count}{motion}
{count}{operator}{motion}

`d` => "delete"
`c` => "change"

> => "indent"

y => "copy"
. => "repeat"
~ => "swap case"
gu => "make lowercase"
gU => "make uppercase"

## Motions

% => First matching paren / bracket

  - => Down to first non-blank character of line
  $ => To end of line
  f/F => Next occurence of char
  t/T => Before next occurence of char
  h/j/k/l => Left, down, uo; right
  ]m => Go the begining of next method
  w/w => "forward" Begining of next word
  b/B => "backward"
  e/E => "forward"

/,? => "search"

## Text Objects

{operator}{a|i}{text-object}

w => "word"
s => "sentance"
p => "paragraph"
"' => "quotes"
b => ()
B => {}
<> =>
[] =>
t => "tag"

## Tags

## Autocomplete 
- https://vim.fandom.com/wiki/Dictionary_completions

Ctrl+n - Everything
Ctrl+p - Everything

Ctrl+x / ctrl+] = Completion

Ctrl+x Ctrl+n - From current file
Ctrl+x Ctrl+F - From filenames
Ctrl+x Ctrl+J - From Tags

## File Browsing  

## Buffers

:e filename - edit another file
:ls - show current buffers
:b 2 - open buffer #2 in this window


## Split 

### Commands

:split filename - split window and load another file
:vsplit file - vertical split
:sview file - same as split, but readonly
:sf (FILE) - Split windows and :find (FILE)
:vert - Make any split {cmd} be vertical

### Keybinds

ctrl-w +/- increase decrease height
ctrl-w >/< increase decrease width
ctrl-w= - make all equal size
ctrl-w\_ - maximize current window
ctrl-w up arrow - move cursor up a window
ctrl-w ctrl-w - move cursor to another window (cycle)
<Ctrl+w> s - Split window
<Ctrl+w> v - Vertical split
<Ctrl+w> q - Close
<Ctrl+w> w - Alternate windows
<Ctrl+w> r - Rotate windows

## Tabs

:tabnew
:tabe


## Windows

:hide - close current window
:windo {cmd} - Execute cmd for all windows
:only - keep only this window open

## Characters

:set list 
:set listchars=eol:¬,tab:>·,trail:~,extends:>,precedes:<,space:·

## Formating

gq

=

## Filetype

/* vim: set filetype=idl : */ 

Type :setfiletype (with a space afterwards), then press Ctrl-d.

See :help cmdline-completion for more on autocompletion in vim's command line.

## Snippets

## References

- https://www.semicolonandsons.com/episode/Advanced-Vim-Workflows
- https://www.youtube.com/watch?v=futay9NjOac&ab_channel=Semicolon%26Sons
- https://blog.carbonfive.com/2011/10/17/vim-text-objects-the-definitive-guide/
- https://www.vi-improved.org/recommendations/#bufexplorer-ctrl-p-gtfo-minibufexpl-nerdtree-vinegar
- http://vimcasts.org/blog/2012/08/on-sharpening-the-saw/
- https://www.youtube.com/watch?v=9jzWDr24UHQ

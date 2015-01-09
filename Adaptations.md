# Adaptations

These changes were made for my situation:

* Mac OS X 10.10
* Apple's Terminal 
* Terminal set as xterm-256 colour
* Terminal theme: base16-ocean-dark.256 from [Chris Kempson][2]

### What's changed


1. Disabled the session name `neatstatus_session` part
2. Added a separator to the buffer section `BUF #`
3. Added a separator to the linenumber/total linenumbers section `LN # / #`
4. Changed the formatting of the linenumber/total linenumbers resulting in narrower section
5. Changed the coloration of the linenumber/total linenumbers section
6. Changed the separator symbol from pipe ‘|’ to ‘⎜’ which is Unicode character _(hex)_`239C` a.k.a “LEFT PARENTHESIS EXTENSION”.

Together with the following lines

```vim
colorscheme base16-ocean
set background=dark
highlight clear CursorLine
highlight LineNr ctermbg=0 ctermfg=15
highlight CursorLineNr ctermbg=0 ctermfg=11 guifg=#dfdf87 guibg=#353d46
highlight StatusLine ctermbg=8 ctermfg=15
highlight Visual ctermbg=8 ctermfg=0 guifg=#000000 guibg=#808080

" 
"	NeatStatusLine
" 

let g:NeatStatusLine_separator = '⎜'
let g:NeatStatusLine_color_position = 'guifg=#ffffff guibg=#505B66 ctermfg=15 ctermbg=8'
let g:NeatStatusLine_color_line     = 'guifg=#ffff00 guibg=#505B66 gui=bold ctermfg=11 ctermbg=8 cterm=bold'
let g:NeatStatusLine_color_filetype = 'guifg=#ffffff guibg=#ff0000 gui=bold ctermfg=237 ctermbg=7 cterm=NONE'
```

in my `.vimrc` file resulted in this statusline 

![Nice statusline][1]

[1]: http://i.imgur.com/0cazgJX.png "Nice statusline"
[2]: https://github.com/chriskempson/base16-builder

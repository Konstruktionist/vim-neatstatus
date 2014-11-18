# Adaptations

These changes were made for my situation:

* Mac OS X 10.10
* Apple's Terminal 
* Terminal set as xterm-256 colour
* Terminal theme: base16-ocean-dark.256

### What's changed


1. Disabled the session name `neatstatus_session` part
2. Added a separator to the buffer section `BUF #`
3. Added a separator to the linenumber/total linenumbers section `LN # / #`
4. Changed the coloration of the linenumber/total linenumbers section

Together with the following lines

```
" =======================================================================
"	NeatStatusLine
" =======================================================================
let g:NeatStatusLine_separator = '⎜'
let g:NeatStatusLine_color_line     = 'guifg=#ff00ff guibg=#000000 gui=bold ctermfg=9 ctermbg=7 cterm=bold'
let g:NeatStatusLine_color_filetype = 'guifg=#ffffff guibg=#ff0000 gui=bold ctermfg=237 ctermbg=7 cterm=NONE'
" =======================================================================
"	NeatStatusLine End
" =======================================================================
```

in my `.vimrc` file resulted in this statusline 

![Nice statusline][1]

[1]: http://imgur.com/900iWZy.png "Nice statusline"

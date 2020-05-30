# Vim + LaTeX snippets setup

*[How I'm able to take notes in mathematics lectures using LaTeX and Vim](https://castel.dev/post/lecture-notes-1/)*

## Vim configuration

Copy `tex.snippets` to `~/.vim/UltiSnips/` and asuming you're using [Vim Plug](https://github.com/junegunn/vim-plug), add the following to your `.vimrc`:

```vim
Plug 'sirver/ultisnips'
    let g:UltiSnipsExpandTrigger = '<tab>'
    let g:UltiSnipsJumpForwardTrigger = '<tab>'
    let g:UltiSnipsJumpBackwardTrigger = '<s-tab>'

Plug 'lervag/vimtex'
    let g:tex_flavor='latex'
    let g:vimtex_view_method='zathura'
    let g:vimtex_quickfix_mode=0

Plug 'KeitaNakamura/tex-conceal.vim'
    set conceallevel=1
    let g:tex_conceal='abdmg'

setlocal spell
set spelllang=en_us
inoremap <C-l> <c-g>u<Esc>[s1z=`]a<c-g>u
```

## Shubodh's fork/notes

[Notion notes link](https://www.notion.so/saishubodh/VIM-LaTeX-Shortcuts-c08d4ec66b7c4ffeb4b5c8f15c4d555d#b2967cae4f1b4d5abc6789e49385aa09)

*  The `b` means that this snippet will only be expanded at the beginning of a line and `A` stands for auto expand, which means I do not have to press Tab to expand the snippet.
* The snip­pet for in­line math is ‘smart’: it knows when to in­sert a space after the dol­lar sign. When I start typ­ing a word di­rect­ly be­hind the clos­ing $, it adds a space. How­ev­er, when I type a non-​word char­ac­ter, it does not add a space, which would be pre­ferred for ex­am­ple in the case of $p$-value.
* sub­scripts. It changes changes a1 to a_1 and a_12 to a_{12}.

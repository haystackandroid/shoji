# shoji

A vim theme that underlays code with colorful "paper rectangles".

Crafted with the magnificent [Colortemplate](https://github.com/lifepillar/vim-colortemplate).

## installation

If you don’t have a preferred plugin helper, consider trying **vim-plug**, which can be installed with:

```
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
  https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

shoji can be installed using vim-plug by adding the following to the top of your vimrc...

```
call plug#begin('~/.vim/plugged')
Plug 'nightsense/shoji'
call plug#end()
```

...then restarting vim and running `PlugUpdate` (from the vim command line).

## activation

shoji consists of two themes:

- the exuberant `shoji_niji`, which underlays code with a rainbow of colorful paper rectangles
- the restrained `shoji_shiro`, which is content with a minimal practical set of paper rectangles

To activate a shoji theme, add one of the following to your vimrc:

- `colorscheme shoji_niji`
- `colorscheme shoji_shiro`

If you'd like to toggle between the two shoji themes, you could define a keybinding like:

```
noremap <silent> <C-s> : if g:colors_name == "shoji_niji" <bar>
                       \ colorscheme shoji_shiro          <bar>
                       \ else                             <bar>
                       \ colorscheme shoji_niji           <bar>
                       \ endif                            <return>
```

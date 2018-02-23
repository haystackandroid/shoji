# shoji

A vim theme that underlays code with colorful "paper rectangles" (block highlighting).

Crafted with the magnificent [Colortemplate](https://github.com/lifepillar/vim-colortemplate).

## variants

The shoji "theme" is actually a pair of themes.

**shoji_niji** is the exuberant one, papering the syntactic landscape in blocky rainbows.

![screenshot of the shoji_niji vim theme](https://github.com/nightsense/shoji/raw/master/screenshots/shoji_niji.png)

**shoji_shiro** is the restrained one, content with pristine black-and-white, reaching for color only when unavoidably practical.

![screenshot of the shoji_shiro vim theme](https://github.com/nightsense/shoji/raw/master/screenshots/shoji_shiro.png)

## installation

If you don’t have a preferred plugin helper, consider trying **vim-plug**, which can be installed with:

```
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
  https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

With vim-plug, shoji can be installed by adding the following to the top of your vimrc...

```
call plug#begin('~/.vim/plugged')
Plug 'nightsense/shoji'
call plug#end()
```

...then restarting vim and running `PlugUpdate` (from the vim command line).

## activation

shoji consists of two themes:


To activate a shoji theme, add one of the following to your vimrc:

- `colorscheme shoji_niji`
- `colorscheme shoji_shiro`

To toggle between the two shoji themes, add a keybinding like:

```
noremap <silent> <C-s> : if g:colors_name == "shoji_niji" <bar>
                       \ colorscheme shoji_shiro          <bar>
                       \ else                             <bar>
                       \ colorscheme shoji_niji           <bar>
                       \ endif                            <return>
```

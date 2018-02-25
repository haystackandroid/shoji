# shoji&ensp;<img alt="logo for the shoji vim theme" src="https://github.com/nightsense/shoji/raw/master/images/logo.png" height="51" />

A vim theme that conveys syntax with colorful background highlighting (instead of colored text).

Crafted with the magnificent [Colortemplate](https://github.com/lifepillar/vim-colortemplate).

## variants

The shoji "theme" is actually a pair of themes.

**shoji_niji** is the exuberant one, showering syntactic rainbows.

<img alt="screenshot of the shoji_niji vim theme" src="https://github.com/nightsense/shoji/raw/master/images/shoji_niji.png" height="294" />

**shoji_shiro** is the restrained one, content with pristine black-and-white, except where color is unavoidably practical.

<img alt="screenshot of the shoji_shiro vim theme" src="https://github.com/nightsense/shoji/raw/master/images/shoji_shiro.png" height="294" />

## installation

If you don’t have a preferred plugin helper, consider trying [vim-plug](https://github.com/junegunn/vim-plug), which can be installed with:

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

To activate a shoji theme, add one of the following to your vimrc:

- `colorscheme shoji_niji`
- `colorscheme shoji_shiro`

To easily toggle between the two shoji themes, add a keybinding to your vimrc, such as...

```
noremap <silent> <C-s> : if g:colors_name == "shoji_niji" <bar>
                       \ colorscheme shoji_shiro          <bar>
                       \ else                             <bar>
                       \ colorscheme shoji_niji           <bar>
                       \ endif                            <return>
```

...changing `<C-s>` (which denotes the keystroke [ctrl+s]) to suit your preference.

## language samples

### clojure

<img alt="screenshot of clojure code highlighted with the shoji_niji vim theme" src="https://github.com/nightsense/shoji/raw/master/images/sample-clojure.png" height="75" />

### erlang

<img alt="screenshot of erlang code highlighted with the shoji_niji vim theme" src="https://github.com/nightsense/shoji/raw/master/images/sample-erlang.png" height="75" />

### lisp

<img alt="screenshot of lisp code highlighted with the shoji_niji vim theme" src="https://github.com/nightsense/shoji/raw/master/images/sample-lisp.png" height="75" />

### php

<img alt="screenshot of php code highlighted with the shoji_niji vim theme" src="https://github.com/nightsense/shoji/raw/master/images/sample-php.png" height="75" />

### r

<img alt="screenshot of r code highlighted with the shoji_niji vim theme" src="https://github.com/nightsense/shoji/raw/master/images/sample-r.png" height="75" />

### rust

<img alt="screenshot of rust code highlighted with the shoji_niji vim theme" src="https://github.com/nightsense/shoji/raw/master/images/sample-rust.png" height="75" />

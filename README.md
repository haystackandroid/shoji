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

A keybinding for the `ShojiToggle()` function can be used to switch between the two shoji themes:

```
noremap <C-s> :call ShojiToggle()<return>
```

Change `<C-s>` (which denotes the keystroke [ctrl+s]) to suit your preference.

## terminal cursor

### shape

To set mode-specific cursor shapes in terminal vim, see the [vim tips wiki](http://vim.wikia.com/wiki/Change_cursor_shape_in_different_modes).

For instance, to set cursor shapes in vte-compatible terminals (like urxvt):

```
let &t_SI = "\<Esc>[6 q"
let &t_SR = "\<Esc>[4 q"
let &t_EI = "\<Esc>[2 q"
```

This sets the cursor to a vertical line for insert mode, underline for replace mode, and block for normal mode.

### color

To set cursor color in (vte-compatible) terminal vim, wrap the `vim` command in a shell function.

For bash/zsh, add the following to `~/.bashrc` or `~/.zshrc`:

```
vim() {
  printf "%b" "\033]11;#fafafa\007\033]12;#2a2a2a\007"
  sh -c "vim $*"
  clear
  printf "%b" "\033]11;#2e3440\007\033]12;#d8dee9\007"
}
```

For fish, add the following to `~/.config/fish/config.fish`:

```
function vim
  printf "%b" "\033]11;#fafafa\007\033]12;#2a2a2a\007"
  sh -c "vim $argv"
  clear
  printf "%b" "\033]11;#2e3440\007\033]12;#d8dee9\007"
end
```

Replace `2e3440` and `d8dee9` with the background and foreground colors of your terminal theme.

For neovim, substitute `vim` with `nvim`.

## language samples

These samples (drawn from [Rosetta Code](https://rosettacode.org/wiki/Sorting_algorithms/Quicksort)) use vim's built-in syntax detection for each filetype.

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

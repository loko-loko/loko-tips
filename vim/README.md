## Install plugins

```
curl -fLo ~/.vim/autoload/plug.vim \
  --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim

touch ~/.vimrc.plug
mkdir ~/vimplug-plugins
mkdir ~/.vim/plugged

chmod -R 755 ~/.vim
```

Edit `~/.vimrc` file:
```vim
" Call the .vimrc.plug file
if filereadable(expand("~/.vimrc.plug"))
    source ~/.vimrc.plug
endif
```

Edit `~/.vimrc.plug` file:
```vim
call plug#begin('~/.vim/plugged')

" Fugitive Vim Github Wrapper
Plug 'tpope/vim-fugitive'
" Tabnine Code completion
Plug 'codota/tabnine-vim'

call plug#end()
```

To install plugins:
```
:PlugInstall
```

## Install Kite

```
bash -c "$(wget -q -O - https://linux.kite.com/dls/linux/current)"
```


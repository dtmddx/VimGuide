set nocompatible	" required, remove compatibility with VI.
filetype off		" required, do not check filetype automatically. 

" setting, include vundle and init runtime path
set rtp+=~/.vim/bundle/Vundle.vim

call vundle#begin()

" Plugin management using vundle, for example:
Plugin 'VundleVim/Vundle.vim'

" The following examples are used to support the installation of Plugins in different format.

" 1. Installation from github.com
" Plugin 'username/repos name'
Plugin 'tpope/vim-fugitive'

" 2. Installation from http://vim-scripts.org/vim/scripts.html'
" Plugin 'name of Plugin'
Plugin 'L9'

call vundle#end()

filetype plugin indent on " required

" some commands used commonly
" :PluginList 	- list all Plugins installd.
" :PluginInstall	- Plugin install
" :PluginUpdate
" :PluginSearch foo	- 
" :PluginClean 		- 

" help vundle :h vundle

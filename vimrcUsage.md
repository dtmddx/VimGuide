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


通过 Vim 插件来完成对 MarkDown 的完美支持

安装完成了 Vundle 后，我们就可以来通过 Vundle 来安装和管理 Vim 的插件了。为了让 Vim 支持 MarkDown 语法高亮显示就需要安装vim-markdown插件了。当然还有针对 MarkDown 一系列的插件需要安装，如：previm、ColorScheme、nerdtree等等，这些插件来配合已达到 Vim 对 MarkDown 的完美支持，这些都是通过 Vundle 就可以来完成了，下面具体的讲解一下。
安装Markdown插件

vim-markdown是一个让Markdown语法高亮且有相关配置的插件。

用 Vundle 来安装很方便，只需要在.vimrc中配置以下参数，然后重新打开 Vim 使用命令PluginInstall开始安装，注意：tabular必须在vim-markdown前面。
Plugin 'godlygeek/tabular'
Plugin 'plasticboy/vim-markdown'
安装完后打开格式为md的文件就可以体验到Markdown语法高亮的效果了。

上述的安装方法后打开md文件是无效的，经过明月实测后发现必须用下面的方法来手动完成vim-markdown插件的安装配置才能生效。

cd ~/.vim/bundle
git clone https://github.com/tamlok/vim-markdown.git

然后将/root/.vim/bundle/vim-markdown文件夹下的plugin目录（存放插件）、syntax目录（存放语法的解析文件）、ftdetect目录（存放插件对哪些后缀的文件生效）至少这三个目录复制到/root/.vim/目录下才会生效的。

网上的文章这里都是个“坑”呀，甚至 Vundle 里安装都是个“坑”根本就不会生效，只有上述的办法才可以。注意！！！

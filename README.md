# ViMConfig
My personal ViM Configuration files

## Getting the distribution
The easiestland probably only-way to get this distribution is by using `git`. Since the [Vundle][1] is a submodule of this repository, it is recommended that you clone recursively

	git clone --recursive https://github.com/jlconlin/ViMConfig.git ~/.vim


## Configure the configuration
Included with these configuration files are

 - `vimrc`
 - `gvimrc`

To use these files—without copying them—create a file `~/.vimrc` with this as the contents

	if filereadable(expand("~/.vim/vimrc"))
	  source ~/.vim/vimrc
	endif
	"
	if has("gui_running") && filereadable(expand("~/.vim/gvimrc"))
	    source ~/.vim/gvimrc
	endif
	
	if filereadable(expand("~/.vim/vimrc.local"))
	  source ~/.vim/vimrc.local
	endif
Then create a link from `$HOME/.vimrc` to `$HOME/.gvimrc`. Doing this will make ViM see these configuration files and you will be happy.
Cloning my distribution, will not automatically get the plugins. However, the Vundle plugin can do that anyway. Simply do this:

## Installing Plugins
Once the repository has been cloned and configured the plugins can be installed simply by executing:

	vim +PluginInstall +qall
as described by the installation procedures for Vundle.

### Building Plugins
There are some (just one as of this writing) plugins that need to be built after they are installed. Here are the instructions for building each of them.
#### vimproc
	cd .vim/bundle/vimproc/
	make
## ViM Plugins used in this distribution

 - [vim-latex][2]
 - [rainbow][3]
 - [Align][4]
 - [nerdtree][5]
 - [python-mode][6]
 - [VisIncr][7]
 - [XML-Folding][8]
 - [ENDF.vim][9]
 - [cpp.vim][10]
 - [quick-scope][11]
 - [vimproc][12]
 - [vimshell][13]
- [SuperTab][14]
- [Tagbar][15]
- [vim-easytags][16]
- [vim-misc][17]

[1]:	https://github.com/gmarik/Vundle.vim
[2]:	https://github.com/neosimsim/vim-latex
[3]:	https://github.com/oblitum/rainbow
[4]:	https://github.com/JLimperg/Align
[5]:	https://github.com/scrooloose/nerdtree
[6]:	https://github.com/klen/python-mode
[7]:	https://github.com/vim-scripts/VisIncr
[8]:	https://github.com/vim-scripts/XML-Folding
[9]:	https://github.com/jlconlin/ENDF.vim
[10]:	https://github.com/jlconlin/cpp.vim
[11]:	https://github.com/unblevable/quick-scope
[12]:	https://github.com/Shougo/vimproc.vim
[13]:	https://github.com/Shougo/vimshell.vim
[14]:	https://github.com/ervandew/supertab.git
[15]:	http://github.com/majutsushi/tagbar
[16]:	https://github.com/xolox/vim-easytags
[17]:	https://github.com/xolox/vim-misc
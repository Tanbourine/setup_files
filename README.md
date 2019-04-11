# dotfiles
Here are my dotfiles for commonly used programs
Feel free to use or suggest improvements!

I use GNU Stow to maintain a symlink with my git repo
see [this link](http://brandon.invergo.net/news/2012-05-26-using-gnu-stow-to-manage-your-dotfiles.html) for a guide to do this yourself. It provides a much cleaner way to keep your dotfiles up to date. This will allow you to **git pull** to get the latest files. I setup the gitignore to ignore plugins and other files that will automatically download on install


## Installation Instructions

### For Linux:

- Install basic tools
```
sudo apt-get install vim
sudo apt-get install git
sudo apt-get install stow
sudo apt-get install curl
```

- Install a better terminal emulator
```
sudo apt-get install terminator
```

- Install zsh [Wiki](https://github.com/robbyrussell/oh-my-zsh/wiki/Installing-ZSH)
```
sudo apt-get install zsh
```

- Install oh-my-zsh [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

- Clone dotfiles and symlink it
```
git clone https://github.com/Tanbourine/dotfiles.git ~/
cd ~/ rm .zshrc
cd dotfiles && stow vim && stow zsh && stow git
```


- Install fonts for better viewing pleasure [powerline fonts](https://github.com/powerline/fonts)
```
sudo apt-get install fonts-powerline
```


- Open vim and run **:PlugInstall**  to initialize plugins

#### i3 gaps setup
Install i3-gaps from [here](https://github.com/pasiegel/i3-gaps-install-ubuntu)
```
cd ~/dotfiles
stow i3 -t ~/.config/i3
```


### For MacOS:

- Install [homebrew](https://brew.sh/)
```
i/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

brew update
brew upgrade
```

- Install [iTerm2](https://www.iterm2.com/)

- Install oh-my-zsh [Wiki](https://github.com/robbyrussell/oh-my-zsh/wiki)
```
brew install zsh zsh-completions
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
- Install GNU stow
```
brew install stow
```

- Clone dotfiles and symlink it
```
git clone https://github.com/Tanbourine/dotfiles.git ~/
cd ~/ rm .zshrc
cd dotfiles && stow vim && stow zsh
```

- To get the zsh powerline to display fonts correctly, install a powerline font
I use Source Code Pro from https://github.com/powerline/fonts 
Change your iTerm font to Souce Code Pro for Powerline


- Open vim and run **:PlugInstall**  to initialize plugins

- Finish installation of YouCompleteMe
```
brew install --with-toolchain llvm
python ~/.vim/plugged/youcompleteme/install.py
```

- Enjoy! 

### For Windows:
- Burn your computer
- But really it's work in progress


## vim

vim is life!

I split my modularized my .vimrc configurations and just sourced them all in my main .vimrc. It makes things much cleaner and easier to follow.

- settings.vim
- plugins.vim
- plugin_configs.vim

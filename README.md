# Mark's dotfiles

My dotfiles are stored in a [bare Git repository](https://www.atlassian.com/git/tutorials/dotfiles). I used to store and manage my dotfiles using a non-bare repository and symlinks, but recently changed to a Git bare repository because it was simpler and easier to maintain and share. If you want to see the benefits of using a Git bare repository for storing dotfiles, watch this excellent [YouTube video by Derek Taylor](https://youtu.be/tBoLDpTWVOM).

# Notes on specific dotfiles

## .gitconfig

I added a simple alias that turns `pull` into `pull --rebase` in order to preserve history.

## .tmux.conf

I don't like the default command prefix of `Ctrl-b` because it forces me to use two hands or an awkward and inefficient stretch of my left hand to hit both keys. Instead, I changed it to `Ctrl-a`, which is much more efficient. 

## .zshrc

I use [`oh-my-zsh`](https://github.com/robbyrussell/oh-my-zsh) to configure my shell. I have also added an alias to make it easier to use a bare Git repo to store my dotfiles. And I have added some `pyenv` configuration. I use a combination of the [`agnoster` theme](https://github.com/agnoster/agnoster-zsh-theme), [iterm2](https://iterm2.com/), and [solarized dark]()  

## .vimrc

Vim out-of-the-box is just not helpful for editing and reading code. I have added some simple configuration, notably line numbers and turning tabs into spaces. 

# My current MacOS(Mojave)  setup

## Homebrew

I installed Homebrew right away to manage packages for MacOS. I installed the following packages:

* `brew cask install slack`
* `brew cask install sublime-text`
* `brew cask install visual-studio-code`
* `brew cask install google-chrome`
* `brew cask install iterm2`
* `brew install pyenv`
* `brew install tmux`

## PIP

I got pip3 for free when I used [`pyenv` to properly install Python3](https://opensource.com/article/19/5/python-3-default-mac) to my machine. After making Python3 the global default versionfor pyenv environments, I installed the following python packages:

* `pip install aws --upgrade --user`
* `pip install powerline-status`  # see [`poweline](https://powerline.readthedocs.io/en/master/installation.html)

## Pyenv

I hate mucking up my system Python when installing random packages to learn and develop on. So to protect and leave my system Python to the operating system, I installed [`pyenv`](https://github.com/pyenv/pyenv#advanced-configuration) and configured my machine to have Python3 set as the global default pyenv environment.

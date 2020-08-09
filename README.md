# dotfiles

*dotfiles for shell setup*

## 0 - Clone this repo
```bash
cd ~
git clone https://github.com/MarkHershey/dotfiles.git
```

## 1 - Shell: [ZSH (Z Shell)](http://zsh.sourceforge.net/)

##### Install ZSH
For Ubuntu:

```bash
sudo apt update
sudo apt install zsh
```
For other OS, refers to [this](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH).

Verify install
```bash
zsh --version
```



##### Change default shell for current user
```bash
chsh -s $(which zsh)
```

Verify default shell
```bash
echo $SHELL
```

should return `/usr/bin/zsh` or `/bin/zsh` or similar.

## 2 - Plugin Manager for ZSH: [Oh My ZSH](https://github.com/ohmyzsh/ohmyzsh)

##### Install Oh My ZSH
```bash
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

or

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```


## 3 - ZSH Plugin: [Zsh Syntax Highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)

##### Install zsh-syntax-highlighting into Oh My ZSH plugins folder
```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```


## 4 - ZSH Theme: [Powerlevel 10k](https://github.com/romkatv/powerlevel10k)

##### Install Powerlevel 10k
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```

##### Install Font `MesloLGS NF`
- [Manual font installation](https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k)
- Select `MesloLGS NF` as font in terminal's preference setting.

##### Copy `ZSH` dotfile

```bash
cp ~/dotfiles/.zshrc ~/.zshrc && source ~/.zshrc
```

##### Option 1: Launch `p10k` configuration wizard
```bash
p10k configure
```

##### Option 2: Copy `p10k` dotfile
```bash
cp ~/dotfiles/.p10k.zsh ~/.p10k.zsh && source ~/.p10k.zsh
```

## 5 - Text Editor: Vim

##### Install Vim
```bash
sudo apt remove --assume-yes vim-tiny
sudo apt update
sudo apt install --assume-yes vim
vim --version
```

##### vimrc

- pls refers to [MarkHershey / vimrc](https://github.com/MarkHershey/vimrc)

## 6 - Others

```bash
sudo apt-get install libncurses5-dev libncursesw5-dev
sudo apt install git
sudo apt install make
sudo apt install build-essential
sudo apt install tree
```

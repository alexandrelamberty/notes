# Managing your .dotfiles with Git and Stow

Create bare repository

```bash
git init --bare $HOME/.dotfiles
```

Create alias

```bash
alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'
```

Set git status to hide untracked files

```bash
dotfiles config --local status.showUntrackedFiles no
```

Add the alias to .bashrc (or .zshrc)

```bash
echo "alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'" >> $HOME/.bashrc
```

Usage

```bash
dotfiles status
dotfiles add .vimrc
dotfiles commit -m "Add vimrc"
dotfiles add .bashrc
dotfiles commit -m "Add bashrc"
dotfiles push
```

Clone your github repository

```bash
git clone --bare https://github.com/USERNAME/dotfiles.git $HOME/.dotfiles
```

Create an alias

```bash
alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'
```

Checkout the git repository to your $HOME

```bash
dotfiles checkout
```

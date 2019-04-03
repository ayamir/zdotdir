# dotfiles.shell

My ~/.shell directory, which contains my zsh/bash configuration.

## Installation

### Backups

**Warning**: before running these commands, you may want to backup your existing dotfiles:

```bash
find ~ -type f -maxdepth 1 \( -name '.bash*' -o -name '.zsh*' \) -exec cp {} {}.bak \;
```

### ZSH

```zsh
git clone git@github.com:mattmc3/dotfiles.shell.git ~/.config/shell
echo "export ZDOTDIR=~/.config/shell" > ~/.zshenv
echo '[[ -f "$ZDOTDIR"/.zshenv ]] && source "$ZDOTDIR"/.zshenv' >> ~/.zshenv
```

### Bash

```bash
git clone git@github.com:mattmc3/dotfiles.shell.git ~/.config/shell
echo "export BASHDOTDIR=~/.config/shell" > ~/.bash_profile
echo '[[ -f "$BASHDOTDIR"/.bash_profile ]] && source "$BASHDOTDIR"/.bash_profile' >> ~/.bash_profile
echo "export BASHDOTDIR=~/.config/shell" > ~/.bashrc
echo '[[ -f "$BASHDOTDIR"/.bashrc ]] && source "$BASHDOTDIR"/.bashrc' >> ~/.bashrc
```
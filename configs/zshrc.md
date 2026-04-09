# .zshrc

## UNIX

```shell
vim ~/.zshrc
```

## Config

```ini
# history
if [ -z "$HISTFILE" ]; then
  HISTFILE="$HOME/.zsh_history"
fi
SAVEHIST=20001
HISTSIZE=30000
setopt EXTENDED_HISTORY
setopt HIST_BEEP
setopt HIST_EXPIRE_DUPS_FIRST
setopt HIST_FIND_NO_DUPS
setopt HIST_IGNORE_DUPS
setopt HIST_IGNORE_SPACE
setopt HIST_REDUCE_BLANKS
setopt INC_APPEND_HISTORY

if type brew &>/dev/null; then
    FPATH=$(brew --prefix)/share/zsh-completions:$FPATH

    autoload -Uz compinit
    compinit
fi

# alias
alias vim='nvim'
alias v='nvim'
alias hosts='sudo vim /etc/hosts'
alias sudo='sudo '
alias cle='clear'
alias fe='yazi'
alias ll='eza -laF --smart-group --icons=always'
alias g='git '
alias gst='git status'
alias gll='git pull && clear'
alias bat='bat --theme=TwoDark '
#alias ssh='kitty +kitten ssh '
alias vkh='nvim .ssh/known_hosts'

# functions
gsh() {
    git add . &&
    git commit -m "Work with repository" &&
    git push &&
    clear
}

ssv() {
    cd "$HOME/solidsoft/ss-vault/" || return
    git add .
    { git commit -m "Work with repository" || true; } &&
    git push
    cd "$HOME" &&
    clear
}

prv() {
    cd "$HOME/pr-vault/" || return
    git add .
    { git commit -m "Work with repository" || true; } &&
    git push
    cd "$HOME" &&
    clear
}

ua() {
    brew update &&
    brew upgrade &&
    brew cleanup
}

# fzf (Ctrl+R fuzzy search)
source <(fzf --zsh)

# external tools
eval "$(starship init zsh)"
eval "$(zoxide init zsh)"
```


```sh
sudo chmod go-w /opt/homebrew/share
```

```sh
vi ~/.zshrc
```

```sh
# ~/.zshrc

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

# completion
autoload -Uz compinit
compinit

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
alias gll='git pull'
alias gp='git push'
alias gco='git commit -am '
alias gf='git diff'
alias bat='bat --theme=TwoDark '
#alias ssh='kitty +kitten ssh '
alias vkh='nvim .ssh/known_hosts'

# functions
gsh() {
    git add . &&
    git commit -m "." &&
    git push &&
    clear
}

ssv() {
    cd "$HOME/Solidsoft/Projects/solidwall-vault/" || return
    git add .
    { git commit -m "Update vault" || true; } &&
    git push
    cd - &&
    clear
}

myv() {
    cd "$HOME/Projects/my-vault/" || return
    git add .
    { git commit -m "Update vault" || true; } &&
    git push
    cd - &&
    clear
}

ua() {
    brew update &&
    brew upgrade -y &&
    brew cleanup
}

# prompt
source <(fzf --zsh)
eval "$(starship init zsh)"
eval "$(zoxide init zsh)"

# proxy
export http_proxy=http://10.24.0.254:10888
export https_proxy=$http_proxy
export HTTP_PROXY="$http_proxy"
export HTTPS_PROXY="$https_proxy"
export no_proxy="10.24.0.0/24,.yandex.net,.solidwall.io,.github.com"
export NO_PROXY="$no_proxy"
```

# .zprofile

## UNIX

```sh
vim ~/.zprofile
```

## Config

```sh
# initialize homebrew environment (for Apple Silicon)
eval "$(/opt/homebrew/bin/brew shellenv)"
# set up ssh agent for Bitwarden
export SSH_AUTH_SOCK=/Users/ivan/.bitwarden-ssh-agent.sock
# fzf
export FZF_DEFAULT_OPTS='--no-height --no-reverse'
# proxy
export http_proxy="http://127.0.0.1:10909"
export https_proxy="http://127.0.0.1:10909"
```

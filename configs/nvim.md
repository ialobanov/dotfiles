# Neovim

## Windows

```powershell
if (!(Test-Path "$env:USERPROFILE\AppData\Local\nvim")) { New-Item -Path "$env:USERPROFILE\AppData\Local\nvim" -ItemType Directory -Force }
```

## UNIX

```shell
mkdir -p $HOME/.config/nvim && git clone https://github.com/ialobanov/nvim-plain.git $HOME/.config/nvim
```

## Config

```shell
git clone https://github.com/ialobanov/nvim-plain.git $env:USERPROFILE\AppData\Local\nvim
```


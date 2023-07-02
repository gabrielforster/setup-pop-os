# Setup PopOS for dev

## Install updates from system
```bash
sudo apt upgrade -y && sudo apt update
```

## Install stuff for linux usage
 - i3 Window Manager
 - curl Its curl...
 - git Its git...
 - Vim Best text editor
 - Nvim Vim as IDE
 - Tmux Terminal multiplexer
```bash
sudo apt install i3 curl git vim neovim tmux -y
```

## Create a ssh key
```bash
ssh-keygen -t ed25519 -C rochafrgabriel@gmail.com
```

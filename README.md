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

## Install Docker and Docker Compose

### Intall Docker
```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common -y

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"

apt-cache policy docker-ce

sudo apt install docker-ce -y

sudo systemctl status docker # Check if its installed correctly
```
#### Run Docker without sudo
Adding ur user in docker group
```bash
sudo usermod -aG docker ${USER}

su - ${USER}
```
### Install Docker Compose
```bash
sudo apt-get install docker-compose-plugin
```

# Setup PopOS for dev

## Install updates from system
```bash
sudo apt upgrade -y && sudo apt update
```

## Install stuff for linux usage
 - i3 Window Manager
	 - i3blocks
 - curl Its curl...
 - git Its git...
 - Vim Best text editor
 - Nvim Vim as IDE
 - Tmux Terminal multiplexer
 - Snap for package installation
 - lxappearance for theme styling inside i3
 - feh for background/image handling
 - compton window transitions and transparency
 - rofi better mod+d on i3
```bash
sudo apt install i3 i3blocks curl git vim neovim tmux snapd lxappearance feh compton rofi -y
```
Logout and switch to i3

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

## Miscellaneous
#### Spotify
```bash
sudo snap install spotify -y
```

#### Arandr - for monitor handling
```bash
sudo apt install arandr -y
```

#### Android Studio
```bash
sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386 -y

sudo snap install android-studio --classic
```

#### Font-awesome
```bash
sudo apt install fonts-font-awesome
```

#### OH-MY-ZSH
```bash
sudo apt install zsh -y

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
#### OpenVPN
```
sudo apt install openvpn easy-rsa
```

#### AWS-CLI
```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

#### Protobuf compiler
```bash
sudo apt install protobuf-compiler
```

#### Accept remove ssh connection
```bash
sudo apt install openssh-server
```

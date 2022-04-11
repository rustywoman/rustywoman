# Common

```sh
sudo apt-get update
````

```sh
sudo apt-get install \
     apt-transport-https \
     ca-certificates \
     curl \
     gnupg \
     lsb-release \
     make
```

# Docker

```sh
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

```sh
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
sudo apt update
sudo apt install docker-ce
docker --version
```

# Docker-Compose

> https://docs.docker.com/compose/install/

```sh
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose -v
```

# Fish ( er )

```sh
sudo apt-add-repository ppa:fish-shell/release-2
sudo apt-get update
sudo apt-get install -y fish
curl https://git.io/fisher --create-dirs -sLo ~/.config/fish/functions/fisher.fish
```

```sh
chsh
```

```
Password:
Changing the login shell for sugi
Enter the new value, or press ENTER for the default
        Login Shell [/bin/bash]: /usr/bin/fish
```

```sh
fish install oh-my-fish/theme-bobthefish
```

```sh
string trim '
set -g theme_newline_cursor yes
set -g theme_display_git_master_branch yes
set -g theme_color_scheme dracula
set -g theme_powerline_fonts yes
set -g theme_display_date no
set -g theme_display_cmd_duration no
set -gx LC_ALL en_US.UTF-8
' >> ~/.config/fish/config.fish
```

> https://www.nerdfonts.com/font-downloads

```sh
sudo apt install golang-go
go get -u github.com/justjanne/powerline-go
```

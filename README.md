# Development Enviroment Setup on Ubuntu Linux

This README helps me with my Ubuntu configuration!

<br>

## Links

### Videos:
- [Laravel Development Enviroment Setup on Linux](https://youtu.be/m7ULdRiMd-w)

### Softwares & Repositories:
- [Visual Studio Code](https://code.visualstudio.com/)
- [MySQL Workbench](https://dev.mysql.com/downloads/workbench/)
- [Beekeeper Editor Community Edition](https://github.com/beekeeper-studio/beekeeper-studio)
- [Github Desktop on Linux](https://github.com/shiftkey/desktop)
- [Docker Engine](https://docs.docker.com/engine/install/ubuntu/)
- [Docker Desktop](https://docs.docker.com/desktop/install/linux-install/)
- [Docker WSL](https://github.com/codeedu/wsl2-docker-quickstart)
- [Laravel Valet on Linux](https://cpriego.github.io/valet-linux/)
- [Laravel Takeout](https://github.com/tighten/takeout)
- [ohmyzsh](https://github.com/ohmyzsh/ohmyzsh)
- [Zinit](https://github.com/zdharma-continuum/zinit)
- [Flatpak](https://flatpak.org/setup/)

<br>

## Removing Snap-store and Installing Gnome-software

**Removing Snap-store**

```sh
snap remove snap-store
```

<br>

**Installing Gnome-software**

```sh
sudo apt install gnome-software gnome-software-plugin-flatpak
sudo apt remove gnome-software-plugin-snap
```

<br>

## Installation Commands

**Installing Net-Tools**

```sh
sudo apt-get update
sudo apt-get install net-tools
```

<br>

**Installing Git**

```sh
sudo apt update
sudo apt-get install git
```

<br>

**Installing Curl**

```sh
sudo apt update
sudo apt-get install curl
```

<br>

**Installing Apache**

```sh
sudo apt update
sudo apt install apache2
```

<br>

**Installing MySQL Server**

```sh
sudo apt update
sudo apt install mysql-server
```

<br>

**Installing PHP**

```sh
sudo apt update
sudo add-apt-repository ppa:ondrej/php
sudo apt install php
```
Some PHP extensions:
```sh
sudo apt install php-mbstring php-cli php-curl php-xml php-zip php-mysql php-pgsql php-sqlite3
```

<br>

**Installing Composer**

```sh
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '55ce33d7678c5a611085589f1f3ddf8b3c52d662cd01d4ba75c0ee0459970c2200a51f492d557530c71c15d8dba01eae') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```
Most likely, you want to put the composer.phar into a directory on your PATH, so you can simply call composer from any directory (Global install), using for example:
```sh
sudo mv composer.phar /usr/local/bin/composer
```
.bashrc or .zshrc:
```
export PATH=$PATH:$HOME/.config/composer/vendor/bin/
```

<br>

**Installing Laravel**

```sh
composer global require laravel/installer
```

<br>

**Installing Node**

First of all, install NVM (Node Version Manager):
```sh
sudo apt update
curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
```
Then execute the command below:
```sh
source ~/.bashrc
```
Or _~/.zshrc_ if you use zshell.

Then, install Node:
```sh
nvm install node
```

<br>

**Installing Java**

```sh
sudo apt update
sudo apt install default-jdk
```

<br>

**Installing Python & PIP**

```sh
sudo apt update
sudo apt install python3
```

```sh
sudo apt install pip
```

<br>

**Installing ZSH**

```sh
sudo apt update
sudo apt install zsh
```

<br>

<hr>

**Commands to not be needed SUDO to run Docker:**
```sh
sudo groupadd docker
sudo usermod -aG docker $USER
```
Then, restart to change it.

## Keyboard US and BR
**Commands to setxkbmap:**
```sh
setxkbmap -model abnt2 -layout "us,br"
setxkbmap -option grp:menu_toggle
```

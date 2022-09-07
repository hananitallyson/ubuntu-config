# Development Enviroment Setup on Ubuntu Linux

This README helps me with my Ubuntu configuration!

<br>

## Development Programs

- [Visual Studio Code](https://code.visualstudio.com/)
- [MySQL Workbench](https://dev.mysql.com/downloads/workbench/)

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

**Installing Gdebi**

```sh
sudo apt update
sudo apt-get install gdebi-core
```

<br>

**Installing GitHub Desktop**

```sh
sudo wget https://github.com/shiftkey/desktop/releases/download/release-3.0.0-linux2/GitHubDesktop-linux-3.0.0-linux2.deb
sudo gdebi GitHubDesktop-linux-3.0.0-linux2.deb
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
To configure your MySQL server, follow the steps:
```sh
sudo mysql
```
```sql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
exit
```
```sh
sudo mysql_secure_installation
```

<br>

**Installing PHP**

```sh
sudo apt update
sudo add-apt-repository -y ppa:ondrej/php
sudo apt install -y php8.1-bz2 php8.1-cgi php8.1-cli php8.1-common php8.1-curl php8.1-dev php8.1-enchant php8.1-fpm php8.1-gd php8.1-gmp php8.1-imap php8.1-intl php8.1-ldap php8.1-mysql php8.1-odbc php8.1-opcache php8.1-pgsql php8.1-phpdbg php8.1-pspell php8.1-readline php8.1-sybase php8.1-tidy php8.1-xmlrpc php8.1-xsl php8.1-sqlite3 php8.1-mbstring php8.1-bcmath php8.1-soap php8.1-zip php8.1-xdebug php8.1-redis php8.1-igbinary php8.1-imagick
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

<br>

**Installing Java**

```sh
sudo apt update
sudo apt install default-jdk
```

<br>

**Installing Python**

```sh
sudo apt-get install python3
```

<br>

**Installing Vim**

```sh
sudo apt update
sudo apt install vim
```

<br>

**Installing Zsh**

```sh
sudo apt update
sudo apt-get install zsh -y
chsh -s /usr/bin/zsh
```
Now that we have set the zsh as our default shell, we have to configure it. So, we will run zsh in the terminal to execute it. This will show the Z shell configuration. You can go for the recommended configuration for the shell by pressing 2.
```sh
zsh
```
You will have to logout of your system and log back in to see the change.

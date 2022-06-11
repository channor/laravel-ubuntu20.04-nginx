# Setup guide for Ubuntu 20.04 with nginx for Laravel - production

## Setup machine
Setup a machine with OS Ubuntu 20.04. I.e virtual machine instance with Google Cloud Platform.

This process is done with VM Instance on GCP.

## Configure machine for laravel

1. `sudo apt update && sudo apt upgrade`.
2. Install Nginx: `sudo apt install nginx`.
3. Install PHP 8.1

### 1. Update and upgrade machine
`sudo apt update && sudo apt upgrade`

### 2. Install dependencies
```bash
# Nginx
sudo apt install nginx

# Install PHP 8.1
sudo apt-get install ca-certificates apt-transport-https software-properties-common
sudo add-apt-repository ppa:ondrej/php # Not sure, but maybe go with ppa:ondrej/nginx
sudo apt update
sudo apt-get install php8.1-cli \
  php8.1-fpm php8.1-pdo_mysql php8.1-gd \
  php8.1-mbstring php8.1-bcmath php8.1-common \
  php8.1-xml php8.1-curl

# Install Mysql server
sudo apt install mysql-server
```

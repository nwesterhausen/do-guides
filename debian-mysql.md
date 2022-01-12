# Installing MySQL on Debian

Steps to install MySQL on Debian ([Sources](#sources))

Follow these instructions on the Droplet console or after connecting to the droplet [via ssh](https://docs.digitalocean.com/products/droplets/how-to/connect-with-ssh/).

## Steps

1. Add the MySQL Repository 
    1. Download the repo installer:

    `wget https://repo.mysql.com//mysql-apt-config_0.8.20-1_all.deb`

    2. Install the repo

    `sudo apt install ./mysql-apt-config_0.8.20-1_all.deb -y`

    1. Answer any questions during setup, your operating system is Debian 11 Bullseye

2. Install MySQL

    `sudo apt-get update && sudo apt-get install mysql-server`

## Sources

- [MySQL 8 Reference - How to Get MySQL](https://dev.mysql.com/doc/refman/8.0/en/getting-mysql.html)
- [MySQL 8 Reference - A Quick Guide to Using the MySQL Apt Repository](https://dev.mysql.com/doc/mysql-apt-repo-quick-guide/en/)
- [Install MySQL 8 on Debian 11 - kifarunix](https://kifarunix.com/install-mysql-8-on-debian-11/)

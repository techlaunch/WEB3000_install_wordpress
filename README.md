# WEB3000_install_wordpress
Cheat sheet to install WordPress in simple steps

Only do steps 1 to 4 if you do not have Apache+PHP+MySQL on your server.
Open a terminal and type the following commands:

## 0) OPEN YOUR SERVER
ssh root@USER.techlaunch.io

## 1) INSTALL APACHE2
sudo apt update
sudo apt install apache2

## 2) INSTALL MYSQL
sudo apt install mysql-server

## 3) PICK A MYSQL PASSWORD
sudo mysql_secure_installation

## 4) INSTALL PHP
sudo apt install php libapache2-mod-php php-mysql
sudo apt install php-cli
sudo apt install php-curl

## 5) DOWNLOAD WORDPRESS
cd /var/www/html
wget https://wordpress.org/latest.zip
sudo apt-get install unzip
unzip latest.zip
mv wordpress WPNAME
chmod 777 -R WPNAME

## 6) CREATE THE MYSQL TABLE
mysql -uroot -pPASSWORD
create database WPNAME;
quit

## 7) DEPLOY WORDPRESS
http://USERNAME.techlaunch.io/WPNAME
add your database name, user and pass
create a wordpress admin account

# prereq.

made sure system was fully updated using
```
sudo apt update
sudo apt upgrade
```
for omeka, mysql needs to be at least 5.5.5 and php needs to be at least 7.1. 
```
mysql --version
php --version
```
mysql is 8.0.45 and php is 8.3.6
## installing the extras
first, i installed mysqli. i had to use the get command. 
```
sudo apt-get update
sudo apt-get install php-mysql
sudo service apache2 restart
```
now it's time to install imagemagick
```
sudo apt instsall imagemagick
sudo a2enmod rewrite
sudo systemctl restart apache2
```
finally, i installed exif
```
sudo apt install exif
```
now im ready to install omeka!

## installing omeka
### creating a new database in mysql
open mysql. creae a new database titled "omeka". 
```
create user ‘omeka’@'localhost' identified by 'XXXXXXXXX';
create database ‘omeka’;
grant all privileges on ‘omeka’.* to 'omeka'@'localhost';
show databases;
\q
```


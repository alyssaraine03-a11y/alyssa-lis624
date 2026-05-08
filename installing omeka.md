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

## stuck!
i've tried to download and extract the latest omeka version, but no command I do seems to work. I have tried the following commands
```
sudo wget https://omeka.org/classic
sudo wget https://omeka.org/classic.zip
sudo wget https://omeka.org/classic/latest.zip
sudo wget https://omeka.org/omeka-3.2.0.zip
sudo wget https://omeka.org/latest.zip
```
and different combinations of the above phrases. nothing has worked to be able to unzip a file. what am I doing wrong?
## thank you dr. burns, now we continue !
to download the .zip
```
sudo wget https://github.com/omeka/Omeka/releases/download/v3.2/omeka-3.2.zip
```
then to unzip use this command 
```
sudo unzip omeka-3.2.zip
```
use 
```
sudo chown -R $USER:www-data /var/www/html/omeka/
sudo find /var/www/html/omeka/ -type d -exec chmod 755 {} \;
sudo find /var/www/html/omeka/ -type f -exec chmod 644 {} \;
sudo chmod -R 775 /var/www/html/omeka/files
```
# does it work:
http://136.112.36.186/omeka/


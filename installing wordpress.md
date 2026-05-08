wordpress.com is a host, so customers can sign up for free. wordpress.org is software. this is what we use. 

wordpress is the front door. it connects to other websites and services the library is associated with like their OPAC. 
## installation
must have at least php 8.3 and mysql 8.0
```
php --version
```
retrieved version 8.3.6
```
mysql --version
```
retrieved version 8.0.45

checking ubuntu version
```
cat /etc/issue.net
```
ubuntu 24.04.4 LTS

installed the following for php
```
sudo apt install php-curl php-xml php-imagick php-mbstring php-zip php-intl
```
restarted apache2 and mysql using
```
sudo systemctl restart apache2
sudo systemctl restart mysql
```
## download/extract
first, change directory
```
cd /var/www/html
```
then, download latest version of wordpress using wget command
```
sudo wget https://wordpress.org/latest.zip
```
then extract the package using unzip
```
sudo unzip latest.zip
```
## ran into a problem!!
somehow, the unzip package was not installed in the /var/www/html directory. I had to download it using 
```
sudo apt-get install unzip
```
then i was able to unzip the latest.zip

make sure to change directory to wordpress by 
```
cd wordpress
```
if you're already in /var/www/html

## create database/user
first, login to mysql
```
sudo mysql -u root
```
create a new user and password. 

## config
same thing we did with opacuser/opacdb but with wordpress
```
cd /var/www/html/wordpress
sudo cp wp-config-sample.php wp-config.php
sudo nano wp-config.php
```

## site
http://136.112.36.186/wordpress
- site name: Alyssa's Library

# troubleshooting

had to move, so my ip address changed. i can access my wp site, but NOT the admin page. i stopped my vm and restarted, which updated to my new ip address. however, the wp admin site is showing a 404 error. The requested URL was not found on this server.

# How I fixed this
I created a new VM titled finalprojectalyssasmith, then followed the instructions above. Now it's working. Yayy!!

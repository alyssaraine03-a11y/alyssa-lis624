# PREP

installed a NEW vm titled 'koha project' with the IP address: 34.170.236.89

```
sudo apt update
sudo apt upgrade
```
clean up
```
sudo apt autoremove -y && sudo apt clean
```
# install

add the repositories! 
```
sudo apt install apt-transport-https ca-certificates curl
sudo mkdir -p --mode=0755 /etc/apt/keyrings
sudo curl -fsSL https://debian.koha-community.org/koha/gpg.asc -o /etc/apt/keyrings/koha.asc
```
i became the root user using 
```
sudo su
```
then i pasted the following into the cl
```
tee /etc/apt/sources.list.d/koha.sources <<EOF
Types: deb
URIs: https://debian.koha-community.org/koha/
Suites: 25.05
Components: main
Signed-By: /etc/apt/keyrings/koha.asc
EOF
```
i updated, then installed mariadb-server. update again! then installed koha-common

make a copy of this 
```
sudo cp /etc/koha/koha-sites.conf /etc/koha/koha-sites.conf.backup
```
then i opened /etc/koha/koha-sites.conf using the nano command, then changed the intra port to 8080 and the opac port to 8081
```
sudo nano /etc/koha/koha-sites.conf
```
enable apache modules 
```
sudo a2enmod rewrite cgi headers proxy_http
sudo systemctl restart apache2
```
copy the config file!!!
```
sudo cp /etc/apache2/ports.conf /etc/apache2/ports.conf.backup
```
create a library called bibliolib 
```
sudo koha-create --create-db bibliolib
```

to open use http://34.170.236.89:8080




# installation
```
sudo apt install php libapache2-mod-php
sudo systemctl restart apache2
```
confirmed installation using php -v, then restarted apache and checked for errors (none). active and running. 

created a sample doc in the root using
```
cd /var/www/html/
sudo nano info.php
```
saved and closed (ctrl+s and ctrl+x)
you can visit the file in browser using...
### http://35.223.130.84/info.php
# configuration
```
cd /etc/apache2/mods-available/
sudo cp dir.conf dir.conf.bak
sudo nano dir.conf
```
then, i manually changed the line to make index.php the first after DirectoryIndex. checked config using
```
apachectl1 configtest
sudo systemctl reload apache2
system ctl status apache2
```
the above commands check config, restart apache, and checked apache status. should be syntax ok and active/running. 
# reflection
### what is client-side programming?
Client-side programming is what happens on the browser on the user’s end. It’s more related to user and what they see. Server-side is what happens on the backend on a remote server. The client’s browser converts from the server programming (like PHP) to the HTML the user sees. PHP must be installed on the server because the “browser does not execute PHP directly”. It doesn't come with a web browser like JavaScript does. PHP has to be configured and installed to be able to work with client-side HTTP software. 
### how to process php
To process PHP, Apache must default to .php instead of .html when sending to a browser. PHP must be installed, configured, and enabled so the browser shows the .php file first. The configuration order matters because it tells the browser what to access first. If you want the .php file to be shown before .html, it must be first in order.
### why php.info shouldn't be public
phpinfo should not remain publicly accessible because it can be expository of important info about your server. It can show configuration status, file paths, history, extensions, and more. These can be helpful for debugging, but can be risky for public access because of the amount of information it shows. 
## link to website
http://35.223.130.84/ 

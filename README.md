# alyssa-lis624
**For spring 2026, lis 624**
what you have set up so far,
what this repo will contain,
or what you learned during this process.

This repo will contain
1. important info for my classwork
2. changes made on my server
3. helpful shortcuts, tips, and nano commands

#### I have learned to keep thorough documentation during this process. Each time I work in the server, exit it, then reopen, my history from my last open is not shown. So, I need to make sure to include the changes I used and commands I sent on this repo to keep track of my progress. If I make a mistake, I can easily reference this doc to see where I went wrong.

## 2/12/2026 
- rebooted system on vm.
- used 'sudo reboot now' command. 

*added 250 documents from web of science called savedrecs.bib*

use less savedrecs.bib to view the whole doc

### tried out these commands to specify lines starting with journal (aka only pulling the journal) ###

grep -i "^journal =" savedrecs.bib | cut -d"=" -f2 |\
    sed 's/ {//' | sed 's/},//' | \
    sort | uniq -c | sort -nr
TO EXIT FILE READING MODE IN LESS 'Q' !!!

made a new nano file for the example called "operating-systems.csv"

## week 6
sudo: package manager    root: the superuser/admin

apt does not require sudo! 'apt search' doesnt modify anything, just searches. 

tldr gives common commands and easy explanations!!! 
*apt search tldr*

if you want to remove a package and extra stuff, 
- use sudo apt --purge remove tldr
- sudo apt autoremove
- sudo apt clean when you install packages to free up disk space
  
to download .deb files (ubuntu) use the dpkg command sudo dpkg -i <file_name.deb>

## installed yaz-client
sudo apt install yaz
to use yaz, its "yaz-client"

open saalck-uky.alma.exlibrisgroup.com:1921/01SAA_UKY
# apache!!
installed apache2 with:
- sudo apt install apache2
  
use the systemctl command to acquire status info about apache2 and make sure it is enabled and running

i installed elinks using 'sudo apt install elinks'

my external ip address is 35.223.130.84 so to open elinks you say elinks 35.223.130.84

### to open your webpage you made, say 'sudo nano index.html'

now you can use any html you know to make a webpage!!
### to open webpage, http://35.223.130.84/

## 3/7/26 installed tmux ##
used 'apt search tmux', 'sudo apt install tmux', and 'tmux' to open new window. 

## PHP
installed php using 
- sudo apt install php libapache2-mod-php
- sudo systemctl restart apache2

confirmed installed version using php -v

then restarted apache and checked for errors (none)
it showed enabled and active/running

created a sample doc in the root using 
- cd /var/www/html/
- sudo nano info.php (which opened up a nano doc called info.php
- added the following command to the doc
<?php
phpinfo();
?>

saved and closed using ctrl+S and ctrl+X

i visited the file from my browser with: http://35.223.130.84/info.php 

when it was confirmed to be the same as the lecture notes showed, i removed it using instrtuctions provided by lecture

### configuring php
1. changed directories using cd /etc/apache2/mods-available/
2. sudo cp dir.conf dir.conf.bak
3. opened the file using sudo nano dir.conf

i then manually changed the line to make index.php the first after DirectoryIndex

checked config using apachectl1 configtest
*i got the syntax ok message*

reloaded and checked status using 
- sudo systemctl reload apache2
- systemctl status apache2 (it says active running and enabled)
## mysql

installed mysql with sudo apt install mysqyl-server
used the command 'systemctl status mysql' to confirm it was active and running and enabled

created user 'opacuser'@'localhost' identified by 'piper777';

left off on the requiring password part, i got stuck and it wouldnt let me type my password. 

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

## 3/7/26 installed tmux ##
used 'apt search tmux', 'sudo apt install tmux', and 'tmux' to open new window. 


## mysql

installed mysql with sudo apt install mysqyl-server
used the command 'systemctl status mysql' to confirm it was active and running and enabled

created user 'opacuser'@'localhost' identified by 'piper777';

left off on the requiring password part, i got stuck and it wouldnt let me type my password. 

okay i had to redo the grant all privileges and it allowed me to continue. 

# server setup documentation for module 4 #

A LAMP stack (Linux, Apache, MySQL, and PHP) is a bundle that helps web applications run smoothly and operate efficiently. Linux is the operating system, Apache is a web server, MySQL is a database for storing data, and PHP is the language used. According to IBM, the user/client requests information from the web server (Apache) and is sent to PHP. PHP sends the request to MySQL to get the data from storage/code. Once the data is received, PHP sends the info back to the web server and client. 
# apache!!
installed apache2 with:
- sudo apt install apache2
  used the systemctl command to acquire status info about apache2 and make sure it is enabled and running
## PHP
installed php using 
- sudo apt install php libapache2-mod-php
- sudo systemctl restart apache2

confirmed installed version using php -v

then restarted apache and checked for errors (none)
it showed enabled and active/running
  ## mysql

installed mysql with sudo apt install mysqyl-server
used the command 'systemctl status mysql' to confirm it was active and running and enabled

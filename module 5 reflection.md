# What's an OPAC?
An OPAC is a database of library’s holdings. It is an online catalog searchable and accessible to the public. It is essential for a library system so users can easily search for materials. 
# Relational Databases
Relational databases store information in tables with keys that explain relationships between each entry. Data can be pulled with different refined searches to get a better understanding of how different points can/do work together. In an OPAC, relational databases can be used to find materials quicker. A search can be done for a topic and an author, and the database will retrieve books by that author about that topic. 
# Setup
Before creating a database, make sure a new user is created for databse purposes so you don't use the root. To do so, login to mysql and create a user. The x represents the pw. Mine is piper777 for opacdb. 

```
mysql> create user 'opacuser'@'localhost' identified by 'XXXXXXXXX';
```
### creating a database
To create a database, use the following command in mysql. Make sure to grant all priveleges to opacuser!!! This is how I messed up at first.  
```
mysql> create database opacdb default character set utf8mb4 collate utf8mb4_0900_ai_ci;
```
### Logging in
To login, you need to put in the password you set. -p means to require password. 
```
mysql -u opacuser -p
```
Type the password (it doesn't show you typing, but it records it). This command logs you into mysql under the user opacuser and making sure it's password protected (-p). Using the "use" command, you can use that database. Make sure you are in the correct database, NOT THE ROOT, this is how I messed up when creating my OPAC. 
```
mysql> use opacdb;
```
Now you're logged in and can start creating tables. 
### Structure
The cataloging module uses both an html doc and a php doc to handle client requests and search for data in the catalog. To insert new records, you will use the mysql command line and "insert into" whatever table you're using. Or, you can go to http://35.223.130.84/cataloging/index.html and insert that way. Mysql works with php to handle requests and new records entered by authorized users. 
The search and request feature works on the OPAC by taking client requests for data (like author/title) and searching the database using the "select from" command to return results that match the search request. 
### Real world
To make the toy opac more real-world like, I would customize it and make it more stylized. I would use more html or css lines to change colors, fonts, and add symbols so users can easily navigate the page. 
## Configuration
Make sure apache config is running: 
```
sudo apachectl configtest
```
Then make sure apache is running: 
```
sudo systemctl restart apache2
sudo systemctl status apache2
```
To verify Apache is taking requests from command line: 
```
curl -I http://IP_ADDRESS/cataloging/index.html
```
# Using documentation
The documentation/repo was very helpful during this lesson. I should have been more detailed about my notes and writing down what I did exactly how I did it. I got stuck at the cataloging module because I was creating the files in the wrong directory. Had I have written down the exact directory I was in, I would have saved a few hours in backtracking and frustration. I did go back to my helpful tips markdown file for common commands I had forgotten how to use (like how to go back if I got stuck in mysql (ctrl+c). I also went back to try and figure out what the commands meant when typing large chunks of them during the table creation process. I didn't find any gaps in the materials, all of the issues I had were solved by either rereading the lecture notes or going to the module 5 help discussion. 

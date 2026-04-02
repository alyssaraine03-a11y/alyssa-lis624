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
Type the password (it doesn't show you typing, but it records it). This command logs you into mysql under the user opacuser and making sure it's password protected (-p). 

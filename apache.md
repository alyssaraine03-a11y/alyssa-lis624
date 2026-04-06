# installation
```
sudo apt install apache2
systemctl apache2
sudo apt install elinks
```
## external IP address
 35.223.130.84

 to open elinks just say elinks  35.223.130.84
 ### opening the webpage
 on the command line
```
sudo nano index.html
```
on the internet: https://35.223.130.84
# reflection
## whats a web server?
A web server is a software that allows users to access websites. Using HTTP, a web server accepts (or denies with an error message) requests from users to view the webpage’s content. A client will request a connection to the webpage from their browser (like Google or Firefox), and the server will allow or deny access. A web server also stores information and content, and it will find the files you request through your browser. 
## whats a document root?
A document root is the “point of access”, per our lecture notes. It is the folder your server is held on. Our webpage for class uses html, so the root is html, more specifically index.html is the name of the document. I have also used CSS which is another type of root. 
## examples of other web servers
Besides Apache, other servers are Nginx and Cherokee. Someone may choose one web server because of its capabilities, performance, or primary languageFor example, Apache is open-source and free to use, and it is relatively easy to learn. It is good for static and dynamic content. Nginx is faster and cannot use dynamic content, though it is stable and has a consistent CPU usage. 

## Configuring Nginx to use PHP Processor:
By default, Nginx serves web pages from:
```bash
/var/www/html
```
Create a New Website Directory
```bash
sudo mkdir /var/www/projectLEMP
```
•	<mark>mkdir</mark> = Make Directory


•	The command creates a new folder named projectLEMP inside <mark>/var/www</mark>

 

Remember to give yourself ownership using
```bash
 sudo chown -R $USER:$USER /var/www/projectLEMP
```

The command below opens a configuration file named projectLEMP in Nginx's sites-available directory.
```bash
sudo nano /etc/nginx/sites-available/projectLEMP
```
Paste the Nginx file below inside the command above.
```Nginx
#/etc/nginx/sites-available/projectLEMP

server {
    listen 80;
    server_name projectLEMP www.projectLEMP;
    root /var/www/projectLEMP;

    index index.html index.htm index.php;

    location / {
        try_files $uri $uri/ =404;
    }

    location ~ \.php$ {
        include snippets/fastcgi-php.conf;
        fastcgi_pass unix:/var/run/php/php8.3-fpm.sock;
    }

    location ~ /\.ht {
        deny all;
    }
}
```

Enable the new Nginx site and test the Nginx configuration
 

Disable the default Nginx site using the command:
```bash
sudo unlink /etc/nginx/sites-enabled/default
```
Reload Nginx
 
The long <mark>echo</mark> command dynamically fetches information from the AWS EC2 Metadata Service:
•	Public hostname (DNS name) 
•	Public IPv4 address 
and writes them into the page.

 

Fetched information from the long <mark>echo</mark>  command
 

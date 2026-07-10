Create a PHP Test File
```bash
Sudo nano /var/www/projectLEMP/info.php
```
This creates a file named info.php inside the website's root directory.

Add PHP code to the PHP Text File
```PHP
<?php
phpinfo();
```
While performing the task, I ran into an error: **502 Bad Gateway**
I discovered my projectLEMP Nginx configuration was using:
```Nginx
fastcgi_pass unix:/run/php/php8.3-fpm.sock;
```
But my server was running:
```Nginx
php8.5-fpm.sock
```
As a result, Nginx could not connect to PHP-FPM and returned **502 Bad Gateway.**
I fixed it by editing the configuration:
```bash
sudo nano /etc/nginx/sites-available/projectLEMP
```
I changed:
```Nginx
fastcgi_pass unix:/run/php/php8.3-fpm.sock;
```
to:
```Nginx
fastcgi_pass unix:/run/php/php8.5-fpm.sock;
```
Saved the file, then tested the configuration:
```bash
sudo nginx -t
```
The test was successful, and I reloaded Nginx:
```bash
sudo systemctl reload nginx
```
I also verified that Nginx is now using the correct socket:
```bash
grep -R "fastcgi_pass" /etc/nginx/sites-available/
```
The projectLEMP entry showed:
```Nginx
fastcgi_pass unix:/run/php/php8.5-fpm.sock;
```
After that, I refreshed my <mark>info.php</mark> page. The **502 error** was resolved, and I saw the PHP information page.
 

 

 
PHP information page.
 

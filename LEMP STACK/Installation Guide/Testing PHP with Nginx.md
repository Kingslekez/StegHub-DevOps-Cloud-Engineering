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
 
![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/8632155a94e2a30b6458d5b45c181e8d3cab3d6a/LEMP%20STACK/Images/Test%20File%20creation%20and%20Troubleshooting.png)
 
![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/8c2f668e700b24e49911ee963ed823d8e9e09f89/LEMP%20STACK/Images/Troubleshooting%202.png)

![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/8fcebe29b43c7749d1029d3a8c89abba57a09a6c/LEMP%20STACK/Images/Troubleshooting%203.png)
 
PHP information page.
![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/0416ceccec3103aad98ec13313f9798a1d938d70/LEMP%20STACK/Images/PHP%20information%20page.png)

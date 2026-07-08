PHP 8.5 is installed along with libapache2-mod-php, php-mysql, and supporting packages (php-common, php8.5-cli, php8.5-readline, libargon2-1, etc.) 

```bash
sudo nano /var/www/html/info.php
```
Add this content:
```php
<?php phpinfo(); ?>
```
Saved using (Ctrl+O, Enter, Ctrl+X), then I visited:
```bash
http://23.23.9.29/info.php
```
I used the full PHP configuration page, confirming Apache, PHP, and MySQL integration are all working. That completed my LAMP stack.
 

PHP 8.5.4 is installed and working. I confirmed via php -v, with Zend Engine and OPcache loaded.
My LAMP stack is now fully installed: Apache, MySQL, and PHP
I checked to confirm everything's integrated correctly:
```bash
sudo nano /var/www/html/info.php
```
Paste in:
```bash
<?php phpinfo(); ?>
```
Saved using (Ctrl+O, Enter, Ctrl+X), then visited:
```bash
http://23.23.9.29/info.php
```
 

I created a new directory 

```bash 
/var/www/projectlamp 
``` 
while setting up a dedicated project folder instead of using the default /var/www/html. Reason being that I planned to host this as its own virtual host.
Next steps to make this a working site:
1. Set ownership to your user:
```bash
sudo chown -R $USER:$USER /var/www/projectlamp
```
2. Created an index file:
```bash
sudo nano /var/www/projectlamp/index.html
```
3. Set up an Apache virtual host for this directory:
```bash
sudo nano /etc/apache2/sites-available/projectlamp.conf
```
With this content:
```bash
apache
<VirtualHost *:80>
    ServerName projectlamp
    ServerAlias www.projectlamp
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/projectlamp
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```
4. Enabled the site and disable the default:
```bash
sudo a2ensite projectlamp
```
```bash
sudo a2dissite 000-default
```
```bash
sudo systemctl reload apache2
```

 

•	Virtual host config (projectlamp.conf) was created with the right content

•  projectlamp site is enabled, 000-default is disabled  

•	Apache reloaded successfully

•	I created the test file: index.html with "Hello LAMP Project"


I visited my instance's IP in the browser:
```bash
http://23.23.9.29
```
I saw "Hello LAMP Project" displayed instead of the old Apache default page. That confirmed my custom virtual host is live and serving correctly.
 
The command ran successfully — both curl calls completed.
Since I chown'd /var/www/projectlamp to my user earlier, the redirect into index.html worked fine without permission errors.
I refresh my browser at:
```bash
http://23.23.9.2
```
I saw: "Hello LAMP from hostname ec2-23-23-9-29.compute-1.amazonaws.com with public IP 23.23.9.29”, confirming that my page is dynamically pulling instance metadata.

 

 The command history shows I:
1.	Edited dir.conf to prioritize PHP files
2.	Reloaded Apache (success, no errors)
3.	Ran vim /var/www/projectlamp/index.php — but without sudo
 

PHP 8.5.4 is properly loaded as an Apache 2 Handler  
Configured via /etc/php/8.5/apache2/php.ini  
Key extensions loaded: mysqli and pdo_mysql (visible in the "Additional .ini files parsed" list) — meaning PHP can talk to MySQL  
64-bit build, Zend Engine active.    
This confirms my full LAMP stack (Apache + MySQL + PHP) is correctly wired together, with the DB connector extensions in place.  
I deleted this test file since phpinfo() exposes server internals:
```bash
sudo rm /var/www/projectlamp/info.php
```
 

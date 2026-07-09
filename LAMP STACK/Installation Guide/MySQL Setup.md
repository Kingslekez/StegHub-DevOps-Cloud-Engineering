MySQL Server is being installed. 
Once it finishes, run:
```bash
sudo systemctl status mysql
```
to confirm it's active, then secure the installation:

```bash
sudo mysql_secure_installation
```
 ![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/b01588b0100acf6f8357163cf5354babee57aab8/LAMP%20STACK/Images/SQL%20Server%20installed.png)

MySQL is active (running) — status shows "Server is operational," enabled on boot, no errors.
Next, I secured it:
```bash
sudo mysql_secure_installation
```
Once that's done, install PHP:
bash
```bash
sudo apt install php libapache2-mod-php php-mysql -y
```

```bash
sudo systemctl restart apache2
```
![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/b2329ef97dd4753e5418f571b26f00974aa52d8f/LAMP%20STACK/Images/Mysql%20Status.png)

I am running through mysql_secure_installation. A couple of notes on what happened:  
•	I entered "8" for password validation level, which is invalid (only 0/1/2 are accepted), it reprompted, and I correctly entered 2 (STRONG).  
•	Important: it says "Skipping password set for root as authentication with auth_socket is used by default." This means root login is tied to OS-level authentication (auth_socket), not a password  
•	It asked about removing the anonymous user, I said y.
1.	Remove anonymous users → y
2.	Disallow root login remotely → y
3.	Remove test database → y
4.	Reload privilege tables → y

![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/b01588b0100acf6f8357163cf5354babee57aab8/LAMP%20STACK/Images/MySql%20installation%20security.png)

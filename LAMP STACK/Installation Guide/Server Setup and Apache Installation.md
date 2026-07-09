I successfully launched an EC2 instance. AWS is now showing a "Next Steps" panel with common follow-up actions, like:  
•	Connect to your instance – SSH/RDP in to start using it  
•	Create billing alerts / AWS budget – avoid surprise charges  
•	Connect an RDS database – if your app needs a backend DB  
•	Create EBS snapshot policy – automated backups of your storage volume  
•  Manage detailed monitoring / CloudWatch alarms – track performance  
•	Create Load Balancer – distribute traffic if you'll run multiple instances
 

My instance "lamp_stack" is up and running, status shows 2/2 checks passed, meaning both system and instance health checks are good.
It's ready to connect to.
 

I used MobaXterm SSH session settings to connect to my EC2 instance. 
•	Remote host: 23.23.9.29 (my instance's public IP)
•	Username: ubuntu (correct default for Ubuntu AMIs)
•	Port: 22 (standard SSH)
•	Private key: pointing to a key in pem file path 

I am connected to my EC2 instance and running sudo apt update. It's pulling the latest package lists from Ubuntu's repos (main, universe, multiverse, security, etc.). 
Once this finishes, get ready to install your LAMP stack:
```bash
sudo apt install apache2 -y
sudo apt install mysql-server -y
sudo apt install php libapache2-mod-php php-mysql -y
```
 

Apache2 installed successfully along with its dependencies (apache2-bin, apache2-data, apache2-utils, libapr1t64, ssl-cert, etc.) 
```bash
sudo systemctl status apache2
```
Apache2 is active (running), enabled to start on boot, and has been up with no errors in the logs.
Next, I confirm it's reachable from my browser using the public ip.
Once that's confirmed, move on to installing MySQL.

Apache is confirmed working
Next step: install MySQL.
```bash
sudo apt install mysql-server -y
```
After that, secure it with:
```bash
sudo mysql_secure_installation
```
Then move on to PHP:
```bash
sudo apt install php libapache2-mod-php php-mysql -y
```
```bash
sudo systemctl restart apache2
```
 

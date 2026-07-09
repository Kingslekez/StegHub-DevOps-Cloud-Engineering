Installing NGINX
Server set up:
EC2 instance fully initialized and ready for installation of dependencies…..
 ![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/d36d14d5643d314655ed78e5d838098f03aad6c2/LEMP%20STACK/Images/EC2%20instance%20fully%20initialized%20.png)

Updating the server…
![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/d36d14d5643d314655ed78e5d838098f03aad6c2/LEMP%20STACK/Images/Updating%20the%20server.png)
 
Nginx is an open-source web server software that also functions as a reverse proxy, load balancer, HTTP cache, and mail proxy server. Igor Sysoev developed it and first released it in 2004 to address the challenge of efficiently handling large numbers of concurrent web connections. Unlike traditional web servers that create a separate process for each connection, Nginx uses an event-driven architecture, enabling it to deliver high performance with low memory consumption.
Nginx is commonly used to host websites, route traffic to application servers, and distribute requests across multiple backend systems to improve reliability and scalability. It also enhances security by hiding internal servers behind a reverse proxy and supports SSL/TLS encryption for secure communication. Features such as caching, compression, URL rewriting, and virtual hosting help optimize website performance. Because of its speed, stability, flexibility, and scalability, Nginx is widely used by organizations worldwide.

Nginx can be installed on various operating systems, including Linux, Windows, and macOS. On Ubuntu or Debian-based Linux systems, first update the package list using 
```bash
sudo apt update
```
install Nginx with…..

```bash
sudo apt install nginx
```
After installation, start the service using 
```bash
sudo systemctl start nginx
``` 
and enable it to start automatically at boot with sudo systemctl enable nginx. To verify that Nginx is running, open a web browser and navigate to the server’s IP address or localhost. A welcome page should appear, confirming successful installation. On Windows, users can download the Nginx package from the official website, extract the files, and run the executable to start the server. Proper firewall configuration may be required to allow HTTP and HTTPS traffic.
 ![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/d36d14d5643d314655ed78e5d838098f03aad6c2/LEMP%20STACK/Images/Nginx%20installation.png)

Confirming the status of nginx
 ![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/d36d14d5643d314655ed78e5d838098f03aad6c2/LEMP%20STACK/Images/Nginx%20up%20and%20running.png)

Nginx successfully installed

 ![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/d36d14d5643d314655ed78e5d838098f03aad6c2/LEMP%20STACK/Images/Nginx%20successfully%20installed.png)

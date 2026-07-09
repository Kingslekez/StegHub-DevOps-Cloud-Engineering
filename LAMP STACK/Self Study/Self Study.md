# LAMP Stack:

 A Simple Explanation:
LAMP stands for Linux, Apache, MySQL, and PHP. It's a classic set of technologies used together to build and run websites and web applications. Think of it as a "recipe" with four main ingredients, where each one plays a specific role.
The Four Components
1. Linux: The Foundation
Linux is the operating system that everything else runs on. It's like the ground floor of a building — stable, reliable, and free to use. Most web servers around the world run on Linux because it's secure, doesn't crash easily, and doesn't cost money to license (unlike Windows Server).
2. Apache: The Web Server
Apache is the software that actually "serves" your website to visitors. When someone types your website address into their browser, Apache receives that request, finds the right files, and sends back the webpage. Think of Apache as a waiter in a restaurant — it takes the customer's order (the request) and brings back the food (the webpage).
3. MySQL: The Database
MySQL stores all your website's data — things like user accounts, blog posts, product listings, or comments. It's organized like a digital filing cabinet with neat folders and labels, making it easy to store, search, and retrieve information quickly. For example, when you log into a website, MySQL checks if your username and password match what's stored.
4. PHP: The Logic/Brains
PHP is a programming language that makes websites dynamic instead of static. It's the part that does the "thinking"; like checking if a form was filled out correctly, calculating prices in a shopping cart, or pulling specific posts from the database to display. PHP connects Apache (the server) with MySQL (the database) and decides what content to show users.
# How They Work Together
Here's a simple flow of what happens when you visit a LAMP-powered website:
1.	You type a website address into your browser
2.	Linux is running quietly in the background, powering the whole server
3.	Apache receives your request and figures out what you're asking for
4.	PHP runs the necessary code — maybe checking who you are or what page you want
5.	If needed, PHP asks MySQL to fetch some data (like your profile info or a list of products)
6.	MySQL sends that data back to PHP
7.	PHP puts it all together into a webpage
8.	Apache sends that finished webpage back to your browser
This entire process usually takes less than a second.
# Why LAMP Is Popular
•	Free and Open Source: All four components are free to use, which saves money  

•	Flexible: Works for small blogs and huge websites alike  

•	Well-Established: It's been around for decades, so there's tons of documentation and community support  

•	Widely Used: Many popular platforms, like WordPress, run on a LAMP stack
### A Simple Analogy
Imagine building a restaurant:
•	Linux = the building itself  

•	Apache = the waiter taking and delivering orders
•	MySQL = the kitchen's pantry, storing all ingredients
•	PHP = the chef who combines ingredients based on the order
Together, these four pieces create a complete, working system for hosting websites, which is why "LAMP" has remained one of the most popular and trusted setups in web development for over 20 years.

# Software Development Lifecycle (SDLC)
The Software Development Lifecycle (SDLC) is a structured process used to plan, design, develop, test, deploy, and maintain software applications. It helps teams deliver high-quality software that meets user requirements while reducing risks, costs, and development time. The typical SDLC phases include planning, requirements gathering, system design, implementation (coding), testing, deployment, and ongoing maintenance. Each stage has specific objectives and deliverables to ensure the project progresses efficiently. Popular SDLC models include Waterfall, Agile, Spiral, and DevOps-based approaches. By following the SDLC, organizations improve collaboration, maintain quality standards, manage project risks effectively, and deliver reliable software solutions to users.

# Linux, file ownership and permissions
In Linux, file ownership and permissions are fundamental security features that control who can access or modify files and directories. Every file has three permission categories: owner (user), group, and others. Each category can be assigned read (r), write (w), and execute (x) permissions. These permissions determine whether a user can view a file, edit it, or run it as a program.

The chmod (change mode) command is used to modify file and directory permissions. Permissions can be set using symbolic notation, such as chmod u+x script.sh to add execute permission for the owner, or numeric notation, such as chmod 755 script.sh, where 7 represents read, write, and execute, 5 represents read and execute, and the final 5 applies the same permissions to others. Proper use of chmod helps protect sensitive files while allowing appropriate access.

The chown (change owner) command changes the ownership of a file or directory. For example, chown alice:developers report.txt assigns ownership to the user alice and the developers group. This command is commonly used by system administrators to ensure files are owned by the correct users and groups.
Together, chmod and chown enable secure access control, ensuring only authorized users can read, modify, or execute files while maintaining system integrity and protecting sensitive data.

# About TCP and UDP
Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) are the two primary transport layer protocols in the Internet Protocol Suite. Both are responsible for transmitting data between devices, but they serve different purposes based on the application's requirements.
TCP is a connection-oriented protocol that establishes a reliable communication session before transmitting data. It guarantees that packets are delivered in the correct order, without duplication, and retransmits lost packets when necessary. These features make TCP ideal for applications where accuracy is critical, such as web browsing, email, file transfers, and database connections. Although reliable, TCP introduces additional overhead, making it slightly slower than UDP.
UDP is a connectionless protocol that sends data without establishing a connection or guaranteeing delivery. It has lower latency and less overhead, making it suitable for real-time applications such as video streaming, online gaming, Voice over IP (VoIP), and live broadcasts, where speed is more important than perfect reliability.
Several network ports are commonly used in web development. Port 80 is the default port for HTTP traffic, while Port 443 is used for secure HTTPS connections using TLS/SSL encryption. Developers often use Port 3000 for Node.js applications, Port 5173 for Vite development servers, Port 8000 for Python development frameworks, Port 8080 as an alternative HTTP port, and Port 3306 for MySQL database connections. Understanding TCP, UDP, and these commonly used ports helps developers configure servers, troubleshoot connectivity issues, and build secure, high-performing web applications.

# Vi (Vim) Editor 
Becoming familiar with the Vim editor is an essential Linux skill for developers and system administrators. Vim is a powerful, keyboard-driven text editor known for its speed and efficiency. It operates in different modes, including Normal, Insert, Visual, and Command mode. Common commands include i to enter Insert mode, Esc to return to Normal mode, :w to save, :q to quit, and :wq to save and exit. Navigation keys such as h, j, k, and l allow fast movement through text. Learning Vim improves productivity, especially when working on remote Linux servers.

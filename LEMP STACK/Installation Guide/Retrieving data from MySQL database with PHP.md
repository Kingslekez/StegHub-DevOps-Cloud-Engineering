Logging into the MySQL server as the administrative root user using my system's sudo privileges.

 ![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/898e331cffbdbcfc37c2d90d5574c00a509e9ef2/LEMP%20STACK/Images/Creating%20example_database%20in%20MySQL%20and%20listing%20databases.png)

MySQL rejected <mark>mysql_native_password</mark> and weak passwords, but succeeded creating <mark>example_user@'%'</mark> with <mark>P@ssWord@1</mark> and full database privileges.

 ![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/898e331cffbdbcfc37c2d90d5574c00a509e9ef2/LEMP%20STACK/Images/Creating%20example_user%20with%20password%20policy%20troubleshooting%20and%20granting%20privileges.png)

<mark>example_user</mark> successfully logged into MySQL 8.4.10 and ran <mark>SHOW DATABASES</mark>, confirming access to <mark>example_database</mark> alongside default system schemas.

 ![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/898e331cffbdbcfc37c2d90d5574c00a509e9ef2/LEMP%20STACK/Images/Logging%20in%20as%20example_user%20and%20confirming%20database%20access.png)

Table creation initially failed (no database selected); after <mark>USE example_database</mark>, <mark>todo_list</mark> table was created and one row inserted successfully.

 ![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/898e331cffbdbcfc37c2d90d5574c00a509e9ef2/LEMP%20STACK/Images/Creating%20the%20todo_list%20table%20and%20inserting%20the%20first%20row.png)

Row inserted and verified via <mark>SELECT *</mark>; exited MySQL, then opened <mark>todo_list.php</mark> in nano editor.

 ![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/898e331cffbdbcfc37c2d90d5574c00a509e9ef2/LEMP%20STACK/Images/Verifying%20the%20inserted%20row%20with%20SELECT%20%2C%20then%20opening%20todo_list.php%20in%20nano.png)

todo_list.php shown in nano editor: PDO connects to MySQL via localhost using credentials, queries todo_list table, echoes items in HTML list.  
**Remember: I edited my password.**

 ![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/898e331cffbdbcfc37c2d90d5574c00a509e9ef2/LEMP%20STACK/Images/todo_list.php%20source%20code%20shown%20in%20nano%20editor.png)

The <mark>todo_list.php</mark> page now loads successfully, displaying the "TODO" heading and the inserted item "My first important item."

 ![Image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/898e331cffbdbcfc37c2d90d5574c00a509e9ef2/LEMP%20STACK/Images/Browser%20view%20of%20the%20working%20TODO%20list%20webpage.png)


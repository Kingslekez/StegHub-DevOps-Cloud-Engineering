Logging into the MySQL server as the administrative root user using my system's sudo privileges.
 

MySQL rejected <mark>mysql_native_password</mark> and weak passwords, but succeeded creating <mark>example_user@'%'</mark> with <mark>P@ssWord@1</mark> and full database privileges.
 

<mark>example_user</mark> successfully logged into MySQL 8.4.10 and ran <mark>SHOW DATABASES</mark>, confirming access to <mark>example_database</mark> alongside default system schemas.
 

Table creation initially failed (no database selected); after <mark>USE example_database</mark>, <mark>todo_list</mark> table was created and one row inserted successfully.
 

Row inserted and verified via <mark>SELECT *</mark>; exited MySQL, then opened <mark>todo_list.php</mark> in nano editor.
 

todo_list.php shown in nano editor: PDO connects to MySQL via localhost using credentials, queries todo_list table, echoes items in HTML list.
**Remember: I edited my password.**
 

The <mark>todo_list.php</mark> page now loads successfully, displaying the "TODO" heading and the inserted item "My first important item."
 


## TODOLIST

A small web application to help you manage your life.



## TECH

Webserver : Apache (xampp)
backend : PHP 5.5
database : phpMyAdmin ( MySQL )
frontend : jQuery , bootstrap

## SETUP

1) start xampp Control (D:\xampp) and start Apache and MySQL.

2) type http://localhost/phpmyadmin/ and create a new database with the name "todos".

3) create a new table todo with the columns :
	id : int(11) , Extra: AUTO_INCREMENT.
	title : varchar(255)
	description : varchar(255)
	priority : varchar(255)
	due_date : datetime , Default : CURRENT_TIMESTAMP


4) open your httpd-vhosts.conf file (D:\xampp\apache\conf\extra) and copy/paste this virtual host : 

<VirtualHost *:80>
    DocumentRoot "D:/xampp/htdocs/todoListMvc/public"
    ServerName todolist
</VirtualHost>

to map http://todolist/ as virtual host.

5) open the hosts file in C:\Windows\System32\drivers\etc notepad ( as admin ) with notepad and add this line :

127.0.0.1       todolist

6) restart Apache and MySQL in xampp Control.

## ERROR ?

1) Fatal error: Call to undefined function mysql_connect() in C:\xampp\htdocs\todoListMVC\app\database.php on line 12

add "extension=php_mysql.dll" to your php.ini file

=> pdo is taking over mysql so we have to specify in the php.ini that we are using mysql.

## ABOUT : Mohamed Amine Allani _ email : amine.allani94@gmail.com
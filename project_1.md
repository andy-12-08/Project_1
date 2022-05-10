## Some basic prerequisite for this project:
- [Installing VS code, Git, OpenSSH Server, and Creating EC2 instance](https://www.youtube.com/watch?v=R-qcpehB5HY)
- [Brief intro into Markdown markup language for documentation, simple git commands](https://www.youtube.com/watch?v=jsNIlK5s6pI)
- [Crash course for beginners (necessary but optional)](https://www.youtube.com/playlist?list=PLtPuNR8I4TvkwU7Zu0l0G_uwtSUXLckvh)

## Create your linux server in the cloud (ssh into your EC2 instance)
![linux_server](.\images\linux_server.PNG)

## Launch your web server in the cloud
- Update packages in the package manager

    ![linux_server](.\images\update.png)

- Install apache using the package manager

    ![linux_server](.\images\apache.png)

- Confirm apache is installed

    ![linux_server](.\images\apache_installed.png)

- Set EC2 configuration to open TCP port 80 (which enables web browsers access web pages on the internet)



    ![linux_server](.\images\enable_port_80.png)

- Acessing ther server locally from our terminal

    ![linux_server](.\images\web_server.png)

## Installing MYSQL
This is a DBMS that will be required to store and manage data for our site in the future.
![linux_server](.\images\mysql.png)
In addition, run the security script that comes pre-installed with MySQL.

:~$ sudo mysql_secure_installation

set a password for MySQL root 

Confirmation that MySQL is working

![linux_server](.\images\sudo_mysql.png)

[If you encounter any challenge with setting root password for MySQL check this link](https://exerror.com/failed-error-set-password-has-no-significance-for-user-rootlocalhost-as-the-authentication-method-used-doesnt-store-authentication-data-in-the-mysql-server/)

After you set your password, and you want to load MySQl, you will be required to provide your password, you can load mysql using the p (for password) tag as shown below.

![linux_server](.\images\mysql_login_2.png)

Alternatively,

![linux_server](.\images\mysql_login.png)

## Installing PHP
While Apache serves the content of your website, and MySQL stores and manages your data, PHP is that component which will process our code to display dynamic content to our end user. 
![linux_server](.\images\php.png)

At this point, the LAMP stack is completely installed
- Linux
- Apache
- MySQL
- PHP

## Creating a virtual host using Apache
Here we will create and setup a new domain (server block) on Apache server (and name it 'projectlamp'). This new host will be created next to the default ('html' domain) on the           '/var/www/' directory. After creating this doman, enable the required permissions.
![linux_server](.\images\domain.png)

We will then configure Apache server to serve documents from this new host, and we do this by creating a new configuration file ('projectlamp.conf') in Apache's sites-available directory.

![linux_server](.\images\c.png)

![linux_server](.\images\cd.png)















    



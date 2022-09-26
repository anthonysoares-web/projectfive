# prerequisite

* Start 2 AWS instance (one for sql client and the other for sql server)



#  MySQL SERVER steps

* Installing myslq server

![](./screenshots/image1.png)

![](./screenshots/image2.png)



* Enable sql server service

![](./screenshots/image3.png)

* Set sql server password

![](./screenshots/image4.png)


* Run security scipts on sql server
  sudo mysql_secure_installation

 ![](./screenshots/image5.png) 


* Create a new remote user, and database on SQL server using the following commands

    CREATE USER  'remote_user' @'%' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';
    CREATE DATABASE test_db
    GRANT ALL ON test_db.* TO 'remote_user'@'%' WITH GRANT OPTION;
    FLUSH PRIVILEGES


    ![](./screenshots/image6.png)

* Configure sql server to allow connections from remote host
    sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf


    ![](./screenshots/image7.png)


* Restart mysql for client

![](./screenshots/image8.png)



#  MySQL CLIENT steps

* Install SQL Client


![](./screenshots/image9.png)

![](./screenshots/image10.png)

* Get IP address for sql client instance

![](./screenshots/image11.png)

* Connect to SQL Server from SQL CLIENT

![](./screenshots/image12.png)

![](./screenshots/image13.png)




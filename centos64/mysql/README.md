### How to use

     $ MYSQL_HOST=127.0.0.1    # Set the ip address/hostname of your docker host
     $ docker run -d -t -p 3306:3306 mogproject/mysql

##### MySQL

     $ mysql -uroot -h $MYSQL_HOST
     mysql> select host, user from mysql.user;
     mysql> exit


##### Hint

* Default password of ```ssh-user``` is ```ssh-user```
* You are allowed to use ```sudo``` in the container. e.g. ```$ sudo -s```

### How to build

    $ docker build -t mogproject/mysql .


### How to use

     $ SSH_PORT=49900        # Set any unused port
     $ APACHE_PORT=49000
     $ MYSQL_PORT=49001
     $ SSH_HOST=127.0.0.1    # Set the ip address/hostname of your docker host
     $ docker run -d -t -p $SSH_PORT:22 -p $APACHE_PORT:80 -p $MYSQL_PORT:3306 mogproject/apache-mysql-php

##### SSH, Apache + PHP

     $ ssh -p $SSH_PORT -l ssh-user $SSH_HOST
     container$ sudo /bin/bash -c "echo '<?php phpinfo(); ?>' > /var/www/html/info.php"
     container$ exit
     $ curl http://$SSH_HOST:$APACHE_PORT/info.php

##### MySQL

     $ mysql -P $MYSQL_PORT -uroot -h $SSH_HOST
     mysql> select host, user from mysql.user;
     mysql> exit


##### Hint

* Default password of ```ssh-user``` is ```ssh-user```
* You are allowed to use ```sudo``` in the container. e.g. ```$ sudo -s```

### How to build

    $ docker build -t mogproject/apache-mysql-php .


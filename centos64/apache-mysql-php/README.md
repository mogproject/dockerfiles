### How to use

    $ SSH_PORT=50000        # Set any unused port
    $ SSH_HOST=localhost    # Set the ip address/hostname of your docker host
    $ docker run -d -p $SSH_PORT:22 -p 8000:80 -p 3306:3306 mogproject/apache_mysql_php

* SSH, Apache + PHP

    $ ssh -p $SSH_PORT -l ssh-user $SSH_HOST
    [container]$ sudo /bin/bash -c "echo '<?php phpinfo(); ?>' > /var/www/html/info.php"
    [container]$ exit
    $ curl http://docker1:8000/info.php

* MySQL

    $ mysql -uroot -h $SSH_HOST
    mysql> select host, user from mysql.user;
    mysql> exit


##### Hint

* Default password of ```ssh-user``` is ```ssh-user```
* You are allowed to use ```sudo``` in the container. e.g. ```$ sudo su -```

### How to build

    $ docker build -t mogproject/apache_mysql_php .


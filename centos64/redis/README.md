### How to use

     $ REDIS_HOST=127.0.0.1    # Set the ip address/hostname of your docker host
     $ docker run -d -t -p 6379:6379 mogproject/redis

##### Redis

     $ redis-cli -h $REDIS_HOST
     redis> dbsize
     redis> exit

##### Hint

* Default password of ```ssh-user``` is ```ssh-user```
* You are allowed to use ```sudo``` in the container. e.g. ```$ sudo -s```

### How to build

    $ docker build -t mogproject/redis .


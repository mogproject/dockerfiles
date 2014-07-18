### How to use

     $ REDIS_HOST=127.0.0.1    # Set the ip address/hostname of your docker host
     $ docker run -d -t -p 6379:6379 mogproject/redis

##### Redis

     $ redis-cli -h $REDIS_HOST
     redis> dbsize
     redis> exit


### How to build

    $ docker build -t mogproject/redis .


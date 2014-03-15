### How to use

    $ SSH_PORT=49900        # Set any unused port
    $ SSH_HOST=localhost    # Set the ip address/hostname of your docker host
    $ docker run -d -t -p $SSH_PORT:22 mogproject/sshd-supervisor
    $ ssh -p $SSH_PORT -l ssh-user $SSH_HOST

##### Hint

* Default password of ```ssh-user``` is ```ssh-user```
* You are allowed to use ```sudo``` in the container. e.g. ```$ sudo su -```

### How to build

    $ docker build -t mogproject/sshd-supervisor .


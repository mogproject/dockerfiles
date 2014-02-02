### How to use

    $ SSH_PORT=50000        # Set any unused port
    $ SSH_HOST=localhost    # Set the ip address/hostname of your docker host
    $ docker run -d -p $SSH_PORT:22 mogproject/sshd
    $ ssh -p $SSH_PORT -l ssh-user $SSH_HOST

##### Hint

* Default password of ```ssh-user``` is ```ssh-user```
* You are allowed to use ```sudo``` in the container. e.g. ```$ sudo su -```

### How to build

    $ docker build -t mogproject/sshd .


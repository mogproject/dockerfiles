### How to use

```
$ SSH_FORWARD_PORT=50000
$ DOCKER_HOST=    # Set your docker host!
$ docker run -d -p $SSH_FORWARD_PORT:22 mogproject/sshd
$ ssh -p $SSH_FORWARD_PORT -l ssh-user $DOCKER_HOST
```

##### Hint

* Default password of ```ssh-user``` is ```ssh-user```
* You are allowed to use ```sudo``` in the container. e.g. ```$ sudo bash```

### How to build

```
$ docker build -t mogproject/sshd .
```

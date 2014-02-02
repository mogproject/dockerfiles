CentOS 6.4 (64bit) with shogi-server
====

#### Protocol information

http://shogi-server.sourceforge.jp/


##How to play with shogi-server

### 1. Log in to your docker host

### 2. Download this image

This may take several minutes.

    $ docker pull mogproject/shogi-server

### 3. Run the docker container with port forwarding

    $ docker run -d -p 4081:4081 mogproject/shogi-server

### 4. Check the status of the running container

    $ docker ps

### 5. Connect to shogi-server

1) Using CSA client tool

[Download from here][1], then connect to *docker-host* : 4081

  or

2) Using telnet command

    console1$ telnet <docker-host> 4081
    LOGIN user1 pass1

and
 
    console2$ telnet <docker-host> 4081
    LOGIN user2 pass2

After two users' login, the initial state like below will be shown.

>     BEGIN Game_Summary  
>     Protocol_Version:1.1  
>     Protocol_Mode:Server  
>     Format:Shogi 1.0  
>     Declaration:Jishogi 1.1  
>     Game_ID:event1+default-1500-0+user1+user2+20140106110231  
>     Name+:user1  
>     Name-:user2  
>     Your_Turn:-  
>     Rematch_On_Draw:NO  
>     To_Move:+  
>     BEGIN Time  
>     Time_Unit:1sec  
>     Total_Time:1500  
>     Byoyomi:0  
>     Least_Time_Per_Move:1  
>     END Time  
>     BEGIN Position  
>     P1-KY-KE-GI-KI-OU-KI-GI-KE-KY  
>     P2 * -HI *  *  *  *  * -KA *  
>     P3-FU-FU-FU-FU-FU-FU-FU-FU-FU  
>     P4 *  *  *  *  *  *  *  *  *  
>     P5 *  *  *  *  *  *  *  *  *  
>     P6 *  *  *  *  *  *  *  *  *  
>     P7+FU+FU+FU+FU+FU+FU+FU+FU+FU  
>     P8 * +KA *  *  *  *  * +HI *  
>     P9+KY+KE+GI+KI+OU+KI+GI+KE+KY  
>     +  
>     END Position  
>     END Game_Summary

Congratulations!!  
Type **LOGOUT** command to quit (or continue playing; see the [protocol][2]).


  [1]: http://shogi-server.sourceforge.jp/
  [2]: http://www.computer-shogi.org/protocol/tcp_ip_server_113.html

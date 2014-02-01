# Dockerfile for shogi-server
#
#

# use the centos image provided by dotCloud
FROM centos:6.4

# install packages
RUN yum install -y ruby
RUN yum install -y git

# download shogi-server module
RUN git clone git://git.sourceforge.jp/gitroot/shogi-server/shogi-server.git /opt/shogi-server

# create shogi user and change owner of the directory.
RUN useradd shogi
RUN chown -R shogi /opt/shogi-server

# launch shogi-server when launching the container
ENTRYPOINT ["ruby", "/opt/shogi-server/shogi-server", "event1", "4081"]

# run shogi-server as shogi user
USER shogi

# expose shogi-server port
EXPOSE 4081

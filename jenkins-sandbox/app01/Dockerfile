FROM ubuntu:22.04

RUN apt-get update \
		&& apt-get install -y openssh-server sudo openjdk-17-jdk vim
RUN useradd -rm -d /home/ubuntu -s /bin/bash -g root -G sudo -u 1000 test
RUN echo 'test:test' | chpasswd
RUN service ssh start

EXPOSE 22 8080

CMD ["/usr/sbin/sshd","-D"]
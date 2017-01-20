FROM centos:7

RUN yum install -y gcc cmake
WORKDIR /usr/src/myapp
CMD gcc -o myapp main.c && ./myapp

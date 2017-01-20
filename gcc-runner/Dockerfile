FROM centos:7

RUN yum install -y gcc cmake
WORKDIR /usr/src/app
CMD rm -rf build && \
	mkdir build && \
	gcc -o build/executable main.c && \
	./build/executable

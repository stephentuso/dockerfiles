FROM alpine:latest

RUN apk update && apk add build-base
WORKDIR /usr/src/app
CMD rm -rf build && \
	mkdir build && \
	gcc -o build/executable main.c && \
	./build/executable

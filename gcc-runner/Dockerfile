FROM alpine:latest

RUN apk update && apk add build-base
WORKDIR /usr/src/app
CMD rm -rf build && \
    mkdir build && \
    printf "---------\nCompiling\n---------\n\n" && \
    gcc -o build/executable -Wall -std=c99 *.c && \
    printf "---------\nRunning\n---------\n\n" && \
    ./build/executable

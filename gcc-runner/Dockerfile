FROM alpine:latest

RUN apk update && apk add build-base
WORKDIR /usr/src/app
CMD rm -rf build && \
    mkdir build && \
    echo "---------\nCompiling\n--------\n\n" \
    gcc -o build/executable -Wall -std=c99 *.c && \
    echo "--------\nRunning\n---------\n\n" \
    ./build/executable

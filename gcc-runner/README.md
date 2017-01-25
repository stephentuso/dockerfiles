# gcc-runner

For one of my classes, our C programs are supposed to be compiled ~~in CentOS~~ (scratch that, I'm using Alpine to keep it smaller) with `gcc`. I'm using this docker image for that purpose. The `docker-gcc` script and default command assumes `main.c` is the entry point.

`docker-gcc` can be located outside the project dir and run with the src dir being the first argument (`docker-gcc ./`), or located inside the project dir and run without any arguments. 

# Rstudio

Dockerfiles
Use r-base as a base for your own Dockerfiles. For instance, something along the lines of the following will compile and run your project:
```
FROM r-base
COPY . /usr/local/src/myscripts
WORKDIR /usr/local/src/myscripts
CMD ["Rscript", "myscript.R"]
Build your image with the command:
```

```
$ docker build -t myscript /path/to/Dockerfile
```
Running this container with no command will execute the script. Alternatively, a user could run this container in interactive or batch mode as described above, instead of linking volumes.

Further documentation and example use cases can be found at the rocker-org project wiki.


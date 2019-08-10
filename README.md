# docker-hello-world
Simple hello world app with basic docker and python

**Run following command to run on localhost**
(Make sure you have a proper docker setup)

```docker run -p 4000:80 santoshsharma8150/get-started:part2```


**Dockerfile**

A Dockerfile is a text file that Docker reads in from top to bottom. It contains a bunch of instructions which informs Docker HOW the Docker image should get built.

Some command used in Dockerfile:

1. ```FROM```: Creates a layer from the given (In our case it's ```python:2.7-slim```) Docker image.
2. ```WORKDIR```: This defines the base directory from which all our commands are executed.
3. ```RUN```: This is how we run commands; in this example, RUN is used primarily to install various pieces of software.
4. ```COPY```: Copy the current directory contents into the container at given location. (In our case './app' directory)
5. ```EXPOSE```: Informs Docker that the container listens on the specified network port(s) at runtime.EXPOSE does not make the ports of the container accessible to the host.
6. ```ENV```: The ENV instruction sets the environment variable <key> to the value <value> (In our case 'NAME' is key and 'world is value').
7. ```CMD```: The main purpose of a CMD is to provide defaults for an executing container. These defaults can include an executable, or they can omit the executable, in which case you must specify an ENTRYPOINT instruction as well.


**References**

1. Docker official documentation

      https://docs.docker.com/get-started/

1. Good explanation about docker image vs container

      https://stackoverflow.com/questions/23735149/what-is-the-difference-between-a-docker-image-and-a-container
  
2. Dockerfile command cheat sheet

      https://kapeli.com/cheat_sheets/Dockerfile.docset/Contents/Resources/Documents/index

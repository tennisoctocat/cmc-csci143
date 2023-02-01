# FROM debian = docker run -it debian
# debian is the "original" or "base" image
FROM debian

# every RUN command is going to run automatically in the terminal 
# By default, apt-get asks the user if they really want to update/install things on the system. The -y flag says automatically press the yes button so it automatically does it.
RUN apt-get update -y
RUN apt-get install python3 -y

# COPY moves a file from the lambda server to the Docker container
# leftmost parameter is the location on the lambda server
# rightmost parameter is the location on the docker container. 
COPY ./infinite.py /

# this is the command that gets run when we do docker run
CMD python3 /infinite.py

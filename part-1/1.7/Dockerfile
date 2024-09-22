FROM ubuntu:22.04

WORKDIR /

COPY script.sh .
RUN chmod +x script.sh

# install curl
RUN apt-get update
RUN apt-get -y install curl

CMD ./script.sh


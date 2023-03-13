FROM ubuntu:18.04

# install curl
RUN apt update
RUN apt install -y curl

COPY script.sh .

RUN chmod +x script.sh

CMD ./script.sh
 

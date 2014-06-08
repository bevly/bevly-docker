FROM ubuntu:14.04
RUN apt-get update
RUN apt-get install -y golang-go git
RUN useradd -m --password '*' -s /bin/bash jdoe
ADD scripts/docker-build-bevly-server /home/jdoe/
ENTRYPOINT ["/bin/su", "-l", "jdoe"]
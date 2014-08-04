FROM ubuntu:14.04
RUN apt-get update
RUN apt-get install -y git mercurial build-essential
RUN cd /usr/local && hg clone -u release https://code.google.com/p/go
RUN cd /usr/local/go/src && ./make.bash
RUN echo 'PATH="/usr/local/go/bin:$PATH"' >/etc/profile.d/gopath.sh
RUN useradd -m --password '*' -s /bin/bash jdoe
ADD scripts/docker-build-bevly-server /home/jdoe/
ENTRYPOINT ["/bin/su", "-l", "jdoe"]
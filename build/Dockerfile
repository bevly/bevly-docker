FROM ubuntu:14.04
RUN apt-get update
RUN apt-get install -y git build-essential mercurial curl
RUN cd /usr/local && curl -O https://storage.googleapis.com/golang/go1.5.1.linux-amd64.tar.gz && tar xvzf go1.5.1.linux-amd64.tar.gz
RUN echo 'PATH="/usr/local/go/bin:$PATH"' >/etc/profile.d/gopath.sh
RUN useradd -m --password '*' -s /bin/bash jdoe
ADD scripts/docker-build-bevly-server /home/jdoe/
ENTRYPOINT ["/bin/su", "-l", "jdoe"]
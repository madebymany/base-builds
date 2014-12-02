FROM ubuntu:12.04
RUN echo "deb http://us.archive.ubuntu.com/ubuntu/ precise universe" | tee -a /etc/apt/sources.list
RUN apt-get update -qq
RUN apt-get install -qy --no-install-recommends dialog python-software-properties apt-transport-https
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ precise main restricted'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ precise-updates main restricted'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ precise universe'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ precise-updates universe'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ precise multiverse'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ precise-updates multiverse'
RUN add-apt-repository 'ppa:mxmops/packages'
RUN apt-get update -qq
RUN apt-get install -qy --no-install-recommends apt-transport-s3 curl git-core sudo make openssl python-pip build-essential gcc rsync
RUN echo "gem: --no-document --no-rdoc --no-ri\" | tee /etc/gemrc"

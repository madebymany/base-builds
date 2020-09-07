FROM ubuntu:20.04
ENV DEBIAN_FRONTEND noninteractive
RUN echo "deb http://us.archive.ubuntu.com/ubuntu/ focal universe" | tee -a /etc/apt/sources.list
RUN apt-get update -qq
RUN apt-get install -qy --no-install-recommends dialog software-properties-common
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ focal main restricted'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ focal-updates main restricted'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ focal universe'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ focal-updates universe'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ focal multiverse'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ focal-updates multiverse'
RUN apt-get update -qq
RUN apt-get install -qy --no-install-recommends curl git sudo make openssl build-essential gcc rsync apt-transport-https
RUN echo "gem: --no-document --no-rdoc --no-ri" | tee /etc/gemrc
RUN apt-get autoremove -yq
RUN apt-get clean -yq

FROM ubuntu:14.04
ENV DEBIAN_FRONTEND noninteractive
RUN echo "deb http://us.archive.ubuntu.com/ubuntu/ trusty universe" | tee -a /etc/apt/sources.list
RUN apt-get update -qq
RUN apt-get install -qy --no-install-recommends dialog python-software-properties software-properties-common
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ trusty main restricted'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ trusty-updates main restricted'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ trusty universe'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ trusty-updates universe'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ trusty multiverse'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ trusty-updates multiverse'
RUN apt-get update -qq
# RUN apt-get upgrade
RUN apt-get install -qy --no-install-recommends curl git sudo make openssl python-pip build-essential gcc rsync apt-transport-https
RUN echo "gem: --no-document --no-rdoc --no-ri" | tee /etc/gemrc
RUN apt-get autoremove -yq
RUN apt-get clean -yq

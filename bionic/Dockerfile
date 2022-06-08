FROM ubuntu:18.04
ENV DEBIAN_FRONTEND noninteractive
RUN echo "deb http://us.archive.ubuntu.com/ubuntu/ bionic universe" | tee -a /etc/apt/sources.list
RUN apt-get update -qq
RUN apt-get install -qy --no-install-recommends gpg-agent dirmngr dialog software-properties-common
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ bionic main restricted'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ bionic-updates main restricted'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ bionic universe'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ bionic-updates universe'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ bionic multiverse'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ bionic-updates multiverse'
RUN apt-get update -qq
# RUN apt-get upgrade
RUN apt-get install --install-recommends linux-generic-hwe-18.04  
RUN apt-get install -qy --no-install-recommends curl git sudo make openssl python-pip build-essential gcc rsync apt-transport-https
RUN echo "gem: --no-document --no-rdoc --no-ri" | tee /etc/gemrc
RUN apt-get autoremove -yq
RUN apt-get clean -yq

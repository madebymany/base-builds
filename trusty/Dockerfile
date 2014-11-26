FROM ubuntu:14.04
RUN echo "deb http://us.archive.ubuntu.com/ubuntu/ trusty universe" | tee -a /etc/apt/sources.list
RUN apt-get update -qq
RUN apt-get install -qy --no-install-recommends dialog python-software-properties software-properties-common
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ trusty main restricted'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ trusty-updates main restricted'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ trusty universe'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ trusty-updates universe'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ trusty multiverse'
RUN add-apt-repository 'deb http://us.archive.ubuntu.com/ubuntu/ trusty-updates multiverse'
RUN add-apt-repository 'deb http://apt.mxmdev.com trusty-stable main'
RUN apt-key adv --keyserver 'keys.gnupg.net' --recv-keys '7F40EF0A'
RUN apt-get update -qq
RUN apt-get install -qy --no-install-recommends apt-transport-s3 curl git sudo make openssl python-pip build-essential gcc rsync
RUN echo "gem: --no-document --no-rdoc --no-ri" | tee /etc/gemrc

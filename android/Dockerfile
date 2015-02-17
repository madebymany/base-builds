FROM quay.io/madebymany/build-bases:trusty
RUN apt-get update -qq && apt-get install -y openjdk-7-jre-headless expect lib32z1 lib32ncurses5 lib32bz2-1.0
RUN curl -sSL http://dl.google.com/android/android-sdk_r24.0.1-linux.tgz | tar -xz --no-same-owner
RUN chmod -R a+rX /android-sdk-linux
RUN expect -c 'set timeout -1; spawn android-sdk-linux/tools/android update sdk --all --no-ui; expect "Do you accept the license" { exp_send "y\r" ; exp_continue }'
ENV ANDROID_HOME=/android-sdk-linux

FROM ubuntu:18.04

RUN apt-get update \
 && apt-get install --yes \
      software-properties-common \
      wget \
 && apt-get update

RUN wget https://download.java.net/java/ga/jdk11/openjdk-11_linux-x64_bin.tar.gz
RUN sha256sum openjdk-11_linux-x64_bin.tar.gz
RUN tar xzvf openjdk-11_linux-x64_bin.tar.gz
RUN mkdir /usr/lib/jvm
RUN mv jdk-11 /usr/lib/jvm/openjdk-11-manual-installation/
RUN update-alternatives --install /usr/bin/java java /usr/lib/jvm/openjdk-11-manual-installation/bin/java 1
RUN update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/openjdk-11-manual-installation/bin/javac 1

RUN apt-get install --yes \
      maven \
      apt-transport-https

RUN echo "deb https://dl.bintray.com/sbt/debian /" | tee -a /etc/apt/sources.list.d/sbt.list
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 642AC823 \
 && apt-get update \
 && apt-get install --yes \
      sbt \
      nodejs \
      npm

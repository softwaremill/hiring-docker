FROM ubuntu:18.04

RUN apt-get update \
 && apt-get install --yes \
      software-properties-common \
 && add-apt-repository ppa:webupd8team/java \
 && apt-get update

RUN echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections
RUN apt-get install --yes \
      oracle-java8-set-default \
      oracle-java8-installer \
      maven \
      apt-transport-https

RUN echo "deb https://dl.bintray.com/sbt/debian /" | tee -a /etc/apt/sources.list.d/sbt.list
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 642AC823 \
 && apt-get update \
 && apt-get install --yes \
      sbt \
      nodejs \
      npm

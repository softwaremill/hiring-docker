FROM openjdk:11

RUN apt-get update \
 && apt-get install --yes \
      software-properties-common \
      wget \
 && apt-get update

RUN apt-get install --yes \
      maven \
      apt-transport-https

RUN echo "deb https://dl.bintray.com/sbt/debian /" | tee -a /etc/apt/sources.list.d/sbt.list
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 642AC823 \
 && apt-get update \
 && apt-get install --yes \
      sbt

RUN apt-get install -y curl \
 && curl -sL https://deb.nodesource.com/setup_9.x | bash - \
 && apt-get install -y nodejs \
 && curl -L https://www.npmjs.com/install.sh | sh

CMD ["bash"]

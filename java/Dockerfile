FROM phusion/baseimage
MAINTAINER Paul Wang <wagzhi@gmail.com>

RUN apt-get update
RUN apt-get install -y openjdk-7-jdk
RUN apt-get install unzip
ADD play /play
RUN unzip /play/typesafe-activator-1.2.10.zip
ENV PATH /play/activator-1.2.10:$PATH
MKDIR /workspace
WORKDIR /workspace
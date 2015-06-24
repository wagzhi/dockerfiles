FROM java:7
MAINTAINER Paul Wang <wagzhi@gmail.com>

RUN mkdir /play
RUN apt-get install unzip
ADD play /play
RUN \
	cd /play && \
    unzip typesafe-activator-1.2.10.zip
ENV PATH /play/activator-1.2.10:$PATH
RUN mkdir /workspace
WORKDIR /workspace
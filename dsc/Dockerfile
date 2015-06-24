FROM wagzhi/java:8
MAINTAINER Paul Wang <wagzhi@gmail.com>
#target: wagzhi/cassandra:2.1.2

RUN \
  apt-get update && \
  apt-get install -y python python-dev python-pip python-virtualenv && \
  rm -rf /var/lib/apt/lists/*

RUN mkdir mkdir /csd
ADD packages /csd
RUN cd /csd
#RUN tar zxvf dsc.tar.gz
WORKDIR /csd

EXPOSE 7199 7000 7001 9160 9042
EXPOSE 22 8012 61621

CMD /sbin/my_init -- bash -l

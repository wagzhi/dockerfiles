FROM wagzhi/java:8
MAINTAINER Paul Wang <wagzhi@gmail.com>
RUN echo "deb http://debian.datastax.com/community stable main" | sudo tee -a /etc/apt/sources.list.d/cassandra.sources.list
RUN curl -L http://debian.datastax.com/debian/repo_key | sudo apt-key add -
RUN apt-get update
RUN apt-get install -y dsc20=2.0.11-1 cassandra=2.0.11
RUN service cassandra stop
RUN rm -rf /var/lib/cassandra/data/system/*

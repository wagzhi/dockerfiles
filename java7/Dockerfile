FROM phusion/baseimage
MAINTAINER Paul Wang <wagzhi@gmail.com>

# Install Java.
RUN \
  echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
  add-apt-repository -y ppa:webupd8team/java && \
  apt-get update && \
  apt-get install -y oracle-java7-installer && \
  rm -rf /var/lib/apt/lists/*

# Define working directory.
WORKDIR /

# Define default command.
CMD /sbin/my_init -- bash -l
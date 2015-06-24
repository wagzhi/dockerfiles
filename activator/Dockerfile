FROM wagzhi/oracle-java:7
MAINTAINER Paul Wang <wagzhi@gmail.com>
#target: wagzhi/activator:1.2.10

RUN mkdir /workspace && mkdir /play
ADD packages /play
RUN cd /play && tar -xf activator-1.2.10.tar
RUN mv /play/ivy2-cache.tar /root/
RUN mv /play/sbt-cache.tar /root/
RUN cd /root && tar -xf ivy2-cache.tar && tar -xf sbt-cache.tar
RUN rm /root/ivy2-cache.tar && rm /root/sbt-cache.tar && rm /play/activator-1.2.10.tar
ENV PATH /play/activator-1.2.10:$PATH
WORKDIR /workspace

CMD /sbin/my_init -- bash -l
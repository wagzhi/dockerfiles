FROM wagzhi/activator:1.2.10
MAINTAINER Paul Wang <wagzhi@gmail.com>

EXPOSE 9000 9999
RUN /usr/bin/workaround-docker-2267
RUN echo '172.16.102.245 dockerhost' >> /etc/workaround-docker-2267/hosts
WORKDIR /workspace/mb
RUN /usr/sbin/enable_insecure_key
RUN echo "export TZ='CST-8'" >> /root/.bashrc
CMD /sbin/my_init -- activator -jvm-debug
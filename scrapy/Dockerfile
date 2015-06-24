#
# https://github.com/dockerfile/python
#

# Pull base image.
FROM wagzhi/python 

# Install Python.
RUN sudo apt-get update 
RUN apt-get install -y libxml2-dev
RUN apt-get install -y libxslt1-dev
RUN apt-get install -y zlib1g-dev
RUN apt-get install -y libffi-dev
RUN ln -s /usr/include/libxml2/libxml   /usr/include/libxml
RUN pip install lxml
RUN pip install --upgrade pip
RUN pip install -I cffi==0.8.1
RUN apt-get install -y libssl-dev
RUN pip install scrapy

# Define working directory.
WORKDIR /data

# Define default command.
CMD ["bash"]

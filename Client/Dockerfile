FROM ubuntu:18.04
MAINTAINER Songjie Wang "wangso@missouri.edu"
RUN apt-get update -y
RUN apt-get -y install python-pip
RUN pip install -r requirements.txt
RUN git clone https://github.com/wangso/ImageProcessingWebServices.git
RUN WORKDIR ImageProcessingWebServices
RUN pip install -r requirements.txt
RUN cd ImageProcessingWebServices
RUN wget https://wangso-mec.s3.amazonaws.com/NextServer.txt
ENTRYPOINT ["python"]
CMD ["client.py"]

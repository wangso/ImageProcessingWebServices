FROM valian/docker-python-opencv-ffmpeg
MAINTAINER Songjie Wang "wangso@missouri.edu"
RUN apt-get update -y
RUN apt-get -y install python-pip
RUN git clone https://github.com/wangso/ImageProcessingWebServices.git
WORKDIR ImageProcessingWebServices
RUN pip install -r requirements.txt
RUN apt-get install wget
RUN pip install requests
RUN easy_install requests
ENTRYPOINT ["python"]
CMD ["client.py"]

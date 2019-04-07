# ImageProcessingWebServices

## Object Detection
[server.py](https://github.com/Blowoffvalve/ImageProcessingWebServices/blob/master/server.py) implements a RESTFUL webservice for object detection.
2 Endpoints currently exist

1. /imageProcessing: This uses openCv methods to find the objects that have changed from a preceding frame. It sends each object to /classifier.
2. /classifier: This is a deep learning model that attempts to classify an image into a fixed set of classes.
[client.py](https://github.com/Blowoffvalve/ImageProcessingWebServices/blob/master/client.py) reads a video and sends frames to server.py.

### Setup
1. Install your virtual environment to have the packages specified in [requirements.txt](https://github.com/Blowoffvalve/ImageProcessingWebServices/blob/master/requirements.txt).
2. Start the server by the flask app [server.py](https://github.com/Blowoffvalve/ImageProcessingWebServices/blob/master/server.py).

### Test
1. Unzip [testImages.rar](https://github.com/Blowoffvalve/ImageProcessingWebServices/blob/master/testImages.rar) to the same directory as server.py
2. Send Frame.jpg(it is inside testImages.rar) to a newly setup instance of the app.
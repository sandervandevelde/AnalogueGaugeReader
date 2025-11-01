# AnalogueGaugeReader
This repository is for reading out the value of a analogue Gauge, in this specific case a Hygro meter. The idea is that they hygro meter gets read periodically and registers the read values with the datetime time of the reading so that it can be tracked for later analysis.

In this README you will find the different stages/steps of developing the script with the goal described above in mind.


# Prerequisites
For following the steps/using this code you need to have certain python packages installed, the required packages can be found in the requirements.txt. To install all of them at once use pip install -r /path/to/requirements.txt .

# Step 1: reading an image
For the reading of images and live webcam feeds as well as the processing we will use OpenCV (https://opencv.org/) this is a package that focusses on providing functions for computer vision solutions.

For early development there is no need to use a livestream constantly, mostly because of convenience, however it will be tested in a later stage with a live camera feed. To do this we will use the opencv function called cv.imread({insert path to image}) with as argument the image we want to use. 

For livestreaming from a webcam make sure to create a capture device using cv.VideoCapture({insert webcam ID or address}) see: https://sandervandevelde.wordpress.com/2024/10/12/recording-rtsp-video-feeds-using-python-and-opencv/ for a detailed guide.

The image below will be used for demonstrative purposes.
![image info](./src/20251101_103702.jpg)
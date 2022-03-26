# Tensorflow Lite for Object Detection on a Raspberry Pi 4
Tensorflow object detection models are computationally expensive when used with low power devices such as raspebrry pi with slow inference. Fortunalty we have tensorflow lite models, lightweight deep learning models designed to efficiently run on low power devices and also provide faster inference time. Here is a step by step guide to install and run tensorflow lite models on a raspberry pi 4.


# What you need
1. A raspberry pi 4 (4GB is prefered)
2. A Screen to connect your raspberry pi
3. A keyboard and mouse for the raspberry pi
4. Raspberry pi 4 HDMI cable


# How to run
1. **sudo apt-get update** and **sudo apt-get upgrade** on your raspberry pi 4
2. Enable you camera in the raspberry pi configuration
3. Install virtualenv by doing **sudo pip3 install virtualenv**
4. Create a virtual environment by doing **python3 -m your-env-name** . It will create a folder with your-env-name to hold all the package for this virtual environment. Then activate your environment by running **source your-env-name/bin/activate**.
5. Inside your environment and main folder, run **bash get_pi_requirements.sh** to install all the necesssary packages to run the tensorflow lite object detection model
6. Download this repo
7.  Inside the downloaded folder:
   - pip3
8. Download the model weights and labels file from storage.googleapis.com/download.tensorflow.org/models/tflite/coco_ssd_mobilenet_v1_1.0_quant_2018_06_29.zip and unzip it inside a new folder named **models** that you will create.
9. run **python3 TFLite_detection_webcam.py --modeldir=models** to run the tensorflow object detection on your webcam.
10. run **python3 TFLite_detection_video.py --modeldir=models --video=your_video.mp4** to run the tensorflow object detection on a video. The argument --video in the code should point to your video.
11. run **python3 TFLite_detection_image.py --modeldir=models --video=image** to run the tensorflow object detection on images. The argument --image in the code should point to your image folder.


# INFERENCE

![image_0](https://user-images.githubusercontent.com/48753146/160236998-6ee528ac-8db2-4201-83fc-b258261dd836.jpg)


![image_2](https://user-images.githubusercontent.com/48753146/160237004-a4171e1e-50d7-44d7-bf5d-42b3a66e28ca.jpg)

# # Object Detection And Tracking

Object Detection And Tracking with Yolo and OpenCV

![alt text](https://github.com/gpdsec/ObjectDetectionAndTracking/blob/main/image/image.png?raw=true)

## **Objective Of Project**
Two build systems in which we feed video and a two points which form a line. Whenever any one of the targets crosses that line it will record his id, his image timestamp of video.

## **Project Details**

In this project, I used **Yolo** for person Detection and cascading it with **CSRT** tracker of **OpenCV**. Yolo used to detect bounding boxes from the first frame, which was later used to initialise Multitracker.  
I used *"CSRT"*  over *"KCF"* because it was not able to track fast-moving targets causing it to lose the bounding box even it was a lot faster than *"CSRT"*.  
During building this project, I had two choices to build the project. First, the choice was to build as it is. The second was to use ***TinyYolo*** to create a video feed for this project, but it will decrease our accuracy. Nevertheless, then it became object detection rather than object tracking. That's why I scrapped the idea. But I will use that in other projects.


##### **Libraries Used**
ImageAI with TensorFlow backend used for object detection.  
OpenCV is used for building tracker and video feed.
~~~python
from imageai.Detection import ObjectDetection
import cv2
~~~

##### **Inputs**
objectTracker function three inputs,
1. filename -string containing path to video
2. p1 - cordinate of point one
3. p2 - cordinate of point two
~~~python
def objectTracker(filename, p1, p2):
~~~
##### **Outputs**
It output video in which people being tracked.



**Note**- For More Information Look at code


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://github.com/gpdsec/ObjectDetectionAndTracking/blob/main/LICENSE)

# YOLO-V2-KERAS
This is a learning attempt on implementing YOLO-V2 algorithm for real time multiple object detection.

Localization — Refers to not only identifying is a given object is present inside an image, but also distinguishing the object’s location using a bounding box.
Detection — Simply refers to multiple localizations in a single image.

Reference :- https://pjreddie.com/media/files/papers/YOLO9000.pdf and https://pjreddie.com/darknet/yolo/

Key points of the implementation :-

Step:1 Divide the image using a grid (eg: 19x19)
Step:2 Dividing the image into a grid of smaller images increases the possibilities of object detection inside each cell easier.
Step:3 Perform image classification and Localization on each grid cell 
Step:4 A vector for each cell representing the probability of an object detected, the dimensions of the bounding box and class of the            detected image are given as the output at this step.
Step:5 Perform thresholding to remove multiple detected instances
Step:6 Thresholding picks the cells with the highest probabilities so that the more correcet bounding boxes are selected
Step:7 Perform Non-max suppression to refine the boxes more
Step:8 The technique of non-max suppression offers a convenient way to refine the results more using a calculation know as Intersection          over Union [IoU].

Anchor boxes make YOLO-V2 special as compared to others.Anchor boxes are used to detect several objects in one grid cell. 
The first implementation of Yolo was presented using a model in C known as Darknet by Joseph Redmon et al and over the evolution of the method, implementation with currently more popular ML libraries such as Tensorflow and Keras were also built.


# FingerCounterProject

We have created the Finger Counter Project by using OpenCV and Mediapipe library.

1. HandTrackingModule.py

First we have created basic hand tracking module which will track and draw the hand in realtime video.

In the 1st pythonfile file, Lets start by importing 2 libraries 
import cv2
import mediapipe as mp

Then we will capture the video through webcam  
cap = cv2.VideoCapture(0)

Next we have created a class handDetector where we have defined some variables like no of maxhands to detect, detection confidence etc.

In this class we have defines two important functions - 
1. findHands - which willl detect and draw the hand by connecting landmarks with line.
2. findPosition - which will give you the positions and ids of landmarks.

2. FingerCountingProject.py

Next, We have created main file  which will call the functions that we defines in our previous classs handDetector and will count the number of up fingers.
For counting no of fingers, lets consider the landmark no of every finger i.e. [4, 8, 12, 16, 20].(Given in the hand landmark image.)
We will calculate the (x,y) cordinates of every finger tip and check whether its y value is less than starting landmark point of its finger.
If value of y is less then the finger is said to be up otherwise it will be down.

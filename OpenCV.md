# OpenCV
## About:
OpenCV (Open Source Computer Vision Library) is a library for computer vision and image processing.It supports various programming language such as Python,C++,Java etc.
It can process images,object faces and even handwriting.OpenCV can run on the following desktop operating systems: Windows, Linux, macOS.
The library has more than 2500 optimized algorithms, which includes a comprehensive set of both classic and state-of-the-art computer vision and machine learning algorithms. These algorithms can be used to detect and recognize faces, identify objects, classify human actions in videos, track camera movements, track moving objects, extract 3D models of objects, produce 3D point clouds from stereo cameras, stitch images together to produce a high resolution image of an entire scene, find similar images from an image database, remove red eyes from images taken using flash, follow eye movements, recognize scenery and establish markers to overlay it with augmented reality, etc
All OpenCV array structure are converted to and from numpy arrays.
### Python stores the image as numpy/matrix of an array.
(i).If colored image-3D matrix 
 (ii).If B/W  image-2D matrix  

# Topics:
## 1. Basic operations of OpenCV
    (a).import OpenCV model-->import cv2
    (b).Read the image using cv2.imread("".jpg,1)
    (i).if colored image/RGB-->1
    (ii).if B/W image gray scale-->0

## 2. How Computer reads an image?
    Computer sees a matrix image of range from 0 to 255.
    Colored image-R,G,B(3 Channels)
    Black & White- 1 Channel 

## 3.How to tell the shape of the image
    print(img.shape)

## 4.Displaying the image
    To display the image-->cv2.imshow("",img)
    cv2.waitKey(0)    
    (a).User presses any key and the window will close.
    (b).If we specify a time say cv2.waitKey(2000) it will wait till 2000 ms and then destroy all windows.
    cv2.destroyAllWindows()
    
  ### Code 
    import cv2
    img=cv2.imread("",1) 
    cv2.imshow("",img)
    cv2.waitKey(2000)
    cv2.destroyAllWindows()
         
## 5. OpenCV to capture Videos.
    (a).Capture videos using webcam
        import cv2
        video=cv2.VideoCapture(0)
        video.release() (0 is used to specify that you will use webcam to capture videos.)
    (b).To add a time delay,we need time module
        import cv2,time
        video=cv2.VideoCapture(0)
        time.sleep(3) (This will stop the script for 3s)
        video.release()
    (c).To add a window to capture videos
        import cv2,time
        video=cv2.VideoCapture(0)
        check,frame=video.read   ( check returns bool type and frame is numpy represents first image captured)
        print(check)
        print(frame)
        time.sleep(3)
        video.release()

## 6. Capture Video
    1.Create frame object,which will read the image of video capture object.
    2.Show each frame of the video captured.
    
   ### Code
    import cv2,time
    video=cv2.VideoCapture(0)
    check,frame=video.read()
    time.sleep(3)
    cv2.imshow('Capturing',frame)
    cv2.waitKey(0)
    video.release()
    cv2.destroyAllWindows


        
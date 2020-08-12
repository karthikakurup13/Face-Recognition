>> ## What is opencv?

1. OpenCV (Open Source Computer Vision Library) is an open source computer vision and machine learning software library. 
2. The library has more than 2500 optimized algorithms. 
3. It has C++, Python, Java and MATLAB interfaces and supports Windows, Linux, Android and Mac OS. 
4. OpenCV library is widely used in Python for building real-time Machine Learning and Deep Learning applications.
5. Its cross-platform support and availability in multiple programming languages allow us to develop applications that 
  can be used on different systems. 
6. OpenCV is also fast and efficient as compared to the other libraries for computer vision (Caffe, Keras, etc).      

>> ## Features of opencv
1. Read and write images.
2. Capture and save videos.
3. Process images (filter, transform).
4. Perform feature detection.
5. Detect specific objects in the videos or images.
6. Analyze the video, i.e., estimate the motion in it, subtract the background, and track objects in it.

>> ## Applications
1. Biometrics (iris, finger print, face recognition).
2. Barcode and package label reading.
3. 2D/3D segmentation.
4. Surface Matching.
5. Text recognition.
6. Facial Recognition and Detection.

>> ## Using opencv for Images
### Read Image :
Use the function **cv2.imread()** to read an image. The image should be in the working directory or a full path of image 
should be given.

        import numpy as np
        import cv2
        img = cv2.imread('messi5.jpg',0)  
### Display an image :
Use the function **cv2.imshow()** to display an image in a window. The window automatically fits to the image size.
First argument is a window name which is a string. second argument is our image. You can create as many windows 
as you wish, but with different window names.

        cv2.imshow('image',img)
        cv2.waitKey(0)
        cv2.destroyAllWindows()
**cv2.waitKey()** is a keyboard binding function. Its argument is the time in milliseconds. The function waits for 
specified milliseconds for any keyboard event. If you press any key in that time, the program continues.      
**cv2.destroyAllWindows()** simply destroys all the windows we created. If you want to destroy any specific window, use
the function cv2.destroyWindow() where you pass the exact window name as the argument.
### Write an image
Use the function **cv2.imwrite()** to save an image.
First argument is the file name, second argument is the image you want to save.

        cv2.imwrite('messigray.png',img)
This will save the image in PNG format in the working directory.
### Resizing an image
To resize an image in Python, you can use **cv2.resize()** function of OpenCV library cv2.
Resizing, by default, does only change the width and height of the image. The aspect ratio can be preserved or not, 
based on the requirement. Aspect Ratio can be preserved by calculating width or height for given target height or width
respectively.
          
         resized = cv2.resize(image, (200, 200))
         cv2.imshow("Fixed Resizing", resized)
### Converting an image to grayscale
 
          gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
>> ## Using opencv for Videos
### Playing Video from file
For that we have to just change camera index with video file name. Also while displaying the frame, use 
appropriate time for cv2.waitKey(). If it is too less, video will be very fast and if it is too high, video will be slow . 

          import numpy as np
          import cv2
          cap = cv2.VideoCapture('vtest.avi')
          while(cap.isOpened()):
          ret, frame = cap.read()
          gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)
          cv2.imshow('frame',gray)
          if cv2.waitKey(1) & 0xFF == ord('q'):
          break
          cap.release()
          cv2.destroyAllWindows()
**cv2.VideoCapture(0)** we can capture video from camera      
          
        

# What is OpenCV?
###### OpenCV is a cross-platform library using which we can develop real-time computer vision(Computer Vision can be defined as a discipline that explains how to reconstruct, interrupt, and understand a 3D scene from its 2D images, in terms of the properties of the structure present in the scene.) applications. It mainly focuses on image processing, video capture and analysis including features like face detection and object detection. In other words, OpenCV is a huge open-source library for computer vision, machine learning, and image processing. OpenCV supports a wide variety of programming languages like Python, C++, Java, etc. 

### Computer Vision can be defined as a discipline that explains how to reconstruct, interrupt, and understand a 3D scene from its 2D images, in terms of the properties of the structure present in the scene.

### Computer Vision includes:Image Processing, Pattern Recognition, Photogrammetry

###### OpenCV was originally developed in C++. In addition to it, Python and Java bindings were provided. OpenCV runs on various Operating Systems such as windows, Linux, OSx, FreeBSD, Net BSD, Open BSD, etc.

# What are the features of OpenCV?
######    Using OpenCV library, you can: 1. Read and write images, 2. Capture and save videos, 3. Process images (filter, transform), 4. Perform feature detection, 5. Detect specific objects such as faces, eyes, cars, in the videos or images, 6. Analyze the video, i.e., estimate the motion in it, subtract the background, and track objects in it.    
    
# How to import an image using OpenCV?
######    After importing the required libraries like imutils, numpy and cv2 we move to the next step of loading images.
    
## Loading images in OpenCV:

######    CODE:    
######    img = cv.imread("image file name")
######    cv.imshow("output window",img)
######    cv.waitkey()

### After importing image on terminal using img = cv.imread("image file name") and then img we will get a series of numbers in matrix arranges in array format, here dimension is denoted by the number of brackets present at the starting of array.

### To find size use img.shape indicating as (c,r,d) where c denotes number of columns, r denotes number of rows and d denotes the dimension. Dimension 3 mean, containing 3 matrix, by using RGB concept(where first matrix denote all pixel containing red value similarly, second green and third blue).

#### for grayscle the dimension will be equal to 1.

#### value of grayscale varies from 0 to 255 where 0 stands for absolute black and 255 for absolute white. The value in between indicate gray values. 

## Displaying the image

###### To display the image we use cv2.imshow("",img) and cv2.waitKey() -----> cv2,imshow("file name",img) help show the output and cv2.waitKey() help specify a time untill which the output window wil persist say '100' ms that means the window will stay for 100 ms. Normally it is set to '0' to avoid time dependency. 
   
## Loading a video in OpenCV:

######   CODE:
######   video=cv2.VideoCapture(0)
######   print(video)
######   ret,frame = video.read()
######   print(ret)
######   print(frame)
######   video=cv2.VideoCapture(0) ----> using this command we can load a video.

######   Video is stored as object first to be presented later ---> print(video).Then using ---> ret,frame = video.read() we can read the video and then print(ret) along with print(frame) help display where ret is a variable that contain true or false, help detect whether the ead was successfull or not.

######   if ret = true that means image read successfully if false then error reading image.

######   print(frame) contain our image.

######   Now to show the video we use a while loop.








# Image_Acqusition-_using_Web_Camera
# Aim

To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.

i) Write the frame as JPG 

ii) Display the video 

iii) Display the video by resizing the window

iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7


# Algorithm
# Step 1:
Use cv2.VideoCapture(0) to access web camera

# Step 2:
Use cv2.imread to read the video or image

# Step 3:
Use cv2.imwrite to save the image

# Step 4:
Use cv2.imshow to show the video

# Step 5:
End the program and close the output video window by pressing 'q'

# Program:
### Developed By:VAISHNAVI S
### Register No:212222230165

# i) Write the frame as JPG file
```
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("anbu.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```
# ii) Display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('lion',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
# iii) Display the video by resizing the window
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222240009_anbu',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
# iv) Rotate and display the video
```
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222240009_anbu',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
# Output
# i) Write the frame as JPG image

![di1](https://github.com/Vaishnavi-saravanan/Image_Acqusition-_using_Web_Camera/assets/118541897/3b68ac38-b860-49aa-a033-e16aa74ffd5f)

# ii) Display the video

![di2](https://github.com/Vaishnavi-saravanan/Image_Acqusition-_using_Web_Camera/assets/118541897/e7b659df-9b1b-482a-9dc1-eb42d3629b77)

# iii) Display the video by resizing the window
![di3](https://github.com/Vaishnavi-saravanan/Image_Acqusition-_using_Web_Camera/assets/118541897/a549ccf8-c710-40d1-9906-1f8be47b0ea6)


# iv) Rotate and display the video

![di4](https://github.com/Vaishnavi-saravanan/Image_Acqusition-_using_Web_Camera/assets/118541897/0ced0d7a-b8f7-4b59-a5c0-46373778cc3b)


# Result:
Thus the image is accessed from webcamera and displayed using openCV.

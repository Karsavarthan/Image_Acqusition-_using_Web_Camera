# Image_Acqusition-_using_Web_Camera
## Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera.

### Step 2:
Use cv2.imread to read the video or image.

### Step 3:
Use cv2.imwrite to save the image.

### Step 4:
Use cv2.imshow to show the video.

### Step 5:
End the program and close the output video window by pressing 'q'.


## Program:
``` Python
Developed By: karsavarthan r r
Register No: 212223230100
```
## i) Write the frame as JPG file
```
import cv2
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()
```
## ii) Display the video
```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()

```
## iii) Display the video by resizing the window
```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()

```

## iv) Rotate and display the video
```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```
## Output

### i) Write the frame as JPG image
![WhatsApp Image 2025-04-30 at 11 50 04_35f79b5e](https://github.com/user-attachments/assets/0016fe2a-c671-48db-bc60-860c2129fe0e)



### ii) Display the video

![WhatsApp Image 2025-04-30 at 11 50 04_35f79b5e](https://github.com/user-attachments/assets/e5ca92c7-174f-4847-9dbe-bde2cce75a50)



### iii) Display the video by resizing the window

![WhatsApp Image 2025-04-30 at 11 50 09_07058a00](https://github.com/user-attachments/assets/f178a94c-4969-4153-a097-11edb98dd0c6)



### iv) Rotate and display the video

![WhatsApp Image 2025-04-30 at 11 50 16_2f5d5891](https://github.com/user-attachments/assets/36aeef7c-4b81-41ac-9580-cb8a23b8d705)






## Result:
Thus the image is accessed from webcamera and displayed using openCV.

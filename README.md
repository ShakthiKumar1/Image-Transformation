# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using M=np.float32([[1,0,20],[0,1,50],[0,0,1]]) translated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step3:
Scale the image using M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]]) scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step4:
Shear the image using M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]]) sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

### Step5:
Reflection of image can be achieved through the code M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]]) reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

## Program:
```python
Developed By: Shakthi kumar S
Register Number:212222110043
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("sk1.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)![DIP05-1](https://user-images.githubusercontent.com/121041644/230330081-8ed64e92-2d84-4a7c-bb54-ef299021fe8f.png)![DIP05-1](https://user-images.githubusercontent.com/121041644/230330128-9e5182a2-96e7-43cb-b1ae-8c3648a414c9.png)![DIP05-1](https://user-images.githubusercontent.com/121041644/230330157-3d68d13f-9c1e-4820-be1c-eb20db8ba78d.png)



plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape

i)Image Translation

M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()

ii) Image Scaling

M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

iii)Image shearing

M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()

iv)Image Reflection

M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()

v)Image Rotation

angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

vi)Image Cropping

cropped_img=input_img[20:150,60:230]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()

## Output:
### i)Image Translation

![DIP05-1](https://user-images.githubusercontent.com/121041644/230330325-3745a382-a3e5-4c98-8149-00b820e2e703.png)

### ii) Image Scaling

![DIP05-2](https://user-images.githubusercontent.com/121041644/230330426-c06275be-a2fe-4628-b255-8864f458ba4c.png)

### iii) Image Shering

![DIP05-3](https://user-images.githubusercontent.com/121041644/230328946-41c5d1f1-81eb-48ef-88ea-6ffceab2f576.png)

### iv) Image Reflection

![DIP05-4](https://user-images.githubusercontent.com/121041644/230329129-a78960e0-8e92-4b53-8268-2d22a1cc9157.png)

### v)Image Rotation

![DIP05-5](https://user-images.githubusercontent.com/121041644/230329405-28c09a44-a78b-480b-92dd-3ccdc4c2af60.png)

### vi)Image Cropping

![DIP05-6](https://user-images.githubusercontent.com/121041644/230329458-1f03d765-fc68-45d3-9d42-3c9e1b46651d.png)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.

# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import the required libraries and read the original image.

### Step2:
<br>
Translate the image.

### Step3:
<br>
Scale the image.

### Step4:
<br>
Shear the image.

### Step5:
<br>
Find reflection of image.

### Step6:
<br>
Rotate the image.

### Step7:
<br>
Crop the image.

### Step8:
<br>
Display all the Transformed images.

## Program:
```python
Developed By:HARIDHARSHINI.S
Register Number:212221230033
```
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("santaa.jpeg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim = input_image.shape


i)Image Translation

M = np.float32([[1,0,50],
               [0,1,100],
               [0,0,1]])
translated_image = cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()


ii) Image Scaling

M = np.float32([[2.5,0,0],
               [0,3.8,0],
               [0,0,1]])
scaled_image = cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()


iii)Image shearing

M_x = np.float32([[1,0.5,0],
                 [0,1,0],
                 [0,0,1]])
M_y = np.float32([[1,0,0.5],
                 [0.5,1,0],
                 [0,0,1]])
sheared_xaxis = cv2.warpPerspective(input_image,M_x,(int(cols*1.5),int(rows*1.5)))
sheared_yaxis = cv2.warpPerspective(input_image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_yaxis)
plt.show()


iv)Image Reflection

M_x = np.float32([[1,0,0],
                 [0,-1,rows],
                 [0,0,1]])
M_y = np.float32([[-1,0,cols],
                 [0,1,0],
                 [0,0,1]])
reflected_xaxis = cv2.warpPerspective(input_image,M_x,(int(cols),int(rows)))
reflected_yaxis = cv2.warpPerspective(input_image,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_yaxis)
plt.show()


v)Image Rotation

angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_image = cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_image)
plt.show()


vi)Image Cropping

cropped_image = input_image[100:300,120:300]
plt.axis('off')
plt.imshow(cropped_image)
plt.show()
```
## Output:

![image](https://user-images.githubusercontent.com/94168395/231360201-2f8341c5-9736-47f0-a9de-a603b93b3e74.png)

### i)Image Translation
<br>
<br>

![ex 5 a](https://user-images.githubusercontent.com/94168395/231362173-df126947-1504-4b31-94aa-2b68258409df.png)

<br>
<br>

### ii) Image Scaling
<br>
<br>

![ex 5 b](https://user-images.githubusercontent.com/94168395/231361274-7f2ccd64-a0e1-4b92-b966-cfb8175c354e.png)
<br>
<br>


### iii)Image shearing
<br>
<br>
![ex 5 c](https://user-images.githubusercontent.com/94168395/231361316-55e37ffd-99f6-42a5-a632-10ebd7097e9e.png)
<br>
<br>


### iv)Image Reflection
<br>
<br>
![ex 5 d](https://user-images.githubusercontent.com/94168395/231361351-a6cdfb78-c3cc-4d2b-a18f-ec1494edec23.png)
<br>
<br>



### v)Image Rotation
<br>
<br>
![ex 5 e](https://user-images.githubusercontent.com/94168395/231361377-5694f876-479f-4915-9381-46b9e33dfb6f.png)
<br>
<br>



### vi)Image Cropping
<br>
<br>
![ex 5 f](https://user-images.githubusercontent.com/94168395/231361419-2a6c4bde-d7e3-4838-8006-e0313cf62be2.png)
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.

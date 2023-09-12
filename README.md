# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1:
Import the necessary libraries and read the original image and save it as a image variable.
<br>

### Step2:
Translate the image.
<br>

### Step3:
Scale the image.
<br>

### Step4:
Shear the image.
<br>

### Step5:
Find reflection of image.
<br>

### Step6:
Rotate the image.
<br>
### Step7:
Crop the image.
<br>
### Step8:
Display all the Transformed images.
<br>


## Program:
```python
Developed By: GURUMOORTHI R
Register Number: 212222230042
```
```
i)Image Translation

import numpy as np
import cv2
import matplotlib.pyplot as plt
dipt_image = cv2.imread("dipt.jpg")
dipt_image = cv2.cvtColor(dipt_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(dipt_image)
plt.show()
rows,cols,dim = dipt_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image = cv2.warpPerspective(dipt_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()


ii) Image Scaling

import numpy as np
import cv2
import matplotlib.pyplot as plt
dipt_image = cv2.imread("dipt.jpg")
dipt_image = cv2.cvtColor(dipt_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(dipt_image)
plt.show()
rows,cols,dim = dipt_image.shape
M = np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
scaled_img = cv2.warpPerspective(dipt_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

iii)Image shearing

import numpy as np
import cv2
import matplotlib.pyplot as plt
dipt_image = cv2.imread("dipt.jpg")
dipt_image = cv2.cvtColor(dipt_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(dipt_image)
plt.show()
rows,cols,dim = dipt_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(dipt_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(dipt_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()


iv)Image Reflection

import numpy as np
import cv2
import matplotlib.pyplot as plt
dipt_image = cv2.imread("dipt.jpg")
dipt_image = cv2.cvtColor(dipt_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(lion_image)
plt.show()
rows,cols,dim = lion_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(dipt_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(dipt_image,M_Y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()



v)Image Rotation

import numpy as np
import cv2
import matplotlib.pyplot as plt
dipt_image = cv2.imread("dipt.jpg")
dipt_image = cv2.cvtColor(dipt_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(dipt_image)
plt.show()
rows,cols,dim = dipt_image.shape
angle = np.radians(30)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(dipt_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()


vi)Image Cropping

import numpy as np
import cv2
import matplotlib.pyplot as plt
dipt_image = cv2.imread("dipt.jpg")
dipt_image = cv2.cvtColor(dipt_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(dipt_image)
plt.show()
rows,cols,dim = dipt_image.shape
cropped_img=dipt_image[11:500,27:630]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()




```
## Output:
### i)Image Translation

![1](https://github.com/gururamu08/IMAGETRANSFORMATION/assets/118707009/a9a236a5-a4a5-4a2c-8f44-502661e33ff9)

<br>

### ii) Image Scaling

![2](https://github.com/gururamu08/IMAGETRANSFORMATION/assets/118707009/e7be5415-9d1a-48e8-816a-e6015296e3fd)

<br>


### iii)Image shearing

![3](https://github.com/gururamu08/IMAGETRANSFORMATION/assets/118707009/ccb2630d-426c-4c2b-935f-e4f072e2dde1)
![4](https://github.com/gururamu08/IMAGETRANSFORMATION/assets/118707009/a92b520a-c337-421f-85f5-9c077b260c28)

<br>


### iv)Image Reflection

![5](https://github.com/gururamu08/IMAGETRANSFORMATION/assets/118707009/13e5bf5f-a5b6-40d1-910a-07498206a8d3)


<br>



### v)Image Rotation

![6](https://github.com/gururamu08/IMAGETRANSFORMATION/assets/118707009/497029af-74f8-49d3-99f6-9c7bfad5a836)

<br>



### vi)Image Cropping

![7](https://github.com/gururamu08/IMAGETRANSFORMATION/assets/118707009/40e81e1d-3e0e-4273-bb30-e5930ac5323f)

<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.

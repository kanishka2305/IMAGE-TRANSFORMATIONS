# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Import the required packages

### Step2:
<br>
Load the image file in the program.

### Step3:
<br>
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4:
<br>
Display the modified image output.

### Step5:
<br>
End the program.

## Program:
```python
Developed By: KANISHKA V S
Register Number: 212222230061
```
#### i)Image Translation
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread( "/content/dipt image.png")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis( 'off')
plt.imshow(input_image)
plt.show()
rows,cols,dim =input_image.shape
M =np.float32([[1,0,100],
               [0,1,100],
               [0,0,1]])
translated_image =cv2.warpPerspective(input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

#### ii) Image Scaling
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("/content/dipt image.png")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1.5,0 ,0],
              [0,1.8,0],
              [0,0,1]])
scaled_img=cv2.warpPerspective(in_img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```

#### iii)Image shearing
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("/content/dipt image.png")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()
```

#### iv)Image Reflection
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("/content/dipt image.png")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  

```

#### v)Image Rotation
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("/content/dipt image.png")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```

#### vi)Image Cropping
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("/content/dipt image.png")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[2000:3000 ,1000:2500]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation
![image](https://github.com/kanishka2305/IMAGE-TRANSFORMATIONS/assets/113497357/4a95f5af-fa9b-4e03-92ab-b43d5013de6a)


### ii) Image Scaling
![image](https://github.com/kanishka2305/IMAGE-TRANSFORMATIONS/assets/113497357/cd02e76a-7279-4e04-a8fc-0785029f32bd)


### iii)Image shearing
![image](https://github.com/kanishka2305/IMAGE-TRANSFORMATIONS/assets/113497357/9841f537-e871-4e28-9e1e-3d6cab813046)


### iv)Image Reflection
![image](https://github.com/kanishka2305/IMAGE-TRANSFORMATIONS/assets/113497357/8234ac6f-dba2-4563-a06b-4895d8ad9b66)


### v)Image Rotation
![image](https://github.com/kanishka2305/IMAGE-TRANSFORMATIONS/assets/113497357/90e72f5f-c838-4b65-b650-bd5b51c4908f)


### vi)Image Cropping
![image](https://github.com/kanishka2305/IMAGE-TRANSFORMATIONS/assets/113497357/d92b9cab-34c9-46e7-9f57-bbf2ba206d9c)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.

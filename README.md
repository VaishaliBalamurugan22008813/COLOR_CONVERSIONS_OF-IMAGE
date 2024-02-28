# EX-01 COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
 #### Step1: Choose an image and save it as a filename.jpg ,
 #### Step2: Use imread(filename, flags) to read the file.
 #### Step3: Use imshow(window_name, image) to display the image.
 #### Step4: Use imwrite(filename, image) to write the image.
 #### Step5: End the program and close the output image windows.
 #### Step6: Convert BGR and RGB to HSV and GRAY
 #### Step7: Convert HSV to RGB and BGR
 #### Step8: Convert RGB and BGR to YCrCb
 #### Step9: Split and Merge RGB Image
 #### Step10: Split and merge HSV Image

### Program:
```
### Developed By: VAISHALI BALAMURUGAN
### Register Number: 212222230164
```
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
  import cv2
  image=cv2.imread('diptex1.jpg')
  cv2.imshow('vaishali',image)
  cv2.waitKey(0)
  cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:
![image](https://github.com/VaishaliBalamurugan22008813/COLOR_CONVERSIONS_OF-IMAGE/assets/119390134/3469f0ed-5a75-4902-8534-4fd94cd97de2)


  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
   import cv2
   image=cv2.imread('diptex1.jpg',0)
   cv2.imwrite('demos.jpg',image)
```
  </td>
  <td>

### OUTPUT:
![image](https://github.com/VaishaliBalamurugan22008813/COLOR_CONVERSIONS_OF-IMAGE/assets/119390134/fda2560d-adc6-43dc-a198-fe68cbcdd071)


  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
import cv2
image=cv2.imread('diptex1.jpg',1)
print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![image](https://github.com/VaishaliBalamurugan22008813/COLOR_CONVERSIONS_OF-IMAGE/assets/119390134/7ca9bb57-d816-4e72-873d-187711dfbdf8)

  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
import random
import cv2
image=cv2.imread('diptex1.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                     random.randint(0,255),
                     random.randint(0,255)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:
![image](https://github.com/VaishaliBalamurugan22008813/COLOR_CONVERSIONS_OF-IMAGE/assets/119390134/af51861d-f4d1-4872-a72f-aa1379c6897d)

  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
import cv2
image=cv2.imread('diptex1.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('partimage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:
![image](https://github.com/VaishaliBalamurugan22008813/COLOR_CONVERSIONS_OF-IMAGE/assets/119390134/60f64c36-d4df-4147-b561-6be5af0590db)

  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('diptex1.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/VaishaliBalamurugan22008813/COLOR_CONVERSIONS_OF-IMAGE/assets/119390134/d1574187-5a43-4fac-9404-60833a4465d0)


### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('diptex1.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/VaishaliBalamurugan22008813/COLOR_CONVERSIONS_OF-IMAGE/assets/119390134/3b8f7311-4ae9-4ca0-bb61-f8b073071e38)



### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('diptex1.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/VaishaliBalamurugan22008813/COLOR_CONVERSIONS_OF-IMAGE/assets/119390134/8a3a8217-e316-4c07-97d9-783ee20c805a)



### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('diptex1.jpg',1)
img = cv2.resize(img,(300,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/VaishaliBalamurugan22008813/COLOR_CONVERSIONS_OF-IMAGE/assets/119390134/2947c137-90bc-4b19-93c6-20e2e14b78ff)



### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("diptex1.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/VaishaliBalamurugan22008813/COLOR_CONVERSIONS_OF-IMAGE/assets/119390134/5a43c8a3-0b8c-49ab-a484-261293de8832)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.








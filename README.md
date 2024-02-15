# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By:
### Register Number: 

### i) Read and display the image:
```
import cv2
color_img=cv2.imread('123.jpg',1)
cv2.imshow('sakthivel',color_img)
cv2.waitKey(0)
```
### ii)Write the image
```
import cv2
color_img=cv2.imread('123.jpg',1)
w= cv2.imwrite('0.png',color_img)
cv2.imshow('0',color_img)
cv2.waitKey(0)
```
### ii)Write the image
```
import cv2
import random
color_img=cv2.imread('123.jpg',1)
print(color_img.shape)
```
### iv)Access rows and columns:
```
import cv2
import random
color_img=cv2.imread('123.jpg',1)
for i in range(100):
    for j in range(color_img.shape[1]):
        color_img[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2.imshow('212222230053_jeeva',color_img)
cv2.waitKey(0)
```
### v)Cut and paste portion of image:
```
import cv2
color_image=cv2.imread('123.jpg',1)
tag=color_image[5:15,5:15]
color_image[10:20,10:20]=tag
cv2.imshow("sakthivel",color_image)
cv2.waitKey(0)

```
### vi) BGR and RGB to HSV and GRAY
```
import cv2

flower_image = cv2.imread('123.jpg')
cv2.imshow('Original Image', flower_image)

hsv_bgr_image = cv2.cvtColor(flower_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV', hsv_bgr_image)

hsv_rgb_image = cv2.cvtColor(flower_image, cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV', hsv_rgb_image)

gray_bgr_image = cv2.cvtColor(flower_image, cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY', gray_bgr_image)

gray_rgb_image = cv2.cvtColor(flower_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_rgb_image)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### vii) HSV to RGB and BGR:
```
import cv2

flower_hsv_image = cv2.imread('123.jpg')
cv2.imshow('Original HSV Image', flower_hsv_image)

rgb_image = cv2.cvtColor(flower_hsv_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV to RGB', rgb_image)

bgr_image = cv2.cvtColor(flower_hsv_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to BGR', bgr_image)

cv2.waitKey(0)
cv2.destroyAllWindows()

```


### viii) RGB and BGR to YCrCb:
```
import cv2
image = cv2.imread('123.jpg')
cv2.imshow('Original Image', image)
ycrcb_image_rgb = cv2.cvtColor(image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB to YCrCb', ycrcb_image_rgb)
ycrcb_image_bgr = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR to YCrCb', ycrcb_image_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### ix) Split and merge RGB Image:

```
import cv2
image = cv2.imread('123.jpg')
cv2.imshow('Original Image', image)
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel', blue)
cv2.imshow('G-Channel', green)
cv2.imshow('R-Channel', red)
merged_bgr = cv2.merge((blue, green, red))
cv2.imshow('Merged BGR Image', merged_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### x) Split and merge HSV Image:
```
import cv2

image = cv2.imread('123.jpg')
cv2.imshow('Original Image', image)

hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)

cv2.imshow('Hue - Image', h)
cv2.imshow('Saturation - Image', s)
cv2.imshow('Value - Image', v)

merged_hsv = cv2.merge((h, s, v))
cv2.imshow('Merged HSV Image', merged_hsv)

cv2.waitKey(0)
cv2.destroyAllWindows()
```




## Output:

### i) Read and display the image:

![Screenshot 2024-02-15 110720](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/7f8f7cd2-bcf9-4454-8d91-f0270e78e2c4)



<br>
<br>

### ii)Write the image


![Screenshot 2024-02-15 110748](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/ad26c108-5c1a-4fc7-a154-cdbf63fad82e)



<br>
<br>

### iii)Shape of the Image:
![Screenshot 2024-02-15 110804](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/251f3c7e-c57d-436b-8d52-39be654c3439)



<br>
<br>

### iv)Access rows and columns:

![Screenshot 2024-02-15 110839](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/41013503-5506-476c-8206-ca94732ea3d6)


<br>
<br>

### v)Cut and paste portion of image:
![Screenshot 2024-02-15 111759](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/dd108bef-d589-4303-8927-4af6c9785663)


<br>
<br>

### vi) BGR and RGB to HSV and GRAY
![Screenshot 2024-02-15 105247](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/bf523e29-e11d-4ef9-b71a-459bf84439f9)
<br>
![Screenshot 2024-02-15 105300](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/e99f83f1-aefb-4e98-8024-d2bad6e98e46)
<br>
![Screenshot 2024-02-15 105316](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/38addac5-550b-4aa2-a154-b33a29916195)
<br>
![Screenshot 2024-02-15 105330](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/b1da695f-7c82-4d49-ab56-f1560bb1ab3a)
<br>
![Screenshot 2024-02-15 105341](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/58d62a74-49d6-49df-86a0-d5d5dde472bf)
<br>



<br>
<br>

### vii) HSV to RGB and BGR:
![Screenshot 2024-02-15 105247](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/d2905543-2c53-4803-af31-8fe99d779be8)
<br>
![Screenshot 2024-02-15 105525](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/d4b76c98-a05b-47df-9d05-321a48e66640)
<br>
![Screenshot 2024-02-15 105456](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/ee7b8407-b76f-4622-a62a-d0a0ec0a19d6)




<br>
<br>

### viii) RGB and BGR to YCrCb:
![Screenshot 2024-02-15 105247](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/acefe2d2-c923-47da-8327-9afb5ca44016)
<br>
![Screenshot 2024-02-15 112918](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/3a4e7eca-a37c-4334-8358-c9510facac41)
<br>
![Screenshot 2024-02-15 112857](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/488f28df-3c7e-4b79-a804-0a5c33d6eea7)


<br>
<br>

### ix) Split and merge RGB Image:
![Screenshot 2024-02-15 105247](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/b9410190-b8f5-4ce9-a29c-863ac203d81e)
<br>
![Screenshot 2024-02-15 110252](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/8a67b886-902a-4be8-974e-3013d9bdb13f)
<br>
![Screenshot 2024-02-15 110303](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/0e2cd4d4-80f9-4e4a-8fbe-082968454580)
<br>
![Screenshot 2024-02-15 110258](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/fce91289-f949-49a3-8f08-cd5e593cfee9)
<br>
![Screenshot 2024-02-15 110226](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/f3e5e332-3a7f-47e4-9f9a-a2777af4cd11)


<br>
<br>

### x) Split and merge HSV Image:
![Screenshot 2024-02-15 105247](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/e3ae11f2-53cb-4d89-aa53-a1d736028867)
<br>
![Screenshot 2024-02-15 110355](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/b2ef057b-2852-4247-af38-43e4d4be934a)
<br>
![Screenshot 2024-02-15 110400](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/908c0bf9-db0d-453c-a4ae-3cc2e0e30a1e)
<br>
![Screenshot 2024-02-15 110405](https://github.com/sakthivel005/COLOR_CONVERSIONS_OF-IMAGE/assets/120550359/64cfbb1f-ac82-492e-988f-1ece19929aed)



<br>
<br>





## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.








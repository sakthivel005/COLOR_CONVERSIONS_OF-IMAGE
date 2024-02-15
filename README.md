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
### Developed By: GOKUL J
### Register Number: 212222230038 




### i) Read and display the image                  
                                                      
 
  
 ```import cv2                                                      
    image=cv2.imread('lily.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('Gokul J',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
 ```

## Output:
  ![Screenshot 2024-02-15 145958](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/5e323ed8-f85c-4179-9645-feac56b1861e)

### ii)Write the image                         
                                                      
 ```import cv2
    image=cv2.imread('lily.jpg',0)
    cv2.imwrite('d.jpg',image)
```
## Output:
  ![Screenshot 2024-02-15 150603](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/456288b6-6a8b-432b-b007-61b53e9ccad2)
      
### iii)Shape of the Image                           
                                                          
``` import cv2
    image=cv2.imread('space1.jpg',1)
    print(image.shape)
```
## Output:
![Screenshot 2024-02-15 150652](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/71f9a7e9-4a89-4423-b654-96f4747d5a7f)
                                                     
### iv)Access rows and columns                    
                                                       
```import random
    import cv2
    image=cv2.imread('lily.jpg',1)
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

## Output:
  ![Screenshot 2024-02-15 150821](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/d489bf8f-a62d-4b80-bbd8-71584d442a0f)
### v)Cut and paste portion of image               
```import cv2
   image=cv2.imread('lily.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('partimage1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
 
## Output:
  ![Screenshot 2024-02-15 150908](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/961e9455-504a-49a2-bfc2-4831cfc55ac1)

### vi) BGR and RGB to HSV and GRAY           
```import cv2
img = cv2.imread('lily.jpg',1)
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

## Output:
![Screenshot 2024-02-15 150953](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/f1ab3618-070f-4abd-a108-e8b9c0896d28) ![Screenshot 2024-02-15 151041](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/3fdfd6b3-edad-4bbd-8ade-349e25fc9a9a)

![Screenshot 2024-02-15 151014](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/064085ab-97ea-4fe3-9429-ef762c1501bd) ![Screenshot 2024-02-15 151059](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/c4638f94-1ad4-4674-9c2d-1ce3a1ee24e6)

![Screenshot 2024-02-15 151111](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/c17d8d12-88c2-4222-8a7a-2d942ba53c75)


### vii) HSV to RGB and BGR
```import cv2
img = cv2.imread('lily.jpg')
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
## Output:
![Screenshot 2024-02-15 151152](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/e71dc3fd-a499-42a4-8346-31b342521f9b) ![Screenshot 2024-02-15 151218](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/2279f70b-b5e8-4d80-b510-e478c0d7cf5e)

![Screenshot 2024-02-15 151205](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/ddfb22b9-f17a-4e7e-a854-af8b30b949ef)


### viii) RGB and BGR to YCrCb
```import cv2
img = cv2.imread('lily.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![Screenshot 2024-02-15 151329](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/63959b4b-4bf7-4104-bdfc-3887ea716ee4) ![Screenshot 2024-02-15 151404](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/e5a7c534-656a-4a82-b936-01a92fd35fad)

![Screenshot 2024-02-15 151341](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/324e9744-6223-4fd3-b395-20993e0abb99)

### ix) Split and merge RGB Image
```import cv2
img = cv2.imread('lily.jpg',1)
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
##  Output:
![Screenshot 2024-02-15 151445](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/f037a556-9378-4cf2-b036-083b31b58209) ![Screenshot 2024-02-15 151500](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/3bf3468e-c76b-4987-84da-0fb23f7ca54a)

![Screenshot 2024-02-15 151523](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/5dd2d990-53f9-4fdf-87c6-6a3f0a7b69a0) ![Screenshot 2024-02-15 151537](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/28ef4aef-6ea0-4ce3-b61f-e98e2f8e7ed0)




### x) Split and merge HSV Image
```import cv2
img = cv2.imread("lily.jpg",1)
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

## Ouput:
![Screenshot 2024-02-15 151646](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/c2e1719a-6dd2-4b20-bcd1-664eeeec1aa3) ![Screenshot 2024-02-15 151608](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/98755682-209a-4aa3-9068-5add974d3df9)
![Screenshot 2024-02-15 151622](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/90f972cd-3ffa-4088-bc8d-223af79300e8) ![Screenshot 2024-02-15 151634](https://github.com/Gokul0117/COLOR_CONVERSIONS_OF-IMAGE/assets/121165938/4b72062f-36d2-4f0c-9d5e-e7993f288f57)




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







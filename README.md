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


## Output:

### i) Read and display the image

<br>
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("dog.jpeg",1)
cv2.imshow("display window",img)
cv2.waitKey(0)
cv2.destroyAllWindows()
print(img.shape)
<br>
## Output
![Screenshot (27)](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/9b4aec82-0690-44a6-b90b-f17aa66590be)

### ii)Write the image

<br>
img1=cv2.imread("dog.jpeg",0)
cv2.imshow("display window",img1)
cv2.waitKey(0)
cv2.destroyAllWindows()
cv2.imwrite('greyscale.jpeg',img1)
<br>

## Output
![Screenshot 2024-02-22 184132](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/4cb3a2bc-5cb0-4877-b5c4-84e194382d36)

### iii)Shape of the Image

<br>
import cv2
img1=cv2.imread("dog.jpeg",1)
print(img1.shape)
<br>

## Output
![Screenshot 2024-02-22 184909](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/16aabdf4-ac64-436f-9293-444be5f07a0d)

### iv)Access rows and columns
<br>
import random
import cv2
image=cv2.imread('dog.jpeg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255), random.randint(0,255), random.randint(0,255)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
<br>

## Output
![Screenshot 2024-02-22 185319](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/5bac937c-4064-4659-b184-42566fd6612d)

### v)Cut and paste portion of image
<br>
<br>

### vi) BGR and RGB to HSV and GRAY
<br>
import cv2
img2 = cv2.imread("dog,jpeg")
x = 0
y = 200
x1 = 160
y1 = 450
x2 = 0
y2 = 0
cropimg = img2[x:x1+x2, y:y1+y2]
cv2.imshow("Original Image", img2)
cv2.imshow("Cropped Image", cropimg)
cv2.waitKey(0)
cv2.destroyAllWindows()
<br>

## Output
![Screenshot (27)](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/dc84632b-76ff-433f-bb1e-29ad4c9eb077)

### vii) HSV to RGB and BGR
<br>
import cv2
img = cv2.imread('pvr.jpg',1)
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
<br>

## Output
![Screenshot (29)](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/602fde69-e577-4e58-82e6-52a8b5a1e3b6)


### viii) RGB and BGR to YCrCb
<br>
import cv2
img = cv2.imread('pvr.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
<br>

## Output
![Screenshot (29)](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/d00577b2-232e-47fe-b90c-244278fe8f02)


### ix) Split and merge RGB Image
<br>
<br>

### x) Split and merge HSV Image
<br>
<br>




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.








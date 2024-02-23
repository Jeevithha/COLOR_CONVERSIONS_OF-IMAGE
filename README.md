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

## Program:
### Developed By:JEEVITHA S
### Register Number: 212222100016

### i) Read and display the image
```
    import cv2
    image=cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('Original Image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
## Output
![306613280-0a9b3e8a-ab85-48e8-9d9d-5d4212423e5f](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/f7a80922-a292-4a1b-854c-a6517e7f63c3)

### ii)Write the image
```
    import cv2
    image=cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',0)
    cv2.imwrite('demos.jpg',image)
```
## Output
![306613502-9e4b1121-3227-46ee-8cf2-0904bc4c8355](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/ecddb488-c34d-4a2e-9a9a-402d689d492d)
### iii)Shape of the Image

```
    import cv2
    image=cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',1)
    print(image.shape)
```
## Output
![306613865-cc723874-87d0-49fe-bd96-ffba7b8cc99c](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/0fce2dfb-cfe1-4e5a-8664-4b9dbc6c3447)
### iv)Access rows and columns
```
    import random
    import cv2
    image=cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',1)
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
## Output
![306614092-a4e2d451-5459-4f9d-883f-c212a23ee952](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/2e7718b5-9fe8-4f41-b0b6-ca3fd11e11f6)
### v)Cut and paste portion of image
```
   import cv2
   image=cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[150:200,110:160]
   image[110:160,150:200] = tag
   cv2.imshow('partimage1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
## Output
![306614251-ad2712ae-a7e0-44ae-95ad-e18beec06c94](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/0175c42b-477a-41bb-b989-10d3af1c7880)
### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',1)
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
## Output
![306614495-bacea400-bf86-4581-a6f0-bb475402b5f6](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/3b475d59-b055-4269-93d0-bb169c7d9798)
### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg')
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
## Output
![306614776-16b1ebea-a3c5-4cb6-b4f3-bba4b862783f](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/11865f25-c9d0-4eda-bd60-74fc4b583f80)

### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output
![306615182-e3a2691c-3bde-4617-8735-f15a23a1c24a](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/09c5749f-1510-4712-a9ab-0aa9cb6228df)

### ix) Split and merge RGB Image
```
<br>
import cv2
img = cv2.imread('pristine-reflective-lake-show-image-260nw-2305485315.jpg',1)
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
<br>
```
## Output
![306615503-c16e3cb5-278c-47c7-b3e0-e58890f25b71](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/695fe3e0-9457-4f8c-8068-48b37e64c734)

### x) Split and merge HSV Image
```
<br>
import cv2
img = cv2.imread("pristine-reflective-lake-show-image-260nw-2305485315.jpg",1)
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
<br>
```
### Output
![306615616-75cb96db-1d7e-4cb1-ae97-f484e58b0c88](https://github.com/Jeevithha/COLOR_CONVERSIONS_OF-IMAGE/assets/123623197/7ae97408-f2fa-4e84-8105-7757181a2192)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.

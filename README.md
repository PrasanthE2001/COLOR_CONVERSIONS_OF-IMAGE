# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
1.  Draw a line from the top-left to the bottom-right of the image.

2.	Draw a circle at the center of the image.

3.	Draw a rectangle around a specific region of interest in the image.

4.	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.	Convert the image from RGB to HSV and display it.
2.	Convert the image from RGB to GRAY and display it.
3.	Convert the image from RGB to YCrCb and display it.
4.	Convert the HSV image back to RGB and display it.

### Step4:
1.	Access and print the value of the pixel at coordinates (100, 100).
2.	Modify the color of the pixel at (200, 200) to white.

### Step5:
Resize the original image to half its size and display it.
### Step6:
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.	Flip the original image horizontally and display it.
2.	Flip the original image vertically and display it.

### Step8:
Save the final modified image to your local directory.


## Program:
### Developed By: E Prasanth
### Register Number: 212221233002


## Output:

### 1. Read and display the image
i.Load an image from your local directory and display it.
```
img=cv2.imread("gojo.jpeg")
cv2.imshow("display", img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![WhatsApp Image 2024-09-28 at 15 48 01](https://github.com/user-attachments/assets/076960bb-2b3b-4ddf-8305-23681688a5d2)



### Draw Shapes and Add Text
(1) Draw a line from the top-left to the bottom-right of the image.
```
img=cv2.imread("gojo.jpeg")
line=cv2.line(img,(0,0),(736,414),(0,0,255),10)
plt.imshow(line)
plt.axis('off')
plt.show()
```
![WhatsApp Image 2024-09-28 at 15 48 27](https://github.com/user-attachments/assets/5d8fec68-bd66-4e92-b89d-2381498d408d)



2. Draw a circle at the center of the image.
```
img=cv2.imread("gojo.jpeg")
circle=cv2.circle(img,(400,200),(150),(255,0,0),10)
plt.imshow(circle)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/3a034df9-638e-473d-968b-f02c9e08663e)



3.Draw a rectangle around a specific region of interest in the image.
```
image = cv2.imread("gojo.jpeg")
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
l = (200, 100) 
b = (550, 300)  
rectangle = cv2.rectangle(image_rgb, l, b, (255, 0, 0), 5)
plt.imshow(rectangle)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/15891160-441e-4a12-b699-b99ad659b8cb)




4.Add the text "OpenCV Drawing" at the top-left corner of the image.
```
iimport cv2
import matplotlib.pyplot as plt
image = cv2.imread("gojo.jpeg")
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image_rgb, 'OpenCV Drawing', (50, 50), font, 1, (255, 0, 0), 2)
plt.imshow(image_rgb)
plt.axis('off')
plt.show()
```
![image](https://github.com/user-attachments/assets/1bd83165-32b3-435f-9c12-b9bbe1ed7244)



### iii)Image Color Conversion
(i)Convert the image from RGB to HSV and display it
```
import cv2
image = cv2.imread('gojo.jpeg',1)
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/940f35af-1b00-41d5-becd-c44dfed04a7d)



(2) Convert the image from RGB to GRAY and display it.

```
import cv2
image = cv2.imread('gojo.jpeg',1)
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/81d97fc3-42bb-4b8e-b59e-a74b65abcf44)




(3) Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('gojo.jpeg',1)
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/d311fd68-0c52-4502-addf-b54d901f3ab4)



(4) Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('gojo.jpeg',1)
image = cv2.resize(image,(300,200))
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/990a7cff-728d-498e-9799-d6c73d7b508f)



### iv)Access and Manipulate Image Pixels
(1) Access and print the value of the pixel at coordinates (100, 100)
```
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
![image](https://github.com/user-attachments/assets/e3e07855-01fb-427b-af27-429b17fb9fe3)



(2) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('gojo.jpeg',1)
image = cv2.resize(image,(400,300))
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/b231f746-4f46-4c16-8a07-0b8d9c43dbdf)



### v)Image Resizing:
Resize the original image to half its size and display it.
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (350,200))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/34c686bc-169b-4dc6-9c17-bbd21076d9ca)



### vi)Image Cropping
Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
```
import cv2
image = cv2.imread('gojo.jpeg',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/d87c519f-a436-40c6-aa06-be1c4bd7c95f)


### vii)Image Flipping:
(1) Flip the original image horizontally and display it.
```
import cv2
image = cv2.imread("gojo.jpeg")
image= cv2.resize(image, (400,300))
res=cv2.rotate(image,cv2.ROTATE_180)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/91ffa498-ff9d-4862-b43c-a6431fb75c3d)



(2) Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("gojo.jpeg")
image= cv2.resize(image, (400,400))
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/bf00e551-1c35-445b-aeb0-b2d1154dd082)



### viii)Write and Save the Modified Image
Save the final modified image to your local directory.
```
import cv2
img = cv2.imread("gojo.jpg")
cv2.imwrite('apple.jpg',img)
```
![image](https://github.com/user-attachments/assets/34bbd9fa-bb9a-416b-a3c7-e4c462c34209)



## Result:

Thus the images are read, displayed, and written ,and color conversion was performed successfully using the python program.

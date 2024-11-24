# COLOR_CONVERSIONS_OF-IMAGE->
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

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
1.Load an image from your local directory and display it.
### Step2:
1.Draw a line from the top-left to the bottom-right of the image.

2.Draw a circle at the center of the image.

3.Draw a rectangle around a specific region of interest in the image.

4.Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
1.Convert the image from RGB to HSV and display it.

2.Convert the image from RGB to GRAY and display it.

3.Convert the image from RGB to YCrCb and display it.

4.Convert the HSV image back to RGB and display it.

### Step4:
1.Access and print the value of the pixel at coordinates (100, 100).

2.Modify the color of the pixel at (200, 200) to white.

### Step5:
1.Resize the original image to half its size and display it.
### Step6:
1.Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
1.Flip the original image horizontally and display it.

2.Flip the original image vertically and display it.

### Step8:
1.Save the final modified image to your local directory.


## Program:
### Developed By: AJAY ASWIN M
### Register Number: 212222240005

### i)Read and Display an Image
```
import cv2
import matplotlib.pyplot as plt
image=cv2.imread('kolhi.jpg')
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image)
plt.axis('off')
plt.show()
```
### Output
![{A3052B53-90D6-41A3-9C70-BB5EB98B1526}](https://github.com/user-attachments/assets/afd7f227-8afc-42e0-825b-c00325a5a69f)


### ii)Draw Shapes and Add Text
1) Draw a line from the top-left to the bottom-right of the image.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("kolhi.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
res = cv2.line(image, (0, 0), (440,591), (200, 100, 205), 10)
plt.imshow(res)
plt.axis('off')
plt.show()
```
### Output
![{18C2D785-C65E-4378-90A5-BA8DA3C4E297}](https://github.com/user-attachments/assets/06a8a81a-e9fa-4f3d-b4e8-05bbed6287aa)


(2) Draw a circle at the center of the image.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("kolhi.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
image = cv2.resize(image,(500,500))
res = cv2.circle(image,(250,250), 150, (255, 0, 0), 10)
plt.imshow(res)
plt.axis('off')
plt.show()
```
### Output
![{A78A5DA2-EF90-434C-A3E6-4AEA0E4C7A78}](https://github.com/user-attachments/assets/44205b68-7045-43cf-8190-40cf588679cf)


(3) Draw a rectangle around a specific region of interest in the image.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("kolhi.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
res = cv2.rectangle(image, (440-20,591-20), (0+10,0+10),(200,0, 0), 10)
plt.imshow(res)
plt.axis('off')
plt.show()
```
### Output
![{D22F27A5-EF1B-463D-887E-529586CAC280}](https://github.com/user-attachments/assets/19780a37-c4cb-4396-b3ae-1660f34f298b)


(4) Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("kolhi.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_SIMPLEX
res = cv2.putText(image,"VIRAT", (5,150), font,1.5, (0, 0, 0),5)
plt.imshow(res)
plt.axis('off')
plt.show()
```
### Output
![{FCB555D5-686D-49BA-8876-2480CFED752D}](https://github.com/user-attachments/assets/54b2915e-5aed-4600-9e14-55c6cf999a4d)


### iii)Image Color Conversion
1) Convert the image from RGB to HSV and display it
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("kolhi.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
hsv2 = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
plt.imshow(hsv2)
plt.axis('off')
plt.show()
```
### Output
![{D89B1E41-CC5D-499B-B3C6-B56A8847B8C4}](https://github.com/user-attachments/assets/dd1a0063-28c1-45c6-85ac-db69eed98010)


(2) Convert the image from RGB to GRAY and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("kolhi.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
gray2 = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
plt.imshow(gray2)
plt.axis('off')
plt.show()
```
### Output
![{0260EFCD-0D3C-4F8E-BA80-6B82DB93FA11}](https://github.com/user-attachments/assets/49df5e27-2d78-4403-96c0-9f73cc87f087)


3) Convert the image from RGB to YCrCb and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("kolhi.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
YCrCb1 = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
plt.imshow(YCrCb1)
plt.axis('off')
plt.show()
```
### Output
![{BC9D5546-7C5A-4301-BA21-E14D0E72760C}](https://github.com/user-attachments/assets/8262a58a-2b01-4bb4-be79-1daa7abe876f)


(4) Convert the HSV image back to RGB and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("kolhi.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
BGR = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
plt.imshow(BGR)
plt.axis('off')
plt.show()
```
### Output
![{F03536E2-7E38-4CA3-8751-E3306EDD584A}](https://github.com/user-attachments/assets/86859770-d6dc-4a00-9d63-9d06e847824a)


### iv)Access and Manipulate Image Pixels
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("kolhi.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
image[199, 199] = [255, 255, 255]
plt.imshow(image)
plt.axis('off')
plt.show()
```
### Output
![{704F2D4F-1C0D-47D7-9833-F154A47B6747}](https://github.com/user-attachments/assets/df789033-02cb-4ea9-bf94-7bd7633dbca2)

### v)Image Resizing
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("kolhi.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
resized_img = cv2.resize(image, (900, 1000))
plt.imshow(resized_img)
plt.axis('off')
plt.show()
```
### Output
![{2B889DCA-C081-4644-B9E2-7C93267EA788}](https://github.com/user-attachments/assets/3e85bcc6-a56c-4ee8-8287-ccd3d02c8675)


### vi)Image Cropping
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("kolhi.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
roi = image[50:50 + 425, 50:50 + 425]
plt.imshow(roi)
plt.axis('off')
plt.show()
```
### Output
![{6F77A881-46DB-46EE-9CFE-3616E06CFE31}](https://github.com/user-attachments/assets/3562010e-a470-4ffa-9ab4-256784f7e32f)


### vii)Image Flipping
(1) Flip the original image horizontally and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("kolhi.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
res=cv2.rotate(image,cv2.ROTATE_180)
plt.imshow(res)
plt.axis('off')
plt.show()
```
### Output
![{089DDA9E-C5C0-4F4F-836F-9065B5AF0184}](https://github.com/user-attachments/assets/8aa5b934-a820-4217-9f0b-043967b2624f)


(2) Flip the original image vertically and display it.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("kolhi.jpg")
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
image=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
plt.imshow(image)
plt.axis('off')
plt.show()
```
### Output
![{F9076D27-CEFF-4107-A55D-F995B9573222}](https://github.com/user-attachments/assets/bdbfca83-3cd1-4f3f-afdc-d3fa26ef1e64)


### viii)Write and Save the Modified Image
```
import cv2
img = cv2.imread("kolhi.jpg")
cv2.imwrite('virat_kolhi.jpg',img)
```
### Output
![{C7FAEF53-9F07-4737-9AC4-C8494EAA79B5}](https://github.com/user-attachments/assets/5762e5b0-1163-40ad-8ff3-1b17a9297ee8)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.








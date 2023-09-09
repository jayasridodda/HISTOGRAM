
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and any one channel of the color image.

### Step3:
Display the histograms.

### Step4:
Equalize the color image.

### Step5:
Display the equalized grayscale image.

## Program:
```
# Developed By: JAYASRI DODDA
# Register Number:212222240028
```
```
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('ex4.png')
plt.imshow(Gray_image)
plt.show()
Color_image=cv2.imread('ex4c.jpeg')
plt.imshow(Color_image)
plt.show()

# Write your code to find the histogram of gray scale image and color image channels.

hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("gray_scale value")
plt.ylabel("pixel count")
plt.stem(hist)
plt.show()

# Display the histogram of gray scale image and any one channel histogram from color image

hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("color_scale value")
plt.ylabel("pixel count")
plt.stem(hist1)
plt.show()

# Write the code to perform histogram equalization of the image. 

equ=cv2.equalizeHist(cv2.imread('ex4.jpeg',0))
equ=cv2.cvtColor(equ,cv2.COLOR_BGR2RGB)
plt.title("Equalised Image")
plt.axis("off")
plt.imshow(equ)
plt.show()

```
## Output:
### Input Grayscale Image and Color Image
![Screenshot from 2023-09-09 15-40-25](https://github.com/jayasridodda/HISTOGRAM/assets/123259278/a8e0054b-7df8-4f00-abbb-c067f8889003)

### Histogram of Grayscale Image and any channel of Color Image
![Screenshot from 2023-09-09 15-42-37](https://github.com/jayasridodda/HISTOGRAM/assets/123259278/ac53333d-a1f3-4863-bd6a-3cf63dbea0a4)
![Screenshot from 2023-09-09 15-42-45](https://github.com/jayasridodda/HISTOGRAM/assets/123259278/50353ec6-1803-4a4d-968d-3c4594ec3e9f)

## Histogram Equalization of Grayscale Image
![Screenshot from 2023-09-09 15-44-04](https://github.com/jayasridodda/HISTOGRAM/assets/123259278/9eaba6a3-5617-421f-b300-c5d3ea4a7de4)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.

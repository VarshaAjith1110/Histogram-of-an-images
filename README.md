# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: Varsha Ajith
# Register Number: 212221230118

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("fl2.jpg")
color_image = cv2.imread("fl.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Display the histogram of gray scale image and any one channel histogram from color image
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("fl2.jpg")
color_image = cv2.imread("fl.jpg")
gray_hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()

# Write the code to perform histogram equalization of the image. 
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("fl2.jpg",0)
cv2.imshow("Gray Image",gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows



```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/VarshaAjith1110/Histogram-of-an-images/assets/94222288/5fa788f0-f9d2-4cab-a9e2-3987cb3f7c5c)


### Histogram of Grayscale Image and any channel of Color Image

![image](https://github.com/VarshaAjith1110/Histogram-of-an-images/assets/94222288/b7e9e2ba-38a0-483e-8dff-1a40a536579a)
![image](https://github.com/VarshaAjith1110/Histogram-of-an-images/assets/94222288/20275cd9-82f0-4f2d-b500-721171473754)


### Histogram Equalization of Grayscale Image.

![image](https://github.com/VarshaAjith1110/Histogram-of-an-images/assets/94222288/ae2dae77-5fd4-458c-b101-281c8d324405)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.

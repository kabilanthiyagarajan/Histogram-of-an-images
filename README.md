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
Developed By: JEGADEESH S
Register Number: 212222230055
```

### Input Grayscale Image and Color Image : 

```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("flower.jpg")
color_image = cv2.imread("sphere.jpg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Histogram of Grayscale Image and any channel of Color Image :

```python
import numpy as np
import cv2
Gray_image = cv2.imread("flower.jpg")
Color_image = cv2.imread("sphere.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```

### Histogram Equalization of Grayscale Image :
```python
import cv2
gray_image = cv2.imread("flower.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### Input Grayscale Image and Color Image
![WhatsApp Image 2024-03-16 at 09 22 06_27b31357](https://github.com/Nagul71/Histogram-of-an-images/assets/118661118/857ab205-3e14-4e96-b434-347656739b0b)
![WhatsApp Image 2024-03-16 at 09 22 06_7c7540a1](https://github.com/Nagul71/Histogram-of-an-images/assets/118661118/9b674a19-6854-4046-9b21-bc60e6da229d)


### Histogram of Grayscale Image and any channel of Color Image

#### Gray Scale -

![image](https://github.com/Nagul71/Histogram-of-an-images/assets/118661118/441834f1-fee0-4fc3-8a0f-d0d1027e8675)
![image](https://github.com/Nagul71/Histogram-of-an-images/assets/118661118/ae043712-4878-446e-adf1-543d29811c55)



#### Color Image -

![image](https://github.com/Nagul71/Histogram-of-an-images/assets/118661118/e6eb2750-21ff-44d6-a189-63567fa56b16)
![image](https://github.com/Nagul71/Histogram-of-an-images/assets/118661118/4ce65170-b561-4bae-a3b3-3f8ba82bd633)




### Histogram Equalization of Grayscale Image :

![WhatsApp Image 2024-03-16 at 09 21 49_4e0db3b2](https://github.com/Nagul71/Histogram-of-an-images/assets/118661118/087a53e2-d1fc-4d75-838f-aee6af150e5c)


![WhatsApp Image 2024-03-16 at 09 21 49_56aa6cb4](https://github.com/Nagul71/Histogram-of-an-images/assets/118661118/c056c740-7dc3-4d2a-b5bb-cdc37d556f56)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.

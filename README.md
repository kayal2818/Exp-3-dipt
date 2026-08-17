# Exp-3-dipt
## Histogram Equalization Using OpenCV (Grayscale & Color Images)
## Aim
To write a Python program using OpenCV to perform histogram equalization on both grayscale and color images to enhance image contrast and brightness.

The program performs the following operations:

Read and display a grayscale image
Plot histogram of the grayscale image
Apply histogram equalization on grayscale image
Read and display a color image
Plot histogram of B, G, R channels
Convert image to HSV color space
Apply histogram equalization on the Value (V) channel
Convert the enhanced image back to BGR format
Display original and enhanced images with histograms
## Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib
## Algorithm
## Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

## Step 2:
Read the image parrot.jpg in grayscale format.

## Step 3:
Display the grayscale image and plot its histogram.

## Step 4:
Apply histogram equalization using cv2.equalizeHist() to enhance contrast.

## Step 5:
Display original grayscale image, its histogram, enhanced image, and its histogram using a 2 × 2 grid.

## Step 6:
Read the same image in color format.

## Step 7:
Split the image into B, G, R channels and plot their histograms.

## Step 8:
Convert the image from BGR to HSV color space.

## Step 9:
Apply histogram equalization on the V (Value) channel.

## Step 10:
Merge the channels and convert the image back to BGR format.

## Step 11:
Display original color image, histogram, enhanced image, and enhanced histogram using a 2 × 2 grid.

## Program
## Developed By:
## Name: kayalvizhi.v

## Register No: 212225040182
## Step 1:
```
import cv2
from matplotlib import pyplot as plt
```
## Step 2:
```
# Load the color image
image = cv2.imread('parrot.jpg')
```
## Step 3:
```
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
## Step 4:
```
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
## Step 5
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
```
## Step 6:
```
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
## Step 7:
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
```
## Step 8:
```
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
## Step 9:
```
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
```
## Step 10:
```
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
## Output
## Grayscale Histogram Equalization

* Original grayscale image is displayed
  
  <img width="735" height="580" alt="image" src="https://github.com/user-attachments/assets/cd40538a-d257-4692-88e3-a09f6e75c7cb" />

* Histogram of original grayscale image is plotted

  <img width="750" height="615" alt="image" src="https://github.com/user-attachments/assets/f60bd783-419a-4459-b364-561b62922f65" />

* Enhanced image after histogram equalization is displayed

  <img width="767" height="581" alt="image" src="https://github.com/user-attachments/assets/11e3bf92-b90f-42b9-b780-1ddd93becec0" />

* Histogram of enhanced grayscale image shows improved contrast

  <img width="740" height="615" alt="image" src="https://github.com/user-attachments/assets/04808a42-3c23-4b66-92a5-cf0e5e895053" />

## Result

   Thus, histogram equalization is successfully performed on both grayscale and color images using OpenCV. The contrast and brightness of the images are significantly improved, enhancing visual quality and feature visibility.




  





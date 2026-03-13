# EXP-8-THRESHOLDING
## Developed By: HARISHBALA J
## Reg No.: 212224223002
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages

### Step2:
Read the Image and convert to grayscale
### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.
## Program
#### NAME : HARISHBALA J ####

#### REG NO : 212224223002 ####
```
import cv2
import matplotlib.pyplot as plt

# Read the Image and convert to grayscale

image=cv2.imread('hasna.jpeg')
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)

# Original image

plt.subplot(2,2,1)
plt.imshow(cv2.cvtColor(image,cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

# Use Global thresholding to segment the image

_,global_thresholded = cv2.threshold(gray_img, 127, 255, cv2.THRESH_BINARY)

# Use Adaptive thresholding to segment the image

adaptive_thresholded = cv2.adaptiveThreshold(gray_img, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)

# Use Otsu's method to segment the image 

_,otsu_thresholded = cv2.threshold(gray_img, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

# Global Thresholding
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')

# Adaptive Thresholding
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')

# Otsu's Method
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

# Show the plot
plt.tight_layout()
plt.show()
```
## Output
<img width="411" height="295" alt="Screenshot 2026-03-13 093342" src="https://github.com/user-attachments/assets/17ff8851-f456-474f-a015-1db2a38f0852" />
<img width="426" height="289" alt="Screenshot 2026-03-13 093335" src="https://github.com/user-attachments/assets/75a615f1-1672-490d-8d61-7b7ace18a262" />
<img width="377" height="240" alt="Screenshot 2026-03-13 093328" src="https://github.com/user-attachments/assets/42b65344-eceb-4e3e-9eaa-4cc1cd57f1fe" />
<img width="437" height="286" alt="Screenshot 2026-03-13 093347" src="https://github.com/user-attachments/assets/3b159364-0745-4030-bb8e-33af9a746cad" />





## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.

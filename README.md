# EX. NO: 03
# Histogram Equalization Using OpenCV (Grayscale & Color Images)
### Developed By:
## Name: Nara Guna Susmitha
### Register No:212224230176

## Aim

To write a Python program using OpenCV to perform histogram equalization on both grayscale and color images to enhance image contrast and brightness.

The program performs the following operations:

- Read and display a grayscale image  
- Plot histogram of the grayscale image  
- Apply histogram equalization on grayscale image  
- Read and display a color image  
- Plot histogram of B, G, R channels  
- Convert image to HSV color space  
- Apply histogram equalization on the Value (V) channel  
- Convert the enhanced image back to BGR format  
- Display original and enhanced images with histograms  

---

## Software Used

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (`cv2`)  
- NumPy  
- Matplotlib  

---

## Algorithm

### Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:
Read the image `parrot.jpg` in grayscale format.

### Step 3:
Display the grayscale image and plot its histogram.

### Step 4:
Apply histogram equalization using `cv2.equalizeHist()` to enhance contrast.

### Step 5:
Display original grayscale image, its histogram, enhanced image, and its histogram using a 2 × 2 grid.

### Step 6:
Read the same image in color format.

### Step 7:
Split the image into B, G, R channels and plot their histograms.

### Step 8:
Convert the image from BGR to HSV color space.

### Step 9:
Apply histogram equalization on the V (Value) channel.

### Step 10:
Merge the channels and convert the image back to BGR format.

### Step 11:
Display original color image, histogram, enhanced image, and enhanced histogram using a 2 × 2 grid.

---

## Program


```
import cv2
from matplotlib import pyplot as plt
image = cv2.imread('Qno. 1.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
    
##  Output:
<img width="417" height="458" alt="WhatsApp Image 2026-11-14 at 10 22 04 PM" src="https://github.com/user-attachments/assets/55ed577c-d23f-495e-a527-b7cf696e6af7" />
<img width="700" height="497" alt="WhatsApp Image 2026-11-14 at 10 22 30 PM" src="https://github.com/user-attachments/assets/25714c5c-1b9e-4583-9066-50a7815a2b42" />
<img width="395" height="467" alt="WhatsApp Image 2026-11-14 at 10 22 43 PM" src="https://github.com/user-attachments/assets/fca8e544-1ab0-4e22-a5f7-a97509a52ed0" />
<img width="692" height="477" alt="WhatsApp Image 2026-11-14 at 10 23 14 PM" src="https://github.com/user-attachments/assets/87149b84-1b74-4589-9458-1a9947f99db3" />


## Result

Thus, histogram equalization is successfully performed on both grayscale and color images using OpenCV. The contrast and brightness of the images are significantly improved, enhancing visual quality and feature visibility.

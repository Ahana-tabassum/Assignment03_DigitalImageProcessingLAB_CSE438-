# 🎨 Digital Image Processing Lab

## 📌 Lab Information
- **Submitted by:** Maheru Tabassum Ohana  
- **ID:** 2125051015  
- **Section:** 8A  
- **Batch:** 50  
- **Course Code:** CSE 438  
- **Course Title:** Digital Image Processing Lab  
- **University:** University of Information Technology and Sciences (UITS)  
- **Instructor:** Audity Ghosh  
- **Date:** 04 March, 2025  

---

## 🎯 **Objective**
Create two **400x400** images with a black background:
1. **First Image:** A green rectangle at the center.
2. **Second Image:** A magenta circle at the center.

---

## 🛠️ **Implementation Using OpenCV**
### 📌 **Required Libraries**
```python
from google.colab import files
import cv2
import matplotlib.pyplot as plt
import numpy as np
from google.colab.patches import cv2_imshow
```

### 📌 **Creating the Images**
#### ✅ **Image 1: Green Rectangle**
```python
image1 = np.ones((400, 400, 3), dtype=np.uint8) * 255
cv2.rectangle(image1, (100, 100), (300, 300), (0, 255, 0), -1)
cv2_imshow(image1)
```

#### ✅ **Image 2: Magenta Circle**
```python
image2 = np.ones((400, 400, 3), dtype=np.uint8) * 255
cv2.circle(image2, (200, 200), 100, (100, 0, 255), -1)
cv2_imshow(image2)
```

---

## 🎨 **Bitwise and Image Processing Operations**
Perform the following operations using **OpenCV** and display the results:

### ✅ **1️⃣ Bitwise AND (`cv2.bitwise_and`)**
Shows the overlapping region of the two images.
```python
bitwise_and = cv2.bitwise_and(image1, image2)
cv2_imshow(bitwise_and)
```

### ✅ **2️⃣ Bitwise OR (`cv2.bitwise_or`)**
Combines both shapes while retaining their colors.
```python
bitwise_or = cv2.bitwise_or(image1, image2)
cv2_imshow(bitwise_or)
```

### ✅ **3️⃣ Bitwise XOR (`cv2.bitwise_xor`)**
Retains only the non-overlapping parts of both images.
```python
bitwise_xor = cv2.bitwise_xor(image1, image2)
cv2_imshow(bitwise_xor)
```

### ✅ **4️⃣ Bitwise NOT (`cv2.bitwise_not`)**
Inverts the colors of each shape separately.
```python
bitwise_not_image1 = cv2.bitwise_not(image1)
bitwise_not_image2 = cv2.bitwise_not(image2)
cv2_imshow(bitwise_not_image1)
cv2_imshow(bitwise_not_image2)
```

### ✅ **5️⃣ Element-wise Multiplication (`cv2.multiply`)**
Observe the effect on overlapping areas.
```python
Multiplication = cv2.multiply(image1, image2)
cv2_imshow(Multiplication)
```

### ✅ **6️⃣ Alpha Blending (`cv2.addWeighted`)**
Blend both images with transparency effects.
```python
alpha = 0.5
Blending  = cv2.addWeighted(image1, alpha, image2, 1 - alpha, 0)
cv2_imshow(Blending)
```

### ✅ **7️⃣ Image Subtraction (`cv2.subtract`)**
Highlights the differences between the two images.
```python
subtraction = cv2.subtract(image1, image2)
cv2_imshow(subtraction)
```

---

## 🔧 **Installation & Usage**
### 👅 **Installation**
To run this code, install OpenCV and NumPy using:
```bash
pip install opencv-python numpy
```

### ▶️ **Execution**
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/digital-image-processing-lab.git
   cd digital-image-processing-lab
   ```
2. Open the Jupyter Notebook:
   ```bash
   jupyter notebook Digital_Image_Processing_Lab.ipynb
   ```
3. Run the cells to see the results.

---

## 📸 **Sample Output**
(Insert screenshots of images generated.)

---

## 📝 **Conclusion**
This lab focused on **bitwise operations** in OpenCV and how they can be used in **image processing**. Understanding these techniques is essential for computer vision applications.

---

## 📚 **References**
- OpenCV Documentation: [https://docs.opencv.org](https://docs.opencv.org)  
- Python OpenCV Tutorials  

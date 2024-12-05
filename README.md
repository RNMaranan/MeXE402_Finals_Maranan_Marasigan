<h1 align="center">
    <a href="https://git.io/typing-svg">
        <img src="https://readme-typing-svg.herokuapp.com?font=Press+Start+2P&pause=500&width=950&color=0268c0&lines=MExEE+402+-+MExE+Elective+2+Final+Requirement" alt="Typing SVG" />
    </a>
</h1>

![Black and White Modern Artificial Intelligence Presentation (1)](https://github.com/user-attachments/assets/f617b1d5-03a4-48f9-8463-75e44ddd1b91)

###

![i](https://github.com/user-attachments/assets/b57590f1-2053-4cbb-9425-8b89fdb31f0c)

# 📍 INTRODUCTION

## 🤖 What is a Deepfake?  
- Deepfakes are AI-generated media where a person’s likeness is synthesized or manipulated to create realistic but fake images or videos. They often involve replacing a person's face or altering expressions convincingly using deep learning algorithms.  

## 🤖 Problem with Deepfakes  
- Deepfakes pose serious concerns, including misinformation, privacy invasion, and cybercrime. Detecting and distinguishing deepfakes from real images has become a critical challenge in computer vision and digital forensics.  

##  🤖What is Morphological Erosion?  
- Morphological erosion is an image processing technique that reduces image elements based on a structuring element. It helps highlight fine details or diminish certain features, particularly by eroding boundaries or noise in binary or grayscale images.  

## 🤖 How Can Morphological Erosion Detect Deepfakes?  
- Morphological erosion can expose inconsistencies in facial features, edges, or textures that are often introduced during the deepfake synthesis process. Real faces typically have uniform patterns, while deepfakes may reveal irregularities under this method.  

## 🤖 Significance in Computer Vision  
- The rise of deepfake technology has pushed computer vision to develop robust detection mechanisms. Combining traditional image processing like morphological erosion with machine learning provides a new layer of analysis, improving the accuracy of distinguishing manipulated images from authentic ones.

![i (1)](https://github.com/user-attachments/assets/d81e6edb-a197-433e-a35b-5e2cc714cc50)

# 📍 ABSTRACT
```python
import cv2
from google.colab.patches import cv2_imshow
import numpy as np

image = cv2.imread("images/DeepReal.png")
# cv2_imshow(image)

gray = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
canny_image = cv2.Canny(gray,150, 200)
# cv2_imshow(canny_image)

# Erosion and Dilation

kernel = np.ones((1,1), np.uint8)
dilate_image = cv2.dilate(canny_image, kernel, iterations=1)
kernel1 = np.ones((3,3), np.uint8)
dilate_image1 = cv2.dilate(canny_image, kernel1, iterations=1)
kernel2 = np.ones((5,5), np.uint8)
dilate_image2 = cv2.dilate(canny_image, kernel2, iterations=1)
kernel3 = np.ones((7,7), np.uint8)
dilate_image3 = cv2.dilate(canny_image, kernel3, iterations=1)
kernel4 = np.ones((9,9), np.uint8)
dilate_image4 = cv2.dilate(canny_image, kernel4, iterations=1)

#Erosion
kernel = np.ones((1,1), np.uint8)
erode_image = cv2.erode(dilate_image,kernel, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image1,kernel, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image2,kernel, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image3,kernel, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image4,kernel, iterations=1)
cv2_imshow(erode_image)

#kernel1 = np.ones((3,3), np.uint8)
erode_image = cv2.erode(dilate_image,kernel1, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image1,kernel1, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image2,kernel1, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image3,kernel1, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image4,kernel1, iterations=1)
cv2_imshow(erode_image)

#kernel2 = np.ones((5,5), np.uint8)
erode_image = cv2.erode(dilate_image,kernel2, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image1,kernel2, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image2,kernel2, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image3,kernel2, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image4,kernel2, iterations=1)
cv2_imshow(erode_image)

#kernel3 = np.ones((7,7), np.uint8)
erode_image = cv2.erode(dilate_image,kernel3, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image1,kernel3, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image2,kernel3, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image3,kernel3, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image4,kernel3, iterations=1)
cv2_imshow(erode_image)

#kernel4 = np.ones((9,9), np.uint8)
erode_image = cv2.erode(dilate_image,kernel4, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image1,kernel4, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image2,kernel4, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image3,kernel4, iterations=1)
cv2_imshow(erode_image)
erode_image = cv2.erode(dilate_image4,kernel4, iterations=1)
cv2_imshow(erode_image)
```

## 🤖 Objectives
- The project aims to utilize **morphological erosion** to differentiate between deepfake and real face images. The primary focus is to analyze and identify variations in texture and edges and assess how image features shrink under varying kernel sizes.  

## 🤖 Approach  
1. Implement **morphological erosion** on datasets containing deepfake and real face images.  
2. Examine the extracted features, specifically focusing on texture patterns and edge consistency.  
3. Experiment with different **kernel sizes** to evaluate their impact on the erosion process and the visual differences between the two image types.  

## 🤖 Expected Results  
The project expects to highlight unique patterns or inconsistencies in deepfake images that become prominent after erosion.  
- **Real face images**: Anticipated to exhibit more uniform and consistent shrinkage.  
- **Deepfake images**: Expected to reveal irregularities in texture and edges, providing a basis for differentiation.  

This approach could contribute to the development of a practical method for detecting deepfakes in **computer vision** applications.  


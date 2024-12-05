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

# 📍 METHODOLOGY

## 🤖 Dataset Collection and Preprocessing:
   1. Collect a dataset containing both deepfake and real face images.
   2. Ensure equal representation of deepfake and real images to avoid dataset bias.
   3. Resize all images to a uniform dimension for consistent analysis.

## 🤖 Morphological Operation Implementation:
   1. Apply **erosion** and **dilation** operations on the images.
   2. Use varying kernel sizes **(e.g., 1x1 3x3, 5x5, 7x7, 9x9)** for both erosion and dilation to observe feature variations.
   3. Generate processed versions of each image for every combination of kernel sizes **(5 for erosion × 5 for dilation = 25 combinations)**.

## 🤖 Feature Extraction:
   1. Analyze the morphological effects (texture, edge variations, etc.) introduced by erosion and dilation for each kernel size.
   2. Quantify the changes in image features (e.g., edge intensities, texture uniformity) using image-processing metrics like:
   3. Edge detection (e.g., Sobel or Canny filters).
   4. Texture analysis (e.g., Gray Level Co-occurrence Matrix, Local Binary Patterns).
   5. Pixel intensity histograms.

## 🤖 Analysis of Feature Shrinkage:
   1. Compare how image details shrink or expand under each kernel size.
   2. Evaluate the sensitivity of deepfake images versus real images to morphological operations by measuring:
   3. Loss of texture/edge details in real images.
   4. Over-smoothness or artifact appearance in deepfake images.
## 🤖 Visualization and Reporting:
    1. Create visual comparisons of morphological effects (before and after erosion/dilation) for both real and deepfake images.
    2. Summarize findings and key observations in a detailed report.
    3. Highlight the kernel size that provides the most distinct differentiation.
## 🤖 Conclusion and Recommendations:
    1. Conclude whether morphological erosion and dilation effectively differentiate deepfake and real images.
    2. Suggest future improvements, such as incorporating additional image-processing techniques or exploring other morphological operations.



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


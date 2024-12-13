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

![i (2)](https://github.com/user-attachments/assets/47f3e9e1-1c5b-4680-85d5-d458220b145f)

# 📍 PROJECT METHODS

## 🤖 Step 1. Dataset Collection and Preprocessing:
- Collect a dataset containing both deepfake and real face images.
- Ensure equal representation of deepfake and real images to avoid dataset bias.
- Resize all images to a uniform dimension for consistent analysis.

## 🤖 Step 2. Morphological Operation Implementation:
- Apply **erosion** and **dilation** operations on the images.
- Use varying kernel sizes **(e.g., 1x1, 3x3, 5x5, 7x7, 9x9)** for both erosion and dilation to observe feature variations.
- Generate processed versions of each image for every combination of kernel sizes **(5 for erosion × 5 for dilation = 25 combinations)** and additional **(5 for erosion with canny edge detection)**.
- Combine Canny edge detection with the morphological operations.
- Apply the Canny edge detection for erosion to further analyze edge shrinkage or expansion.

## 🤖 Step 3. Feature Extraction:
- Analyze the morphological effects **(texture, edge variations, etc.)** introduced by erosion and dilation for each kernel size.
- Quantify the changes in image features (e.g., edge intensities, texture uniformity) using image-processing metrics like:  
  - **Edge detection** (e.g., Sobel or Canny filters).  
  - **Texture analysis** (e.g., Gray Level Co-occurrence Matrix, Local Binary Patterns).  
  - **Pixel intensity histograms**.  


## 🤖 Step 4. Analysis of Feature Shrinkage:
- Compare how image details shrink or expand under each kernel size.  
- Evaluate the sensitivity of deepfake images versus real images to morphological operations by measuring:  
  - **Loss of texture/edge details** in real images.  
  - **Over-smoothness or artifact appearance** in deepfake images.  

## 🤖 Step 5. Visualization and Reporting:
- Create visual comparisons of morphological effects (before and after erosion/dilation) for both real and deepfake images.
- Summarize findings and key observations in a detailed report.
- Highlight the kernel size that provides the most distinct differentiation.

![i (3)](https://github.com/user-attachments/assets/fdc04aba-2046-485f-a42e-7863f7610a17)

## 📍 CONCLUSION

## 🤖 Findings

## <p align="center">Observations on Morphological Erosion: Deepfake vs. Real Face</p>

### <p align="center">Reference Picture</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/6aa7477f-b2df-4099-837a-bfe02608ca7e" alt="Your Image Description" width="80%">
</p>
<p align="center">
  <b>Left</b>: Deepfake &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <b>Right</b>: Real Face
</p>




### <p align="center">Side-by-Side Comparison</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/c72d45e7-23fa-49a6-9b95-b07305c8ea42" alt="Deepfake vs Real Face Eroded" width="80%">
</p>
<p align="center">
  <b>Left</b>: Deepfake (Eroded) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <b>Right</b>: Real Face (Eroded)
</p>


### <p align="center">Other Examples </p> 

<p align="center">
  <img src="https://github.com/user-attachments/assets/21b4a660-6e7a-4bcc-bc22-1927239077fd" alt="Image 1" width="500">
  <img src="https://github.com/user-attachments/assets/c92c5fbe-9308-4ce4-a376-04c70fa362d3" alt="Image 2" width="500">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/02a05d08-c95b-47f4-af18-5b24b38fddcb" alt="Deepfake (Eroded)" width="500">
  <img src="https://github.com/user-attachments/assets/6a5ff9a4-1cb0-4004-9832-6863cd425610" alt="Real Face (Eroded)" width="500">
</p>




Upon implementing **morphological erosion** on datasets containing deepfake and real face images, the following observations were noted:

### 1. **Line Consistency**
- **Deepfake**: Inconsistent and uneven lines, with noticeable breaks and faint areas such as beard edges and hair strands.  
- **Real Face**: Smooth and connected lines, maintaining structural integrity throughout the image.

### 2. **Level of Detail**
- **Deepfake**: Showed less detail, with fragmented or poorly defined features, such as facial hair and textures.  
- **Real Face**: Retained a higher level of detail, with fine lines and textures accurately represented.

### 3. **Edge Sharpness**
- **Deepfake**: Edges appeared less sharp, with blurry transitions and irregularities in regions that should have continuous lines.  
- **Real Face**: Displayed sharper and well-defined edges, highlighting the clarity of facial features.


### 4. **Structural Noise**
- **Deepfake**: Exhibited noise and artifacts, with unnecessary disruptions in regions that should have been uniform.  
- **Real Face**: Minimal noise, with clean and artifact-free lines.


## 🤖 Challenges

## <p align="center">Challenges in Classifying Deepfake and Real Images</p>

### 1. **Inconsistent Feature Visibility**:  
- Sometimes, even real images may not clearly show facial features due to lighting, angle, or image quality, making it harder to classify them accurately.

### 2. **Inconsistent Line Behavior**:  
- Lines and edges in both deepfake and real images may not always be consistent, especially in areas like facial contours or hair, making it difficult to distinguish between deepfake and real images.

### 3. **Variation in Sharpness**:  
- Sharpness can vary, making it challenging to distinguish between deepfake and real images.

### 4. **Noise and Artifacts**:  
- Both deepfake and real images can exhibit noise or artifacts, though they are more common and prominent in deepfake images, complicating classification.

### 5. **Quality of Image Details**:  
- In some cases, the quality of the image, such as pixelation or blurriness, may obscure key features, making it difficult to classify even real images accurately.

## 🤖 Outcome

## <p align="center">Outcome of Deepfake and Original Images Under Different Kernel Sizes</p>

![EROSION - Google Docs_page-0001](https://github.com/user-attachments/assets/8239254f-9042-4af4-b153-0e7079752fe3)

## <p align="center">Findings Table: Erosion and Dilation Effects</p>


| **Kernel Size** | **Dilation 1×1**                                       | **Dilation 3×3**                                   | **Dilation 5×5**                                   | **Dilation 7×7**                                     | **Dilation 9×9**                                     |
|-----------------|--------------------------------------------------------|----------------------------------------------------|----------------------------------------------------|------------------------------------------------------|------------------------------------------------------|
| **1×1 Erosion** | Fine details retained; sharp and clear edges.          | Edges thicken slightly, fine details remain visible.| Thicker outlines, prominent features emphasized, some details blur.| Noticeable thickening of edges; smaller details fade, bold outlines dominate.| Extreme edge thickening, bold structural lines dominate, finer details erased.|
| **3×3 Erosion** | Completely black, no visible lines.| Moderate edge thickness, fewer fine details.       | Thick edges dominate; smaller features are nearly absent. | Bold, dense outlines dominate; fine details completely removed. | Large, prominent structures persist, heavy abstraction of image. | 
| **5×5 Erosion** | Completely black, no visible lines.          | Slight edge restoration, but focus is on large-scale outlines. | Thick and bold outlines dominate the image.        | Minimal fine detail remains; heavily emphasized outlines. | Maximum simplification, large bold lines dominate. |
| **7×7 Erosion** | Completely black, no visible lines. | Bold, simplified edges reappear; noticeable detail loss. | Thick, blocky outlines dominate.                  | Edges lose structural complexity; bold, abstract appearance. | Maximum abstraction; only largest structural outlines persist. |
| **9×9 Erosion** | Completely black, no visible lines. | Slight edge recovery, minimal abstract lines visible. | Thick and prominent outlines emerge; finer textures are almost absent. | Highly simplified and bold lines; abstract representation. | Maximum abstraction and loss of complexity; only basic shapes and boldest edges remain. | 

## <p align="center">General Observations</p>

### Erosion Behavior:
- As the erosion kernel size increases, finer details are progressively removed, leaving only prominent edges and structures.

### Dilation Behavior:
- Larger dilation kernel sizes enhance the thickness of edges but blur finer details, especially when erosion is aggressive.

![i (4)](https://github.com/user-attachments/assets/04045c0a-f69c-4795-86d7-34e7671cb05a)

## 📍 ADDITIONAL MATERIAL

### Code on Google Colab

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
```python
kernel = np.ones((1,1), np.uint8)
erode_image1 = cv2.dilate(canny_image, kernel, iterations=1)
cv2_imshow(erode_image1)
kernel1 = np.ones((3,3), np.uint8)
erode_image2 = cv2.dilate(canny_image, kernel1, iterations=1)
cv2_imshow(erode_image2)
kernel2 = np.ones((5,5), np.uint8)
erode_image3 = cv2.dilate(canny_image, kernel2, iterations=1)
cv2_imshow(erode_image3)
kernel3 = np.ones((7,7), np.uint8)
erode_image4 = cv2.dilate(canny_image, kernel3, iterations=1)
cv2_imshow(erode_image4)
kernel4 = np.ones((9,9), np.uint8)
erode_image5 = cv2.dilate(canny_image, kernel4, iterations=1)
cv2_imshow(erode_image5)
```
### Google Docs Link for a Clearer Comparison of Kernel Sizes and an Additional Sample Image
Link: https://docs.google.com/document/d/1t6YCFVUJt_Ec93ruNB8spKElL8WSaT12T64t6KtkzpM/edit?usp=sharing

### Google Colab Links for Samples
Link 1:https://colab.research.google.com/drive/1au7TBegidm-HI0K3eyUpoB29igAo6D_s

### OpenCV Basics
Link: https://github.com/RNMaranan/OpenCV_Basics_MEXE-4101_Maranan_Marasigan

![i (5)](https://github.com/user-attachments/assets/87cfe895-6373-419c-9d6b-368163a06878)

## 📍 REFERENCES
https://www.youtube.com/watch?v=E3Lg4aZVCAU&t=1274s


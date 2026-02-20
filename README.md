# Medical Image Segmentation Projects  
## Classical Image Processing Techniques in Biomedical Analysis

---

# 📌 Overview

This repository contains three medical image segmentation projects implemented using classical image processing techniques.

The objective is to explore adaptive thresholding and watershed segmentation for solving real-world biomedical problems involving:

- Brain tumor segmentation
- Retinal vessel extraction
- Cell nuclei separation

All experiments are evaluated using quantitative metrics and visual comparisons.

---

# 🧠 Project 1: Brain MRI Tumor Segmentation  
## Otsu vs Sauvola Thresholding

### 🎯 Objective
Segment tumor regions in brain MRI images and compare:

- Global Thresholding (Otsu)
- Adaptive Thresholding (Sauvola)

### 📂 Dataset
Brain MRI Tumor Segmentation Dataset  
Kaggle Source  
https://www.kaggle.com/datasets/nikhilroxtomar/brain-tumor-segmentation/data

### ⚙️ Methods
- Otsu (Global threshold)
- Sauvola (Local adaptive threshold)

### 📊 Evaluation Metrics
- Dice Score  
- Jaccard Index  

### 🔎 Observations
- Otsu works well for high contrast tumors.
- Sauvola handles uneven intensity variations better.
- Adaptive thresholding produces smoother tumor boundaries.

### ✅ Conclusion
Sauvola outperforms Otsu in heterogeneous MRI images due to its local adaptation capability.

---

# 👁 Project 2: Retinal Vessel Extraction  
## Niblack vs Sauvola Thresholding

### 🎯 Objective
Extract thin retinal vessels from fundus images using local thresholding.

### 📂 Dataset
DRIVE Retinal Vessel Dataset  
https://www.kaggle.com/datasets/andrewmvd/drive-digital-retinal-images-for-vessel-extraction
Structure:
```
training/
    images/
    1st_manual/   (Ground Truth)
    mask/         (FOV Mask)
```

### ⚙️ Methods
- Niblack Thresholding
- Sauvola Thresholding

### 📊 Evaluation Metric
Sensitivity (Recall)

\[
Sensitivity = \frac{TP}{TP + FN}
\]

### 🔎 Observations
- Thin vessels require adaptive thresholding.
- Niblack produces more noise.
- Sauvola preserves fine vessel structures better.

### ✅ Conclusion
Sauvola achieves higher sensitivity and better thin vessel preservation.

---

# 🔬 Project 3: Cell Nuclei Separation  
## Watershed Segmentation

### 🎯 Objective
Separate touching nuclei using:

- Watershed without markers
- Marker-controlled Watershed

### 📂 Dataset
MoNuSeg (Multi-Organ Nuclei Segmentation)  
Source: Grand Challenge Platform  
https://monuseg.grand-challenge.org/Data/

Structure:
```
MoNuSeg/
    Tissue Images/
    Annotations/ (XML polygons)
```

### ⚙️ Methods
1. Basic Watershed (no marker control)
2. Marker-controlled Watershed with:
   - Morphological opening
   - Distance transform
   - Connected components

### 📊 Evaluation Metric
Dice Score

### 🔎 Observations
- Without markers → Over-segmentation.
- Marker-controlled watershed → Clean separation.
- Morphological preprocessing improves performance.

### ✅ Conclusion
Marker-controlled watershed significantly reduces over-segmentation and improves segmentation accuracy.

---

# 🛠 Technologies Used

- Python
- OpenCV
- NumPy
- Matplotlib
- Scikit-image
- XML parsing (ElementTree)

---

# 📈 Key Learnings

- Global thresholding struggles with intensity variation.
- Local adaptive thresholding improves segmentation of fine structures.
- Watershed segmentation requires marker control for stable results.
- Morphological operations enhance classical segmentation pipelines.
- Quantitative metrics are essential for meaningful evaluation.

---

# 🧪 Evaluation Metrics Used

- Dice Score
- Jaccard Index
- Sensitivity (Recall)

---

# 📌 Overall Conclusion

Classical image processing techniques remain powerful for medical image segmentation when carefully applied.

- Adaptive thresholding is superior for fine and low-contrast structures.
- Marker-controlled watershed is essential for separating touching objects.
- Proper preprocessing and evaluation are critical for robust performance.

---

# 👤 Author

Harsh Tripathi  
B.Tech — AI & Data Science  
IIIT Raichur  
Roll No: AD23B1021  

Course: Medical Image Processing  
Submission Date: __________

---

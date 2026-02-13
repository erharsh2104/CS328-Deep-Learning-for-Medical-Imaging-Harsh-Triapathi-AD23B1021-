# CS328-Deep-Learning-for-Medical-Imaging-Harsh-Triapathi-AD23B1021
# Brain MRI Tumor Segmentation — Otsu vs Sauvola Thresholding

## 📌 Project Overview
This project compares **global thresholding (Otsu)** and **adaptive thresholding (Sauvola)** methods for tumor segmentation in brain MRI images. The goal is to analyze how different thresholding strategies affect segmentation accuracy.

The segmentation results are evaluated using **Dice Score** and **Jaccard Index**, which measure similarity between predicted tumor regions and ground truth masks.

---

## 🎯 Objectives
- Segment tumor regions in MRI slices
- Compare global vs adaptive thresholding
- Evaluate segmentation performance using quantitative metrics
- Understand behavior of thresholding under varying image intensity

---

## 📂 Dataset
**Source:** Kaggle — Brain MRI Tumor Segmentation Dataset  
https://www.kaggle.com/datasets/nikhilroxtomar/brain-tumor-segmentation/data

The dataset contains:
- MRI brain images
- Ground truth tumor masks

Each image has a corresponding binary mask marking tumor regions.

---

## ⚙️ Methods Used

### 1. Otsu Thresholding
- Global thresholding method
- Computes a single optimal threshold for the entire image
- Fast and simple
- Sensitive to uneven lighting and intensity variation

### 2. Sauvola Thresholding
- Adaptive/local thresholding
- Threshold varies across image regions
- Handles non-uniform illumination better
- Produces smoother segmentation boundaries

---

## 📊 Evaluation Metrics

### Dice Score
Measures overlap between predicted and ground truth regions.

\[
Dice = \frac{2 |A ∩ B|}{|A| + |B|}
\]

Range: 0 (no overlap) → 1 (perfect match)

---

### Jaccard Index (IoU)
Measures intersection over union.

\[
Jaccard = \frac{|A ∩ B|}{|A ∪ B|}
\]

Range: 0 → 1

---

## 🛠 Installation

Install required libraries:

```bash
pip install opencv-python scikit-image numpy matplotlib
```

---

## ▶️ How to Run

1. Download dataset from Kaggle
2. Extract images and masks into folders
3. Update folder paths in the script:

```python
image_dir = "path_to_images"
mask_dir = "path_to_masks"
```

4. Run the Python script

The program will:
- Apply Otsu segmentation
- Apply Sauvola segmentation
- Compute Dice and Jaccard scores
- Print average performance

---

## 📈 Results

The output shows average Dice and Jaccard scores for both methods.

Expected trend:
- Sauvola performs better in uneven MRI intensity
- Otsu works well for high-contrast tumors
- Adaptive thresholding generally improves accuracy

---

## 🔍 Observations

- Global thresholding struggles with brightness variation
- Adaptive thresholding adapts to local contrast
- Sauvola produces cleaner tumor boundaries
- Otsu may include background noise in complex images

---

## ✅ Conclusion

Adaptive Sauvola thresholding provides more reliable tumor segmentation in heterogeneous MRI images. While Otsu is computationally simpler, Sauvola achieves higher overlap accuracy due to its local threshold adjustment.

This demonstrates the importance of adaptive techniques in medical image segmentation.

---

## 📎 Future Improvements

- Morphological post-processing
- Noise removal
- Deep learning segmentation models
- Multi-threshold hybrid methods

---

## 👤 Author

**Harsh Tripathi**  
B.Tech — AI & Data Science  
IIIT Raichur  

Roll No: AD23B1021  
Course: Image Processing / Computer Vision  
Project: Brain MRI Tumor Segmentation

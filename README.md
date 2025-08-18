# 🌲 Neon Tree Crown Detection & Clustering

This project performs **tree crown detection and clustering** on RGB aerial imagery from the NEON dataset. It uses bounding box annotations to extract individual tree crowns, compute HSV color histograms, and cluster similar crowns using unsupervised learning.

> 🎯 The goal is to demonstrate preprocessing, feature extraction, and clustering in a real-world computer vision pipeline.

---

## 📂 Dataset

- **Source**: [NeonTreeEvaluation GitHub Repo](https://github.com/weecology/NeonTreeEvaluation)
- Includes:
  - Aerial RGB images
  - XML annotations of tree crowns (Pascal VOC format)

---

## 📸 Sample Images and Cropped Crowns

Below are sample input images and their corresponding cropped crown regions, extracted using bounding boxes.

### 🔹 Image 1

**Original Image**  
![Image 1](samples/image_1.jpg)

**Cropped Crowns**  
![Crown 1-1](samples/image_1_crown_0.jpg)  
![Crown 1-2](samples/image_1_crown_1.jpg)

---

### 🔹 Image 2

**Original Image**  
![Image 2](samples/image_2.jpg)

**Cropped Crown**  
![Crown 2-1](samples/image_2_crown_0.jpg)

---

### 🔹 Image 3

**Original Image**  
![Image 3](samples/image_3.jpg)

**Cropped Crown**  
![Crown 3-1](samples/image_3_crown_0.jpg)

---

## 🧠 Project Pipeline

### 1. 🗂️ Unzip and Load Data
- RGB and XML annotation files are unzipped and parsed.
- Each XML file is linked to its corresponding image.

### 2. 📦 Bounding Box Extraction
- The `parse_annotation()` function reads each XML and extracts `(xmin, ymin, xmax, ymax)` for all tree crowns.

### 3. ✂️ Cropping Crowns
- Each bounding box is used to crop a crown from the RGB image.
- Cropped images are saved to `/content/cropped_crowns`.

### 4. 🌈 Feature Extraction
- HSV color histograms are computed using `cv2.calcHist()`.
- Histograms are flattened and normalized.

### 5. 🤖 Clustering
- Crowns are grouped using `KMeans(n_clusters=2)`.
- Cluster distribution is printed.
- Sample images from each cluster are visualized.

---

## 📊 Output Preview

The cropped crowns are clustered into visually distinct groups.  
Each cluster can represent different vegetation types or lighting conditions.

```python
Cluster distribution: Counter({0: 123, 1: 98})

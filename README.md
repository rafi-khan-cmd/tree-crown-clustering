# 🌲 Tree Crown Detection and Clustering using Remote Sensing Imagery

This project involves detecting tree crowns from high-resolution aerial imagery and clustering them based on their visual appearance. It uses RGB images and annotated XML files from the [NEON Tree Evaluation dataset](https://github.com/weecology/NeonTreeEvaluation), applying classical computer vision and unsupervised machine learning techniques in Python.

---

## 📌 Project Overview

🔍 **Goal**:  
Automatically crop tree crowns from annotated aerial images and cluster them by visual similarity (e.g., color/texture) using color histograms and KMeans clustering.

🧠 **Key Techniques**:
- XML parsing and bounding box extraction
- Image cropping and preprocessing
- Feature extraction via HSV color histograms
- Unsupervised clustering with `KMeans`
- Visualization of clustered crowns

---

## 🗂️ Dataset Source

This project uses the publicly available dataset from:

**📦 NEON Tree Evaluation Dataset**  
🔗 GitHub: [https://github.com/weecology/NeonTreeEvaluation](https://github.com/weecology/NeonTreeEvaluation)  
📜 License: Public domain (CC0)

To get the data:

```bash
git clone https://github.com/weecology/NeonTreeEvaluation.git

# Tree Crown Detection and Clustering

This project detects and clusters tree crowns from aerial RGB images using bounding box annotations.

## 🌿 Features
- Parses `.xml` annotations
- Crops crowns from aerial `.tif` images
- Extracts color histograms
- Clusters using KMeans
- Visualizes results

## 📁 Sample Data
Small subset of RGB and XML files are included in `sample_data/`.

> Full dataset was omitted due to size. You can use your own dataset or request access [here](https://drive.google.com/your-shared-folder).

## 📓 Notebook
This project was developed and tested in Google Colab.  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yourusername/tree-crown-detector/blob/main/main.ipynb)

## 🔧 Setup
```bash
pip install -r requirements.txt

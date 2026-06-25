# Tree Crown Detection and Clustering

Unsupervised clustering of tree crowns from aerial RGB imagery using the NEON dataset.

## What it does

Parses bounding box annotations (Pascal VOC XML format), crops individual tree crowns from aerial images, extracts HSV color histograms as features, and clusters crowns using KMeans.

## Dataset

NEON Tree Evaluation dataset: https://github.com/weecology/NeonTreeEvaluation

Includes aerial RGB images and XML annotations for tree crown bounding boxes.

## Pipeline

1. Parse XML annotations and link to corresponding images
2. Crop each tree crown using bounding box coordinates
3. Extract and normalize HSV color histograms with cv2.calcHist()
4. Cluster crowns into 2 groups using KMeans

## Results

221 crowns processed across 3 images. Cluster distribution: Counter({0: 123, 1: 98}). The two clusters broadly correspond to different vegetation types distinguished by HSV color signature.

## Dependencies

Python, OpenCV, NumPy, scikit-learn

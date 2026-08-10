# Copy-Move-Forgery-Detection-ML

Python implementation of a Machine Learning-based Copy-Move Forgery Detection method using SIFT, DWT, Multi-Scale LBP, and SVM.

This notebook uses SIFT, DWT, and Multi-Scale LBP to extract features from images and uses an SVM classifier to detect copy-move forgery.

# Dataset
Tested on the MICC-F220 dataset for copy-move forgery detection.

# Requirements & Installation
Install the required packages using:

```bash
pip install opencv-python numpy scipy pywavelets scikit-image scikit-learn


Classic vs. Machine Learning Approach
This repository focuses on the supervised learning approach (SVM classification). For the classic computer vision implementation using KNN matching and decision fusion, visit the Classic Repository ([https://github.com/shirinnayerdin/copy_move_forgery_detection](https://github.com/shirinnayerdin/copy_move_forgery_detection)).


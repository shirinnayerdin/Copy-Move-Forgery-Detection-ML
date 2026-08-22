# Copy-Move Forgery Detection Using Machine Learning

Python implementation of a Machine Learning-based Copy-Move Forgery Detection method using SIFT, DWT, Multi-Scale LBP, and SVM.

## Overview

This project implements a supervised learning approach for detecting copy-move forgery in images.

The method combines SIFT, DWT, and Multi-Scale LBP features and uses an SVM classifier to distinguish between authentic and forged images.

## Dataset

The model was evaluated on the **MICC-F220** dataset.

The final dataset contained **326 samples**:

- 106 Authentic images
- 220 Forged images

Each image was represented by a **42-dimensional feature vector**.

## Methodology

The overall workflow consists of the following steps:

1. Load the image and convert it to grayscale.
2. Apply Gaussian smoothing.
3. Extract SIFT, DWT, and Multi-Scale LBP features.
4. Combine the extracted features into a 42-dimensional feature vector.
5. Split the dataset into 80% training and 20% testing.
6. Standardize the features using StandardScaler.
7. Train an RBF-kernel SVM classifier.
8. Evaluate the classification performance.

## Results

The SVM classifier achieved an overall accuracy of **90.91%** on the test set.

| Metric | Authentic | Forged |
|---|---:|---:|
| Precision | 0.89 | 0.91 |
| Recall | 0.81 | 0.96 |
| F1-Score | 0.85 | 0.93 |

### Confusion Matrix

| | Predicted Authentic | Predicted Forged |
|---|---:|---:|
| Actual Authentic | 17 | 4 |
| Actual Forged | 2 | 43 |

## Implementation

The project is implemented in **Python** using a Jupyter Notebook.

### Libraries

- OpenCV
- NumPy
- PyWavelets
- scikit-image
- scikit-learn

## Requirements

Install the required packages:

```bash
pip install -r requirements.txt
```
## Classic vs. Machine Learning Approach

This repository focuses on the **supervised machine learning approach using SVM classification**.

For the classical computer vision implementation using KNN matching, decision fusion, and spatial verification, see the [Classic CMFD Repository](https://github.com/shirinnayerdin/copy_move_forgery_detection).

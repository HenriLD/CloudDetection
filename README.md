# Cloud Segmentation in Satellite Imagery

This project explores classical computer vision approaches to cloud segmentation in satellite imagery. The goal is to accurately separate cloud regions from satellite images, enabling improved analyses in meteorology, climate research, and environmental monitoring. This approach avoids deep learning techniques in favor of spectral, morphological, and statistical methods.

---

## Table of Contents

- [Introduction](#introduction)
- [Problem Definition](#problem-definition)
- [Challenges](#challenges)
- [Data](#data)
- [Methodology](#methodology)
- [Evaluation](#evaluation)
- [References](#references)

---

## Introduction

Cloud segmentation plays a crucial role in various applications such as land cover mapping, vegetation studies, and agricultural planning. Accurate identification and removal of cloud regions is essential to prevent misclassification that could lead to erroneous conclusions about the environment. This project focuses on exploring classical computer vision techniques for cloud segmentation, offering a transparent and resource-efficient alternative to deep learning methods :contentReference[oaicite:0]{index=0}.

---

## Problem Definition

Given a satellite image with multiple spectral bands, the objective is to generate a binary mask where each pixel is classified as either cloud or non-cloud. The aim is to maximize the accuracy of the mask for downstream applications such as climate monitoring and land cover analysis.

---

## Challenges

Several challenges complicate the task of cloud segmentation:

- **Variability in Cloud Appearance:** Clouds can vary widely in shape, brightness, texture, and color.
- **Spectral Confusion:** Surface features such as snow and ice may exhibit reflectance properties similar to clouds in certain spectral bands.
- **Lighting and Atmospheric Effects:** Changes in lighting conditions and atmospheric effects can alter cloud appearance over time.

---

## Data

The project utilizes the "95-Cloud" dataset, which comprises:
- 95 Landsat 8 scenes
- Over 17,000 non-overlapping patches
- Images with red, green, blue, and near-infrared channels
- Per-pixel ground truth labels for segmentation

For more details, refer to the [GitHub repository](https://github.com/SorourMo/95-Cloud-An-Extension-to-38-Cloud-Dataset).

---

## Methodology

The approach is centered on a pipeline of classical computer vision techniques, avoiding the use of deep neural networks. Proposed methods include:

- **Color Thresholding and Histograms:** Leveraging the near-infrared channel for multispectral analysis to differentiate between clouds and similar features like snow or ice.
- **Edge Detection:** Using methods such as Canny or Laplacian of Gaussian to capture scale-agnostic features, accommodating clouds of various sizes.
- **Principal Component Analysis (PCA):** To reduce dimensionality and enhance feature discrimination.
- **Morphological Operations:** For denoising and refining the segmentation mask.
- **Ensemble Methods:** Per-pixel voting could be employed to combine multiple strategies for improved performance, despite potential computational costs.

---

## Evaluation

The segmentation performance will be evaluated using the ground truth masks from the dataset. Metrics to be used include:

- Precision
- Recall
- F1 Score
- Jaccard Index
- Accuracy

These metrics will help identify the strengths and weaknesses of the different approaches.

---

## References

1. Mahajan, S., & Fataniya, B. (2019). Cloud detection methodologies: Variants and development—a review. *Complex & Intelligent Systems, 6*(2), 251–261. [https://doi.org/10.1007/s40747-019-00128-0](https://doi.org/10.1007/s40747-019-00128-0)
2. Danda, S., Challa, A., & Daya Sagar, B. S. (2016). A morphology-based approach for cloud detection. *2016 IEEE International Geoscience and Remote Sensing Symposium (IGARSS)*, 80–83. [https://doi.org/10.1109/igarss.2016.7729011](https://doi.org/10.1109/igarss.2016.7729011)
3. Hayatbini, N., Hsu, K., Sorooshian, S., Zhang, Y., & Zhang, F. (2019). Effective cloud detection and segmentation using a gradient-based algorithm for satellite imagery: Application to improve PERSIANN-CCS. *Journal of Hydrometeorology, 20*(5), 901–913. [https://doi.org/10.1175/jhm-d-18-0197.1](https://doi.org/10.1175/jhm-d-18-0197.1)
4. Zi, Y., Xie, F., & Jiang, Z. (2018). A Cloud Detection Method for Landsat 8 Images Based on PCANet. *Remote Sensing, 10*(6), 877. [https://doi.org/10.3390/rs10060877](https://doi.org/10.3390/rs10060877)

Image Tampering Detection with Cryptographic Verification

**Author:** Ivan Bageya  
**Date:** August 2026  
**Dataset:** CASIA 2.0  

## Overview
This project implements an AI-powered image forensics system that detects tampered images using:
- **MobileNetV2** deep learning model
- **SHA-256 cryptographic hashing** for chain-of-custody
- **Grad-CAM** explainable AI visualizations
- **Error Level Analysis (ELA)** preprocessing

## Methodology
1. **Data Preparation** - Split CASIA 2.0 dataset (70/15/15)
2. **Cryptographic Hashing** - SHA-256 for each image
3. **Feature Engineering** - Error Level Analysis (ELA)
4. **Model Training** - Transfer learning with MobileNetV2
5. **Explainability** - Grad-CAM heatmaps
6. **Forensic Reporting** - Audit trail generation

## 📊 Results
| Metric    | Score  |
|-----------|--------|
| Accuracy  | 0.9027 |
| Precision | 0.8349 |
| Recall    | 0.9479 |
| F1 Score  | 0.8878 |
| AUC       | 0.9690 |


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

## Results
| Metric    | Score  |
|-----------|--------|
| Accuracy  | 0.9027 |
| Precision | 0.8349 |
| Recall    | 0.9479 |
| F1 Score  | 0.8878 |
| AUC       | 0.9690 |

## Cryptographic:
    Algorithm: SHA-256
    Records: 100

## Explainable AI:
    Method: Grad-CAM
    Layer: features.18

## Outputs:
    Model: /content/mobilenet_ela_final.pth
    Config: model_config.json
    Audit: audit_report.csv
    Report: forensic_report.json
    Training Curves: training_curves.png
    Confusion Matrix: confusion_matrix.png
    ROC Curve: roc_curve.png
    Grad-CAM Outputs: gradcam_outputs/
## Outputs Two: Mobile App Integration 

I am developing a **mobile application** that makes image tampering testing quick and accessible. The app uses the trained model from this project to provide on-the-go forensic analysis.
### App Features
-  **Camera Integration:** Capture or upload images directly from your phone
-  **Real-time Analysis:** Instant tampering detection using the trained MobileNetV2 model
-  **Cryptographic Verification:** SHA-256 hash verification for chain of custody
### App Results
The `app/` folder contains sample results from the mobile app testing:

| File | Description |
|------|-------------|
| `app/screenshots/` | UI screenshots showing the app in action |
| `app/test_results/` | Sample images with their detection results |

####  User Interface
The app provides a simple, intuitive interface for forensic analysis:
- Home screen with upload/photo options
- Results screen showing tampering probability

####  Example Results
| Image Type | Detection Result | Confidence | Hash Status |
|------------|-----------------|------------|-------------|
| Authentic |  PASS | 89.2% | INTACT ✅ |
| Tampered |  FAIL | 92.4% | INTACT ✅ |
| Authentic |  PASS | 87.6% | INTACT ✅ |
| Tampered |  FAIL | 94.1% | INTACT ✅ |

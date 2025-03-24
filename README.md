# Radar Target Classification using Deep Learning (MSTAR Dataset)

This project explores deep learning-based classification of ground targets in Synthetic Aperture Radar (SAR) images using the MSTAR dataset. It compares a series of models, from classical convolutional networks to transformer-based and hybrid architectures, designed specifically for scenarios with limited data availability.

---

## 📁 Project Structure

- `models/`: Contains training notebooks for each architecture:
  - `1_custom_cnn.ipynb`: Baseline ResNet-like CNN
  - `2_mobilenetv2.ipynb`: Fine-tuned lightweight MobileNetV2
  - `3_vit_only.ipynb`: Vision Transformer (ViT) only
  - `4_hybrid_cnn_vit.ipynb`: Hybrid CNN + ViT model (best performing)
  - `5_siamese_hybrid.ipynb`: Siamese model using hybrid backbone for few-shot learning

- `data_preprocessing/`: Scripts for image resizing, normalization, augmentation, and train-test split

- `results/`:
  - `confusion_matrix.png`: Confusion matrix for Hybrid model
  - `classification_report.txt`: Precision, recall, F1-score

- `images/`:
  - Architecture/system diagrams (used in report)

- `README.md`: Project overview and model comparison

- `requirements.txt`: Libraries used

---

## ✅ Final Test Accuracies

| Model               | Test Accuracy |
|--------------------|---------------|
| Custom CNN         | 97.43%        |
| MobileNetV2        | 83.21%        |
| Vision Transformer | 99.26%        |
| Hybrid CNN + ViT   | **99.89%**    |
| Siamese Hybrid     | 95.51%        |

---

## 💪 Highlights

- **Hybrid CNN-ViT model** delivered the best classification performance (99.89%) on the 8-class MSTAR SAR benchmark.
- **Siamese network** using the hybrid model showed strong performance (95.5%) for pairwise similarity tasks.
- Extensive use of transfer learning, data augmentation, and mixed precision to address the small dataset challenge.

---

## 🛠️ Setup

```bash
pip install -r requirements.txt
```

---

## 📄 Report

Full project report with system design, algorithm iterations, and analysis: [link-to-final-report.pdf](#)

---

## 📅 Course Info

This repository is part of the final project for a Deep Learning course, focusing on SAR-based target classification with small datasets.


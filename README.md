# Radar Target Classification using Deep Learning (MSTAR Dataset)

This project explores deep learning-based classification of ground targets in Synthetic Aperture Radar (SAR) images using the MSTAR dataset. It compares a series of models, from classical convolutional networks to transformer-based and hybrid architectures, designed specifically for scenarios with limited data availability.

---

## 📁 Project Structure

- `models/`: Contains training notebooks for each architecture:
- `data_preprocessing/`: Scripts for image resizing, normalization, augmentation, and train-test split
 ### 📂 Deep Learning Models

| Model                        | Description                                                     | Notebook Link                                                                 |
|-----------------------------|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| 📊 Data Visualization       | Visual inspection of the MSTAR dataset                         | [📓 View Notebook](https://github.com/Mulubrhan21/Radar_Target_Classification_mstar/blob/main/DLmodels/Data_Visualization.ipynb) |
| 🧠 Custom CNN (ResNet50)     | Baseline ResNet-inspired CNN for SAR classification            | [📓 View Notebook](https://github.com/Mulubrhan21/Radar_Target_Classification_mstar/blob/main/DLmodels/Cnn(ResNet50).ipynb)       |
| ⚡ MobileNetV2 (Fine-Tuned)  | Lightweight CNN fine-tuned for edge deployment                  | [📓 View Notebook](https://github.com/Mulubrhan21/Radar_Target_Classification_mstar/blob/main/DLmodels/MobileNetV2_.ipynb)        |
| 🧠 Vision Transformer (ViT)  | Transformer model capturing global SAR features                 | [📓 View Notebook](https://github.com/Mulubrhan21/Radar_Target_Classification_mstar/blob/main/DLmodels/ViT.ipynb)                 |
| 🔗 Hybrid CNN + ViT         | Fused model combining CNN local features + ViT global features | [📓 View Notebook](https://github.com/Mulubrhan21/Radar_Target_Classification_mstar/blob/main/DLmodels/Hybrid_vitcnn.ipynb)       |

- `results/`:
  - `confusion_matrix.png`: Confusion matrix for Hybrid model
  - `classification_report.txt`: Precision, recall, F1-score

- `images/`:
  - Architecture/system diagrams (used in report)

- `README.md`: Project overview and model comparison
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


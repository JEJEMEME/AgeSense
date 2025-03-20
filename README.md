# 📱 AgeSense

*A lightweight, mobile-friendly age prediction model optimized for deployment across multiple platforms (PyTorch, ONNX, CoreML).*  

---

## 🎯 Overview

**AgeSense** is a mobile-optimized deep learning model for predicting age from facial images. The model leverages **MobileNetV2** architecture to ensure high performance and efficiency on mobile devices. Provided in PyTorch, ONNX, and CoreML formats, **AgeSense** can easily be integrated into iOS, Android, or Web-based applications.

---

## 🔍 Dataset

- **Dataset:** [All-Age-Faces Dataset (UTKFace)](https://susanqq.github.io/UTKFace/)  
- The age labels were extracted from filenames formatted as `xxxAyy.jpg`, where `yy` denotes the individual's age.

---

## ⚙️ Model Details

- **Architecture**: MobileNetV2 (Pretrained)
- **Task**: Age Regression
- **Training Data Split**: 80% train / 20% validation
- **Epochs**: 15
- **Loss Function**: Mean Absolute Error (L1 Loss)
- **Optimizer**: Adam with differential learning rates
- **Learning Rate Scheduler**: StepLR (decay every 5 epochs)

---

## 📊 Performance

| Metric                      | Result           |
|-----------------------------|------------------|
| **Mean Absolute Error (MAE)** | **6.27 years**    |

*(Evaluated after 15 epochs on the validation set.)*

---

## 🚀 Usage

The trained model is available in the following formats:

- **PyTorch** (`age_model.pt`)
- **ONNX** (`age_model.onnx`)
- **CoreML** (`age_model.mlmodel` & `age_model_quantized.mlmodel`)

You can directly integrate these models into your mobile applications or inference pipelines.

---

## 📜 License

- **Author**: jejememe
- **License**: MIT License

---

## 📮 Contact

For inquiries, please contact:

- **Email**: ray@jejememe.com
- **GitHub**: [jejememe](https://github.com/jejememe)

---


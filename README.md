# 📱 AgeSense

*A lightweight, mobile-friendly age prediction model optimized for deployment across multiple platforms (PyTorch, ONNX, CoreML, TFLite).*  

---

## 🎯 Overview

**AgeSense** is a mobile-optimized deep learning model for predicting age from facial images. The model leverages a modified **MobileNetV2** architecture that benefits from enhanced data augmentation and extended fine-tuning for improved performance. It is provided in multiple formats (PyTorch, ONNX, CoreML) so you can easily integrate it into iOS, Android, or web applications.

---

## 🔍 Dataset

- **Dataset:** [All-Age-Faces Dataset](https://github.com/JingchunCheng/All-Age-Faces-Dataset?tab=readme-ov-file)  

---

## ⚙️ Model Details

- **Architecture**: Modified MobileNetV2 (Pretrained)
- **Task**: Age Regression
- **Training Data Split**: 80% train / 20% validation
- **Epochs**: 30
- **Loss Function**: Mean Squared Error (MSE Loss)
- **Optimizer**: AdamW with differential learning rates  
  - Backbone: lr = 1e-4  
  - Classifier: lr = 1e-3  
- **Learning Rate Scheduler**: StepLR (decay every 10 epochs)
- **Data Augmentation**: Uses `RandomResizedCrop`, `RandomHorizontalFlip`, `RandomRotation`, and `ColorJitter` for better generalization.
- **Fine-Tuning**: Extended fine-tuning by freezing only the initial layers (i < 10) of MobileNetV2.

---

## 📊 Performance

| Metric                      | Result           |
|-----------------------------|------------------|
| **Mean Absolute Error (MAE)** | **5.76 years**    |

*(Evaluated on the validation set after 30 epochs.)*

---

## 🚀 Usage

The trained model is available in the following formats for seamless integration into your mobile or web applications:

- **PyTorch** (`age_sense.pt` or `one_a_complete_age_model.pth`)
- **ONNX** (`age_sense.onnx`)
- **CoreML** (`age_sense.mlmodel` & `age_sense_quantized.mlmodel`)

---

## 📜 License

- **Author**: ray@jejememe
- **License**: MIT License

---

## 📮 Contact

For inquiries, please contact:

- **Email**: ray@jejememe.com
- **GitHub**: [jejememe](https://github.com/jejememe)

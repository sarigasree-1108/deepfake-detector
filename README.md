<div align="center">

# 🕵️ Deepfake Detector

### *An AI-powered web application that exposes manipulated faces with high accuracy*

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://tensorflow.org)
[![Streamlit](https://img.shields.io/badge/Streamlit-App-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io)
[![Keras](https://img.shields.io/badge/Keras-EfficientNetV2-D00000?style=for-the-badge&logo=keras&logoColor=white)](https://keras.io)

</div>

---

## 📌 Overview

**Deepfake Detector** is a machine learning project that identifies whether a face image is **real** or **AI-generated (fake)**. It leverages a fine-tuned **EfficientNetV2-B0** architecture and is served through an interactive **Streamlit** web app with two engaging modes.

> 🏆 **Top Model Accuracy: ~96.5%** on validation data using EfficientNetV2-B0

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔍 **Detector Mode** | Upload any face image and get an instant Real/Fake prediction with confidence score |
| 🎮 **Game Mode** | Challenge yourself — guess if an image is real or fake before the model reveals the answer |
| ⚡ **Fast Inference** | Pre-trained model cached for near-instant predictions |
| 🧠 **EfficientNetV2-B0** | State-of-the-art CNN backbone fine-tuned for deepfake detection |

---

## 🏗️ Project Structure

```
deepfake-detector/
│
├── 📁 PretrainedModel/
│   ├── 📁 streamlit_deepfake_detector/   # Streamlit web app
│   │   ├── multipage_app.py              # Main app entry point
│   │   └── 📁 images/                   # Sample Real & Fake images
│   ├── dffnetv2B0.json                   # Model architecture
│   ├── dffnetv2B0.h5                     # Model weights
│   └── deepfake_model_tutorial.ipynb     # Model walkthrough notebook
│
├── 📁 main/
│   └── 📁 Training/
│       └── Full_Training.ipynb           # Full training pipeline
│
├── 📁 helper/
│   └── config.py                         # Utility functions & model helpers
│
├── 📁 results/
│   ├── model_eval.csv                    # Model comparison results
│   └── v2b0_history.csv                  # Training history
│
└── README.md
```

---

## 🤖 Model Performance

Multiple architectures were trained and evaluated. Here is a comparison:

| Model | Val Accuracy | Val AUC | Val Precision | Val Recall |
|---|---|---|---|---|
| 🥇 **EfficientNetV2-B0** | **96.51%** | **98.24%** | 99.19% | 94.98% |
| 🥈 CNN (Tuned) | 91.81% | 96.99% | 91.42% | 92.36% |
| 🥉 EfficientNetV2-L | 89.12% | 95.64% | 88.75% | 89.69% |
| CNN (Benchmark) | 82.16% | 91.69% | 77.23% | 91.39% |

> The **EfficientNetV2-B0** model achieved the best balance of accuracy and generalization.

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install streamlit tensorflow tf-keras numpy pillow streamlit-image-select
```

### Run the App

```bash
cd PretrainedModel/streamlit_deepfake_detector
streamlit run multipage_app.py
```

Then open your browser at **http://localhost:8501** 🎉

---

## 🕹️ How to Use

### 🔍 Detector Mode
1. Select **"Detector Mode"** from the sidebar
2. Upload a `.jpg` or `.jpeg` face image
3. Instantly see the prediction: **Real** or **Fake** with a confidence score

### 🎮 Game Mode
1. Select **"Game Mode"** from the sidebar
2. Browse the sample image gallery and click an image
3. Make your guess — **Real** or **Fake**
4. See how your guess compares to the model's prediction and the ground truth!

---

## 🧪 Training Pipeline

The model was trained using:
- **Architecture:** EfficientNetV2-B0 (transfer learning)
- **Loss:** Binary Cross-Entropy
- **Optimizer:** Adam
- **Callbacks:** EarlyStopping, ReduceLROnPlateau
- **Input Size:** 256 × 256 pixels
- **Metrics:** Accuracy, AUC, Precision, Recall

Full training code is available in [`Full_Training.ipynb`](main/Training/Full_Training.ipynb).

---

## 📦 Tech Stack

- **Deep Learning:** TensorFlow / Keras (EfficientNetV2-B0)
- **Web App:** Streamlit
- **Image Processing:** Pillow, NumPy
- **Data Analysis:** Pandas, Matplotlib, Seaborn

---

## 📄 Research Paper

This project is accompanied by a research paper:

> **"A Robust Framework for Deepfake Detection Using Advanced Neural Architectures and Generalization Techniques"**

Available in [`PretrainedModel/streamlit_deepfake_detector/`](PretrainedModel/streamlit_deepfake_detector/)

---

## 👩‍💻 Author

**Sari Gasree**
- GitHub: [@sarigasree-1108](https://github.com/sarigasree-1108)

---

<div align="center">

*Made with ❤️ and a passion for AI safety*

⭐ **Star this repo if you found it useful!** ⭐

</div>

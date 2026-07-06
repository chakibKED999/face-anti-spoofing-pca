# 🎭 Face Anti-Spoofing using PCA & SVM

A Computer Vision project that detects whether a face presented to a camera is **Real** or **Fake** using **Principal Component Analysis (PCA)** for dimensionality reduction and an **SVM classifier** for binary classification.

The project was developed using the **CASIA Face Anti-Spoofing Dataset** and includes a complete machine learning pipeline, from image preprocessing to interactive prediction using uploaded images or a webcam.

---

# 📌 Overview

Face recognition systems are vulnerable to presentation attacks such as:

* 📷 Printed photographs
* 📱 Replay attacks on screens
* 🎭 Fake facial representations

This project proposes an anti-spoofing pipeline capable of distinguishing between genuine and fake faces by combining dimensionality reduction with supervised classification.

---

# ✨ Features

* ✅ Image preprocessing pipeline
* ✅ Face normalization
* ✅ PCA (Eigenfaces) feature extraction
* ✅ Automatic dimensionality reduction
* ✅ SVM classifier
* ✅ PCA visualization
* ✅ Model calibration
* ✅ Upload image prediction
* ✅ Webcam prediction
* ✅ Performance evaluation

---

# 📊 Dataset

**CASIA Face Anti-Spoofing Dataset**

Dataset statistics:

* **Images:** 1,655
* **Image size:** 64 × 64
* **Features per image:** 4,096
* **Classes:**

  * Real
  * Fake

Each image is converted into a grayscale vector before PCA projection.

---

# ⚙️ Machine Learning Pipeline

The system follows these stages:

1. Face preprocessing
2. Grayscale conversion
3. Image resizing (64×64)
4. Image vectorization
5. Feature standardization
6. PCA dimensionality reduction
7. SVM classification
8. Probability calibration
9. Final prediction

---

# 🧠 PCA Analysis

The project includes a complete exploratory PCA study:

* Eigenvalue analysis
* Explained variance
* Cumulative variance
* Eigenfaces visualization
* Correlation circles
* Biplots
* Contribution analysis
* Cos² analysis
* Correlation heatmaps
* Pixel importance maps

Unlike many PCA projects that only use dimensionality reduction, this project also analyzes the structure and interpretability of the feature space.

---

# 🤖 Classification

Several PCA dimensions were evaluated before training the classifier.

The final model uses:

* **PCA**
* **Balanced SVM (RBF Kernel)**
* **Probability calibration**

The optimal number of principal components was selected experimentally, with **150 principal components** providing the best validation performance.

---

# 📈 Evaluation

The project evaluates the model using:

* Confusion Matrix
* Balanced Accuracy
* Recall
* Classification Errors
* Threshold Calibration
* Validation vs Test Comparison

It also analyzes misclassified samples to better understand challenging cases located near the overlap between the Real and Fake classes.

---

# 📷 Interactive Demo

The notebook supports real-time testing through:

* 📁 Uploading an image
* 📷 Webcam capture (Google Colab)

The prediction pipeline automatically:

* Detects the face
* Applies preprocessing
* Projects the image into PCA space
* Predicts whether the face is **Real** or **Fake**

Example predictions include successful classification of both genuine faces and spoofing attacks with confidence scores.

---

# 🛠 Technologies Used

* Python
* NumPy
* Pandas
* OpenCV
* Scikit-learn
* Matplotlib
* Google Colab

---

# 📂 Project Structure

```text
face-anti-spoofing-pca/
│
├── notebook.ipynb
├── dataset/
├── models/
├── results/
│   ├── eigenfaces.png
│   ├── confusion_matrix.png
│   ├── pca_projection.png
│   ├── calibration_curve.png
│   └── webcam_demo.png
├── README.md
├── requirements.txt
└── docs/
    └── report.pdf
```

---

# 🚀 Future Improvements

* Deep learning based anti-spoofing (CNNs)
* Liveness detection using video sequences
* Real-time desktop application
* Mobile deployment
* Support for RGB and depth images
* Benchmark against modern deep learning models

---

# 📄 License

This project is available for educational and research purposes.

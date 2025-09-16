# MNIST Classification using VGG19 Pretrained Model

## 🎯 Aim

To classify handwritten digits (0–9) from the **MNIST dataset** by leveraging a **pretrained VGG19 model** as a feature extractor, followed by fully connected layers for classification.

---

## 📌 Project Description

* The MNIST dataset consists of **60,000 training** and **10,000 testing grayscale images** of handwritten digits, size **28×28 pixels**.

* Since VGG19 expects **3-channel images** and minimum size of **48×48**, preprocessing involves:

  * Expanding grayscale images to **RGB (3 channels)** by repeating the single channel.
  * Resizing each image to **48×48 pixels**.

* **Pretrained VGG19** (without top classifier layers) is used as a **feature extractor**.

* A simple classification head is added:

  * Flatten → Dense(256, ReLU) → Dense(10, Softmax).

* The model is trained using **Adam optimizer** and **categorical crossentropy loss**.

---

## 📊 Workflow

```
Data Loading → Preprocessing (RGB & Resize) → VGG19 Feature Extraction → Classification Layers → Evaluation & Visualization
```

---

## ✅ Results & Visualizations

* Final Test Accuracy achieved: **\~98–99%** (high performance due to pretrained features).
* Visualized:

  * Bar plot showing dataset size distribution.
  * Training history curves for accuracy and loss (train vs. validation).
  * Confusion matrix showing detailed class-wise performance.
  * Sample predictions with predicted probabilities shown in bar charts.

| Metric        | Value (Approx) |
| ------------- | -------------- |
| Test Accuracy | \~98–99%       |
| Test Loss     | Varies         |

---

## 📊 Example Visual Output

* Confusion Matrix shows strong diagonal dominance → Few misclassifications.
* Prediction Bar Plots visualize model confidence per class.

---


## ✅ Insights

* Using a pretrained model like **VGG19** provides strong features, enabling very good performance even when fine-tuning only the top layers.
* Preprocessing (RGB conversion + resizing) is essential to make the data compatible with VGG19 input.
* Provides a good baseline for transfer learning in image classification tasks.

---
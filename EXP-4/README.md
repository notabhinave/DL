# CIFAR-10 Classification: Xavier vs. Kaiming Initialization with MLP

## 🎯 Aim

To classify CIFAR-10 images using a **Multi-Layer Perceptron (MLP)** model and compare the effect of two weight initialization strategies — **Xavier (Glorot Normal)** and **Kaiming (He Normal)** — on model performance.

---

## 📌 Project Description

This project demonstrates the role of **weight initialization** in training deep neural networks.

* The **CIFAR-10 dataset** (60,000 color images across 10 classes) is used.
* The model is built as an **MLP**, where the images are flattened into vectors and passed through multiple fully connected layers with ReLU activations.
* Two initialization techniques are tested:

  * **Xavier (Glorot Normal):** Balances the variance of inputs and outputs, suitable for sigmoid/tanh.
  * **Kaiming (He Normal):** Optimized for ReLU activations, maintains stable variance in deeper networks.
* Regularization is applied using **L2 weight decay** to control overfitting.

The models are trained with the **Adam optimizer** for 20 epochs, and their performance is compared through accuracy metrics and training history plots.

---

## 📊 Results

* Both models successfully learn to classify CIFAR-10 images, but **Kaiming initialization typically outperforms Xavier** in this ReLU-based architecture.
* Accuracy curves show that Kaiming converges faster and often achieves **higher validation accuracy**.
* The MLP approach achieves moderate results (\~40–55% test accuracy) on CIFAR-10, which highlights the challenge of image classification without convolutional layers.
* Visualization of accuracy plots helps illustrate the difference in learning dynamics between the two initializations.

---


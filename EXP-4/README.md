# **CIFAR-10 Classification: Xavier vs. He Initialization with MLP**

## **Aim**

To compare the performance of **Xavier (Glorot Normal)** and **He Normal** weight initialization methods in a fully connected neural network (MLP) for image classification on the CIFAR-10 dataset, using **data augmentation**, **Batch Normalization**, **Dropout**, and **Early Stopping**.

---

## **Short Description**

This project focuses on evaluating how **different weight initialization strategies** impact the training and performance of an MLP on image data.
The CIFAR-10 dataset contains **60,000 color images (32×32×3)** in **10 classes** (e.g., airplane, car, bird, cat, etc.).

### **Main Features**

* **Data Preprocessing:** Normalized pixel values and one-hot encoded labels.
* **Data Augmentation:** Rotation, width & height shift, and horizontal flips.
* **Model Architecture:**

  * Flatten input layer (32×32×3 → vector form).
  * Dense layers: 512 → 256 → 128 neurons with Batch Normalization, Dropout, and L2 regularization.
  * Output layer with 10 neurons (Softmax).
* **Comparison Setup:**

  * **Xavier (Glorot Normal)** initialization with **Sigmoid** activation.
  * **He Normal** initialization with **ReLU** activation.
* **Training:** Adam optimizer with tuned learning rates, EarlyStopping callback.

---

## **About the Result**

* **Final Test Accuracy:**

  * **Xavier (Sigmoid):** \~42.24%
  * **He (ReLU):** \~40.51%
* Xavier initialization with Sigmoid slightly outperformed He initialization with ReLU in this MLP setting.
* The accuracy values are moderate because MLPs are not well-suited for high-dimensional image data compared to CNNs.
* Data augmentation helped reduce overfitting, but the overall model still struggled to capture spatial features in CIFAR-10 images.

---

## **Result Highlights**

* **Best Xavier Model:** Accuracy peaked around epoch 40.
* **Best He Model:** Accuracy peaked around epoch 39.
* Early stopping prevented unnecessary training and potential overfitting.
* The plots show that:

  * Both models had steady but slow improvement.
  * Loss curves stabilized but did not reach very low values due to dataset complexity.

---

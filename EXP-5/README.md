# 🖼️ MNIST Handwritten Digit Classification using CNN

## **1. Aim**

The goal of this project is to develop and train a **Convolutional Neural Network (CNN)** that can accurately classify handwritten digits (0–9) from the **MNIST dataset**. CNNs are particularly well-suited for image recognition tasks because they are capable of automatically learning spatial hierarchies of features through convolution and pooling operations.

---

## **2. Project Description**

The MNIST dataset is one of the most widely used benchmarks for image classification. It contains **70,000 grayscale images** of handwritten digits, each of size **28x28 pixels**. Out of these, **60,000 images are used for training** and **10,000 images for testing**.

### **Steps followed in the project:**

1. **Data Loading and Preprocessing**

   * Loaded MNIST dataset from TensorFlow.
   * Normalized pixel values to a range between 0 and 1 for faster and stable training.
   * Reshaped data into 4D tensors to fit CNN input shape: `(samples, height, width, channels)`.
   * Converted labels into **one-hot encoded vectors** for multi-class classification.

2. **Model Architecture**

   * The CNN model is built using `tf.keras.Sequential()` with the following layers:

     * **Conv2D (32 filters, kernel size 3x3, ReLU)** → Extracts low-level features like edges.
     * **MaxPooling2D (2x2)** → Reduces spatial dimensions while retaining key features.
     * **Conv2D (64 filters, kernel size 3x3, ReLU)** → Learns more complex features.
     * **MaxPooling2D (2x2)** → Further reduces dimensions and prevents overfitting.
     * **Conv2D (64 filters, kernel size 3x3, ReLU)** → Learns even higher-level features.
     * **Flatten Layer** → Converts 2D feature maps into a 1D vector.
     * **Dense (64 units, ReLU)** → Fully connected layer for learning non-linear combinations of features.
     * **Dense (10 units, Softmax)** → Output layer for 10 digit classes.

3. **Compilation**

   * **Optimizer**: Adam (adaptive learning optimizer).
   * **Loss Function**: Categorical Crossentropy (since it’s multi-class classification).
   * **Metrics**: Accuracy.

4. **Training**

   * Trained the model for **5 epochs** with **batch size of 64**.
   * Used an **80-20 training-validation split**.
   * Accuracy and loss values were recorded for both training and validation sets.

5. **Evaluation**

   * The trained model was tested on unseen **10,000 test images**.
   * Achieved high accuracy with minimal overfitting.

---

## **3. Results**

The model showed excellent performance on MNIST classification.

* **Training Accuracy**: \~99%
* **Validation Accuracy**: \~98–99%
* **Test Accuracy**: \~99%

This indicates that the CNN was able to generalize well to unseen data.

| Metric              | Value (Approx) |
| ------------------- | -------------- |
| Training Accuracy   | 99%            |
| Validation Accuracy | 98–99%         |
| Test Accuracy       | \~99%          |

---

## **4. Visualizations**

The following plots were generated to track training progress:

1. **Accuracy Curve** – Training vs. Validation accuracy over epochs.

   * Shows steady improvement and stabilization around 98–99%.

2. **Loss Curve** – Training vs. Validation loss over epochs.

   * Loss decreases consistently, indicating effective learning.

📊 Example:

* Accuracy Plot: Demonstrates how the model steadily learns features.
* Loss Plot: Ensures that the model is not overfitting/underfitting.

---


## **5. Conclusion**

* CNNs are extremely effective for digit recognition tasks.
* The model achieved close to **99% accuracy**, proving its robustness and reliability.
* This project can be extended to more complex datasets (like CIFAR-10, Fashion-MNIST) to analyze CNN performance further.



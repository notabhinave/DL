# Simple RNN on IMDB dataset

## 🎯 Aim

To classify movie reviews from the **IMDB dataset** as **positive or negative** using a **Recurrent Neural Network (RNN)** model, leveraging word embeddings and sequential learning.

---

## 📌 Project Description

* The **IMDB dataset** contains **50,000 movie reviews** labeled as positive (1) or negative (0).
* Each review is preprocessed into **word indices** with a fixed vocabulary size (e.g., top 10,000 most frequent words).
* Steps followed:

  * Load dataset and preprocess reviews (padding/truncation).
  * Use an **Embedding Layer** to map words to dense vectors.
  * Apply **RNN/LSTM/GRU layers** to capture sequential dependencies.
  * Add Dense layer with **sigmoid activation** for binary sentiment classification.

---

## 📊 Workflow

```
Data Loading → Preprocessing (Tokenization & Padding) → Embedding Layer → RNN (LSTM/GRU) → Dense → Output (Positive/Negative)
```

---

## ✅ Results & Visualizations

* Model achieves around **85–90% accuracy** depending on hyperparameters (embedding size, number of RNN units, epochs).
* Training/Validation curves are plotted to show performance trends.
* Confusion matrix provides insights into misclassified reviews.

| Metric            | Value (Approx) |
| ----------------- | -------------- |
| Training Accuracy | \~90%          |
| Test Accuracy     | \~85–88%       |

---

## 📊 Example Visual Output

* **Training vs Validation Accuracy** plots.
* **Training vs Validation Loss** plots.
* **Confusion Matrix** for binary classification.

---


## ✅ Insights

* RNNs (especially **LSTM/GRU**) capture sequential dependencies, making them effective for sentiment analysis.
* Word embeddings reduce dimensionality and improve representation of words compared to one-hot encoding.
* Overfitting can occur if the RNN is too deep or trained too long — regularization (dropout/L2) helps.

---


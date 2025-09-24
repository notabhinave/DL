🎯 Aim
To perform a comparative analysis of RNN, LSTM, and GRU models for sentiment classification on the IMDB dataset, evaluating their performance in terms of accuracy, loss trends, and generalization ability.

📌 Project Description
The IMDB dataset contains 50,000 movie reviews labeled as positive (1) or negative (0).
Each review is preprocessed into word indices with a fixed vocabulary size (e.g., top 10,000 most frequent words).
Steps followed:
-Load dataset and preprocess reviews (padding/truncation).
-Use an Embedding Layer to map words to dense vectors.
-Build three separate models using RNN, LSTM, and GRU layers.
-Train and evaluate each model on the dataset.

Compare their performance using accuracy, loss, and confusion matrices.

📊 Workflow
Data Loading → Preprocessing (Tokenization & Padding) → Embedding Layer → RNN / LSTM / GRU → Dense → Output (Positive/Negative) → Comparison

✅ Results & Observations

-RNN: Fast to train, but struggles with long-term dependencies, leading to lower accuracy.=
-LSTM: Handles long-term dependencies better, achieves higher accuracy than vanilla RNN.
-GRU: Performs similarly to LSTM but with fewer parameters, making it computationally more efficient.

Metric | RNN | LSTM | GRU
Training Accuracy | ~85% | ~90% | ~89%
Test Accuracy | ~82–84% | ~86–88% | ~85–87%

Generalization | Prone to vanishing gradients | Strong long-term memory | Balanced memory + efficiency

📊 Example Visual Output

Training vs Validation Accuracy plots for RNN, LSTM, GRU
Training vs Validation Loss plots
Comparative Confusion Matrices

✅ Insights

RNNs are less effective for long sequences due to vanishing gradient issues.
LSTM shows the best performance overall, especially in capturing contextual meaning.
GRU provides nearly the same accuracy as LSTM with faster training due to fewer gates.
Choice between LSTM and GRU depends on whether accuracy (LSTM) or efficiency (GRU) is prioritized.
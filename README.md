# Document Classification Using Deep Learning

## Overview

This project implements and compares multiple Deep Learning approaches for automatic document classification using the AG News dataset. The objective is to classify news articles into one of four predefined categories:

* World
* Sports
* Business
* Sci/Tech

The project evaluates the performance of three different models:

1. Multi-Layer Perceptron (MLP) with TF-IDF Features
2. Vanilla Long Short-Term Memory (LSTM)
3. Bidirectional Long Short-Term Memory (BiLSTM)

---

## Dataset

**Dataset:** AG News Dataset

The AG News dataset is a benchmark dataset widely used for text classification tasks. It contains news articles categorized into four classes:

| Label | Category |
| ----- | -------- |
| 0     | World    |
| 1     | Sports   |
| 2     | Business |
| 3     | Sci/Tech |

Dataset Split:

* Training Samples: 100,000
* Validation Samples: 20,000
* Testing Samples: 7,600

---

## Technologies Used

* Python
* PyTorch
* Scikit-Learn
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Hugging Face Datasets

---

## Project Workflow

### 1. Data Preparation

* Load AG News dataset
* Create train, validation, and test splits
* Normalize class labels

### 2. Feature Engineering

#### MLP

* TF-IDF Vectorization
* 4,000 text features

#### LSTM / BiLSTM

* Text tokenization
* Vocabulary construction
* Sequence padding
* Integer encoding

### 3. Model Development

* MLP Architecture
* Vanilla LSTM Architecture
* Bidirectional LSTM Architecture

### 4. Model Training

* Adam Optimizer
* Early Stopping
* Cross Entropy Loss
* Batch Size = 64

### 5. Model Evaluation

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

---

## Model Performance

| Model              | Accuracy |
| ------------------ | -------: |
| MLP + TF-IDF       |   89.62% |
| Vanilla LSTM       |   28.91% |
| Bidirectional LSTM |   90.61% |

### Best Performing Model

**Bidirectional LSTM (BiLSTM)** achieved the highest classification accuracy of **90.61%**.

---

## Results

The experimental results demonstrate that:

* BiLSTM achieved the highest overall accuracy.
* MLP provided competitive performance with lower computational cost.
* Vanilla LSTM performed significantly worse than the other models.
* Bidirectional context learning improved classification performance.

---

## Sample Predictions

| News Headline                                                  | Predicted Category |
| -------------------------------------------------------------- | ------------------ |
| Apple launches a new AI powered iPhone                         | Sci/Tech           |
| Manchester United wins the football championship               | Sports             |
| Stock market falls after weak earnings reports                 | Business           |
| United Nations discusses global climate policies during summit | World              |
| NASA successfully launches next-generation space telescope     | Sci/Tech           |

---

## Repository Structure

```text
Document-Classification-Using-Deep-Learning/
│
├── Document_Classification.ipynb
├── README.md
├── requirements.txt
└── assets/
    ├── accuracy_comparison.png
    ├── confusion_matrix.png
    └── training_curves.png
```

---

## Future Improvements

* Integrate pre-trained word embeddings (Word2Vec, GloVe)
* Implement GRU-based architectures
* Fine-tune Transformer models such as BERT
* Hyperparameter optimization
* Deploy as a web application using Streamlit

---

## Conclusion

This project successfully developed an automated news article classification system using Deep Learning techniques. Among the evaluated models, the Bidirectional LSTM achieved the highest accuracy of **90.61%**, making it the most effective model for AG News document classification.

---

## Author

Nirbhay Kumar

Course Project – Deep Learning for Document Classification

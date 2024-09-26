#  Reproducing "Dropout: A Simple Way to Prevent Neural Networks from Overfitting"

**Authors:** Carl Machaalani, Winnie Yongru Pan
**Date:** December 5, 2023

## Abstract
In this project, we reproduce the key aspects of the paper ["Dropout: A Simple Way to Prevent Neural Networks from Overfitting."](https://www.cs.toronto.edu/~rsalakhu/papers/srivastava14a.pdf) We implement dropout during the training of a neural network, randomly dropping neurons and their connections. Our results demonstrate that dropout improves accuracy by reducing overfitting, achieving major improvements over other regularization techniques.


## 1. Introduction
Neural networks are versatile but prone to overfitting. To address this, we reproduce models as close to the original paper, introducing dropout to simulate multiple network configurations efficiently.

## 2. Scope of Reproducibility
- **Claim 1 (6.1.1):** Dropout significantly improves classification robustness across various architectures without the need for architecture-specific hyperparameter tuning.
- **Claim 2 (6.5):** Employing dropout regularization on the MNIST dataset results in lower generalization error compared to other regularization methods.
- **Claim 3 (7.4):** The effectiveness of dropout varies with the dataset size, showing improved classification error with larger datasets.

## 3. Methodology
### 3.1 Model Descriptions
We constructed several neural network models to replicate the claims:
- **Standard Neural Network:** Architecture with layers of 784, 800, 800 neurons, using sigmoid and softmax activations.
- **Dropout Neural Networks:** Dropout models with logistic and ReLU activation functions, as shown in Tables 1 and 2.

### 3.2 Datasets
- **MNIST Dataset:** 60,000 training examples and 10,000 test examples. We used an 80/20 split for training and testing, respectively.

### 3.3 Hyperparameters
- Used fixed hyperparameters from the original paper.
- **Epochs:** Limited to 100 epochs due to Google Colab constraints.
- **Optimizers:** Chose Adam and SGD based on effectiveness.

## 4. Results
### 4.1 Reproducing Original Paper
- **Claim 1:** Our dropout NN model achieved a 1.47% error (logistic units) and 1.42% error (ReLU) compared to the original 1.35% and 1.25%.
- **Claim 2:** Dropout with max-norm regularization resulted in the lowest error of 1.36%, closely aligning with the paper's reported 1.05%.
- **Claim 3:** We evaluated different dataset sizes, confirming the paper's claim that larger datasets benefit more from dropout.

## 5. Discussion
### 5.1 What Was Easy
- Replicating models and processing the MNIST dataset was straightforward given our familiarity with neural networks.

### 5.2 What Was Difficult
- Incompatibility with Python 2.0 required rebuilding the model in Python 3, which led to some deviations in results.

## 6. Conclusion
This study validates dropout as an effective regularization technique, reducing overfitting and enhancing generalization.

## 7. Statement of Contributions
- **Carl:** Reproduced Claims 1 and 2, corresponding code, and result write-ups.
- **Yongru:** Reproduced Claim 3 and completed the rest of the write-up.


**The Full Report can be found in the repository. 
**

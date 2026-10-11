# Fake News Detection

A deep-learning project that classifies news articles as **Fake** or **Real** using TensorFlow and Keras. The project uses a Kaggle fake news dataset and evaluates model performance through accuracy, loss, a classification report, and a confusion matrix.

## Overview

The spread of misinformation makes it increasingly important to analyze the credibility of news content. This project explores a deep-learning-based approach to binary fake news classification.

The model is trained and evaluated using labeled news data. Its performance is measured using classification metrics to assess how accurately it distinguishes fake news from real news.

### Key Features

- Binary classification of news articles: Fake or Real
- Deep-learning model implemented using TensorFlow and Keras
- Kaggle fake news dataset
- Training and evaluation through a Jupyter Notebook
- Performance evaluation using accuracy and loss
- Class-wise precision, recall, and F1-score
- Confusion matrix analysis

## Tech Stack

- **Language:** Python
- **Deep Learning:** TensorFlow / Keras
- **Dataset:** Kaggle fake news dataset
- **Development Environment:** Jupyter Notebook

## Dataset

The project uses a Kaggle fake news dataset containing news examples labeled as Fake or Real.

The data is used to train the classifier and evaluate its performance on a held-out test set.

| Property | Details |
|---|---|
| Dataset source | Kaggle |
| Task | Binary text classification |
| Classes | Fake, Real |
| Test-set support | 8,980 samples |
| Development environment | Jupyter Notebook |

The exact dataset filename, preprocessing configuration, and train/test split procedure are not specified in this README.

## Methodology

The project follows a supervised deep-learning workflow:

1. **Load the dataset:** Load the labeled fake and real news examples.
2. **Prepare the data:** Prepare the dataset for the model using the preprocessing implemented in the notebook.
3. **Train the model:** Train the TensorFlow/Keras model on the training data.
4. **Evaluate performance:** Measure classification performance on the test data.
5. **Analyze predictions:** Use the classification report and confusion matrix to examine correct predictions and misclassifications.

The current implementation is notebook-based and evaluates news data from the dataset rather than providing a standalone web application or API.

## Results

### Model Performance

| Metric | Result |
|---|---:|
| Training accuracy | 99.70% |
| Training loss | 0.0145 |
| Test accuracy from confusion matrix | **99.62%** |
| Logged evaluation accuracy | 99.55% |
| Logged evaluation loss | 0.0237 |

**Accuracy calculation:** The confusion matrix contains 4,672 correctly classified fake articles and 4,274 correctly classified real articles, out of 8,980 test examples.

\[
\text{Accuracy} = \frac{4672 + 4274}{8980} \times 100 \approx 99.62\%
\]

The logged evaluation accuracy differs slightly from the accuracy calculated from the confusion matrix. Both reported values are retained here to make that discrepancy transparent.

### Classification Report

| Class | Precision | Recall | F1-score | Support |
|---|---:|---:|---:|---:|
| Fake | 1.00 | 0.99 | 1.00 | 4,696 |
| Real | 0.99 | 1.00 | 1.00 | 4,284 |
| **Macro average** | **1.00** | **1.00** | **1.00** | **8,980** |
| **Weighted average** | **1.00** | **1.00** | **1.00** | **8,980** |

*Note: The classification report values are rounded to two decimal places. They should not be interpreted as exact 100% performance.*

### Confusion Matrix

Rows represent actual labels and columns represent predicted labels, using the class order Fake, Real.

| Actual / Predicted | Fake | Real |
|---|---:|---:|
| Fake | 4,672 | 24 |
| Real | 10 | 4,274 |

The model correctly classified most examples in both classes. It misclassified 24 fake examples as real and 10 real examples as fake.

These results indicate strong performance on the evaluated test set. However, performance on other datasets or current real-world news may differ.

## Limitations

- **Dataset dependence:** Results depend on the dataset's source, quality, and label definitions.
- **Generalization:** High test accuracy does not guarantee reliable predictions on news from unfamiliar publishers, topics, or time periods.
- **Potential data leakage:** The dataset split and preprocessing should be checked to ensure that information from the test set does not influence training.
- **Changing news patterns:** Language, writing styles, and misinformation techniques change over time.
- **Limited interface:** The current implementation is notebook-based and does not provide a confirmed standalone news-input interface.

## Future Improvements

Potential directions for improvement include:

- Evaluating the model on an independent dataset from a different source.
- Checking for duplicates and data leakage across dataset partitions.
- Testing performance on more recent news articles.
- Examining false positives and false negatives in greater detail.
- Documenting the model architecture and preprocessing pipeline.
- Developing an interface for entering news text and viewing predictions.
- Adding model explainability or evidence-based credibility signals.

## Learning Outcomes

This project provides practical experience with:

- Supervised text classification
- Deep-learning workflows using TensorFlow and Keras
- Binary classification metrics
- Confusion matrix interpretation
- Model evaluation and error analysis
- The limitations of dataset-based fake news detection

## Author

**Punyam Gupta**

GitHub: [@Punyam22](https://github.com/Punyam22)

## Repository

[Fake News Detection on GitHub](https://github.com/Punyam22/Fake-news-detection)

---

This project explores the application of deep learning to fake news classification and evaluates the model using quantitative classification metrics.

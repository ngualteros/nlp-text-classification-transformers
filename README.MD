
# NLP Text Classification — Neural Networks vs. Transformers

## Overview

This project explores multiclass text classification using two deep learning approaches: a classical neural network and a Transformer-based architecture.

Developed as part of my Master's degree in Artificial Intelligence at Universidad Internacional de La Rioja (UNIR), the project covers text preprocessing, tokenization, word embeddings, neural network development, model training, validation, and text predictions.

The main objective is to explore different neural network architectures for automatically categorizing text documents.

## Technologies

- Python
- TensorFlow
- Keras
- NumPy
- Jupyter Notebook
- Natural Language Processing (NLP)
- Deep Learning
- Word Embeddings
- Transformers
- Multi-Head Attention

## Dataset

The project uses the **20 Newsgroups Dataset**, a text classification dataset containing documents organized into 20 topic categories.

Dataset source:
https://www.cs.cmu.edu/afs/cs.cmu.edu/project/theo-20/www/data/

The notebooks download the dataset using Keras utilities.

The dataset includes topics related to technology, politics, religion, science, and other discussion categories.

## Project Structure

```text
nlp-text-classification-transformers/
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   ├── 01_classical_neural_network.ipynb
│   └── 02_transformer_classifier.ipynb
│
└── results/
    └── model_comparison.md
```

## Methodology

### 1. Data Preparation

- Download and explore the 20 Newsgroups dataset.
- Load text documents and their corresponding labels.
- Prepare text samples for classification.
- Shuffle the dataset using a fixed random seed.
- Split the dataset into training and validation subsets.

### 2. Text Vectorization

Text is transformed into numerical representations using Keras `TextVectorization`.

Configuration:
- Maximum vocabulary size: 20,000 tokens.
- Sequence length: 200 tokens.

These representations are used as inputs for both neural network architectures.

### 3. Classical Neural Network

The first model uses a sequential neural network architecture.

Main components:
- Embedding layer.
- Flatten layer.
- Dense hidden layer with ReLU activation.
- Dropout regularization.
- Softmax output layer for multiclass classification.

The model is trained using sparse categorical cross-entropy and RMSprop optimization.

### 4. Transformer-Based Model

The second approach implements a Transformer-based text classifier using TensorFlow and Keras.

Main components:
- Token embeddings.
- Positional embeddings.
- Multi-head self-attention.
- Feed-forward neural network.
- Layer normalization.
- Dropout regularization.
- Global average pooling.
- Softmax classification layer.

The Transformer architecture is implemented using custom Keras layers rather than fine-tuning a pretrained language model.

### 5. Model Training

Both notebooks configure training with:

- 20 epochs.
- Batch size: 128.
- Training and validation datasets.
- Classification accuracy monitoring.

### 6. Predictions

Both models are used to predict the category of example text inputs.

The notebooks demonstrate the end-to-end workflow from raw text to predicted document category.

## Model Evaluation

The original academic notebooks include training and validation accuracy.

A more complete comparative evaluation using an independent test dataset, macro-F1 score, and confusion matrices is planned as a future improvement.

No additional performance results are claimed until they have been reproduced and verified.

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/nlp-text-classification-transformers.git
cd nlp-text-classification-transformers
```

Create a Python virtual environment:

```bash
python -m venv .venv
```

Activate the environment on Windows:

```powershell
.\.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open the notebooks inside the `notebooks/` directory and execute the cells sequentially.

Note: TensorFlow/Keras compatibility and dataset availability should be verified in the target environment before considering the project fully reproducible.

## Future Improvements

- Evaluate both models using an independent test dataset.
- Calculate precision, recall, and macro-F1 scores.
- Generate confusion matrices.
- Compare training performance and generalization.
- Improve code organization and reproducibility.
- Experiment with additional model architectures.

## Academic Context

This project was developed as part of the Natural Language Processing coursework of the Master's in Artificial Intelligence at UNIR.

The activities were based in part on educational notebook material associated with François Chollet and Keras. The repository documents academic implementations and exercises rather than claiming the original invention of the underlying architectures.

## Author

**Nicolás Gualteros Pérez**

Systems Engineer | Master's in Artificial Intelligence

AI Engineering | Machine Learning | NLP | AI Automation

LinkedIn: https://www.linkedin.com/in/nicogualteros

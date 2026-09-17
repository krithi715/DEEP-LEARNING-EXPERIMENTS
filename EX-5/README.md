# Tiny Shakespeare Text Generation Using RNN

## 1. Project Overview

This project implements a **Simple Recurrent Neural Network (RNN)** for next-word prediction and text generation using the **Tiny Shakespeare dataset**.

The model learns word patterns from Shakespeare's text and generates new text based on a given seed word or sentence.

## 2. Objectives

* Load and explore the Tiny Shakespeare dataset.
* Convert text into lowercase.
* Tokenize the text into individual words.
* Create a vocabulary and assign integer values to words.
* Generate input sequences for next-word prediction.
* Apply padding to the sequences.
* Split the dataset into training and validation sets.
* Build a Simple RNN model.
* Train and evaluate the model.
* Generate text using different seed inputs.

## 3. Dataset

**Dataset:** Tiny Shakespeare

The Tiny Shakespeare dataset contains text from the works of William Shakespeare.

The text is converted into lowercase and tokenized into individual words before being used for model training.

## 4. Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* Hugging Face Datasets
* Google Colab / Jupyter Notebook

## 5. Model Architecture

The model consists of the following layers:

```text
Input Sequence
      |
      v
Embedding Layer
      |
      v
Simple RNN Layer
      |
      v
Dense Layer with Softmax
      |
      v
Next Word Prediction
```

### Embedding Layer

The Embedding layer converts each word into a numerical vector representation.

### Simple RNN Layer

The Simple RNN layer learns patterns and relationships between words in the sequence.

### Dense Layer

The Dense layer with Softmax activation predicts the next word from the available vocabulary.

## 6. Data Preprocessing

The following preprocessing steps are performed:

1. Load the Tiny Shakespeare dataset.
2. Explore the text samples.
3. Convert the text to lowercase.
4. Tokenize the text into words.
5. Create a vocabulary.
6. Convert words into integer sequences.
7. Generate input and target sequences.
8. Apply padding to make sequences equal in length.
9. Split the data into training and validation sets.

## 7. Model Training

The model is compiled using:

* **Optimizer:** Adam
* **Loss Function:** Sparse Categorical Cross-Entropy
* **Evaluation Metric:** Accuracy

The dataset is divided into:

* **80% Training Data**
* **20% Validation Data**

The model is trained for multiple epochs to learn word patterns from the dataset.

## 8. Performance Evaluation

The model performance is evaluated using:

* Training Accuracy
* Validation Accuracy
* Training Loss
* Validation Loss

The following graphs are generated:

* Accuracy vs Epoch
* Loss vs Epoch

These graphs are used to observe the learning performance of the model during training.

## 9. Text Generation

After training, a seed word or sentence is provided as input to the model.

For example:

```text
Seed: "to be or not"
```

The model predicts the next word and repeatedly uses the predicted words to generate new text.

Multiple seed inputs are used to observe how the generated text changes based on the initial input.

## 10. Observations

* The RNN learns basic word patterns from the Shakespeare dataset.
* The model can predict the next word based on previous words.
* The generated text shows patterns similar to the training text.
* Some generated sentences may not be grammatically correct.
* A Simple RNN may have difficulty remembering information from very long sequences.
* The quality of generated text depends on factors such as training epochs and sequence length.

## 11. Project Structure

```text
Tiny-Shakespeare-RNN/
│
├── Tiny_Shakespeare_RNN.ipynb
├── README.md
│
└── screenshots/
    ├── dataset.png
    ├── model_summary.png
    ├── training.png
    ├── accuracy.png
    ├── loss.png
    └── generated_text.png
```

## 12. Student Details

**Name:** Krithika K
**Roll No:** 24BAD061
**Department:** Artificial Intelligence and Data Science
**Institution:** Kumaraguru College of Technology

## 13. Result

A Simple RNN-based next-word prediction and text generation model was successfully implemented using the Tiny Shakespeare dataset. The model was trained and evaluated using training and validation data, and text was generated using different seed inputs.


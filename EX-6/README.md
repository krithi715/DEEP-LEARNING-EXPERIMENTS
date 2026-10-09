
# LSTM-Based Sentiment Analysis

## 1. Aim

To implement a Long Short-Term Memory (LSTM) neural network for sentiment analysis and classify movie reviews as positive or negative based on learned linguistic patterns.

## 2. Objectives

* Understand the architecture and working of LSTM networks.
* Perform text preprocessing and tokenization.
* Convert textual data into numerical sequences.
* Build and train an LSTM-based sentiment classification model.
* Evaluate model performance using classification metrics.
* Predict sentiments for new movie reviews.
* Analyze the model's ability to learn contextual and sequential patterns.

## 3. Technologies Used

* Python
* TensorFlow and Keras
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* TensorFlow Datasets
* Google Colab
* GitHub

## 4. Dataset

The IMDB Movie Reviews dataset is used for sentiment classification.

* **Training dataset:** 25,000 reviews
* **Testing dataset:** 25,000 reviews
* **Sentiment classes:** Positive and Negative
* **Labels:** 0 represents Negative and 1 represents Positive

The training dataset is further divided into training and validation sets.

## 5. Methodology

### Part A: Dataset Preparation

1. Load the IMDB Movie Reviews dataset.
2. Explore sample reviews and sentiment labels.
3. Examine the distribution of positive and negative reviews.
4. Convert text to lowercase and remove punctuation.
5. Tokenize the reviews and build a vocabulary.
6. Convert text into numerical sequences.
7. Apply sequence padding to maintain a fixed length of 200 tokens.
8. Split the training data into training and validation sets.

### Part B: LSTM Model Implementation

The model consists of the following layers:

| Layer     | Description                                                     |
| --------- | --------------------------------------------------------------- |
| Embedding | Converts word IDs into dense vectors of 64 dimensions           |
| LSTM      | Learns sequential patterns using 64 units                       |
| Dense     | Produces a binary sentiment prediction using sigmoid activation |

The model is compiled using the Adam optimizer, binary cross-entropy loss, and accuracy as an evaluation metric.

### Part C: Model Training and Evaluation

The model is trained for 5 epochs with a batch size of 64.

The following evaluation metrics are calculated:

* Accuracy
* Precision
* Recall
* F1-score
* Test loss

A confusion matrix is generated to analyze classification errors. Training and validation accuracy and loss are plotted against epochs.

### Part D: Sentiment Prediction

New movie reviews are provided as input to the trained model. The same vocabulary and preprocessing method are used to convert the reviews into numerical sequences.

The model predicts a probability, which is converted into a Positive or Negative sentiment label using a threshold of 0.5. Predicted labels are compared with expected sentiments, and the observations are documented.

## 6. Model Architecture

```text
Input Movie Reviews
        |
        v
Text Preprocessing
        |
        v
Tokenization and Padding
        |
        v
Embedding Layer
(64-dimensional vectors)
        |
        v
LSTM Layer
(64 units)
        |
        v
Dense Layer
(Sigmoid Activation)
        |
        v
Positive / Negative
Sentiment Prediction
```

## 7. Evaluation Metrics

**Accuracy:** Measures the proportion of correctly classified reviews.

**Precision:** Measures how many reviews predicted as positive are actually positive.

**Recall:** Measures how many actual positive reviews are correctly identified.

**F1-score:** Represents the harmonic mean of precision and recall.

**Confusion Matrix:** Shows true positives, true negatives, false positives, and false negatives.

The actual metric values are recorded from the notebook after training and evaluation.

## 8. Results and Observations

* Textual reviews are converted into numerical sequences suitable for LSTM processing.
* The Embedding layer learns dense word representations.
* The LSTM layer learns sequential and contextual patterns from movie reviews.
* Training and validation curves help monitor model learning and identify possible overfitting.
* The confusion matrix and classification metrics help evaluate prediction performance.
* New reviews are classified as positive or negative based on their predicted probabilities.
* Neutral reviews cannot be directly classified as a separate category because the model is trained for binary classification.

## 9. Advantages of LSTM

* Learns relationships between words in sequential text.
* Retains important information across multiple time steps.
* Helps address the vanishing gradient problem associated with Simple RNNs.
* Supports sentiment analysis and other natural language processing tasks.

## 10. Conclusion

The LSTM-based sentiment analysis model demonstrates how deep learning can be used to classify movie reviews. Text preprocessing, tokenization, numerical representation, and sequence padding prepare the data for training. The trained model is evaluated using classification metrics and a confusion matrix, and it is tested on new reviews to analyze its sentiment prediction capabilities.


## 12. Future Improvements

* Experiment with different sequence lengths and embedding dimensions.
* Compare LSTM performance with Simple RNN and GRU models.
* Tune the number of epochs and LSTM units.
* Extend the model to classify positive, negative, and neutral sentiments.
* Use dropout and other regularization techniques to reduce overfitting.

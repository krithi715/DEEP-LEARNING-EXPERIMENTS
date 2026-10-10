# Text Preprocessing and Word Embedding Generation Using Word2Vec

## Aim
To perform text preprocessing using NLTK and generate word embeddings using Gensim Word2Vec to analyze semantic relationships and word similarity.

## Objectives
- Perform text preprocessing using NLTK.
- Generate vocabulary and analyze word frequencies.
- Train a Word2Vec model using the Skip-gram architecture.
- Generate 100-dimensional word embeddings.
- Calculate cosine similarity between word pairs.
- Analyze semantic relationships between words.

## Software Requirements
- Python
- Google Colab
- NLTK
- Gensim
- NumPy
- Matplotlib
- GitHub

## Dataset
The Brown Corpus available through NLTK is used for text processing. The `news` category is selected for analysis.

## Methodology

### Part A: Dataset Preparation and Text Preprocessing
- Load the Brown Corpus.
- Convert text into lowercase.
- Perform word tokenization.
- Remove punctuation and stop words.
- Apply lemmatization using `WordNetLemmatizer`.
- Display original and preprocessed text.

### Part B: Vocabulary Generation and Word Frequency Analysis
- Create a vocabulary from preprocessed text.
- Calculate word frequencies using NLTK's `FreqDist`.
- Identify the ten most frequent words.
- Display vocabulary size and frequency distribution.
- Prepare tokenized sentences for Word2Vec training.

### Part C: Word Embedding Generation Using Word2Vec
- Train a Word2Vec Skip-gram model using Gensim.
- Set the embedding dimension to 100.
- Set the context-window size to 5.
- Generate and display word embedding vectors.
- Identify the five most similar words for a selected word.

### Part D: Word Similarity Analysis
- Select three word pairs from the vocabulary.
- Calculate cosine similarity scores.
- Compare scores and identify the most similar pair.
- Visualize similarity scores using a bar chart.
- Analyze the relationship between contextual similarity and word embeddings.

## Word2Vec Parameters

| Parameter | Value |
|---|---|
| Architecture | Skip-gram |
| Vector size | 100 |
| Context window | 5 |
| Minimum word count | 2 |
| Training epochs | 10 |

## Results and Observations
- Text preprocessing reduces noise and standardizes text.
- Stop-word removal and lemmatization help reduce unnecessary vocabulary variations.
- Word frequency analysis identifies commonly occurring words.
- Word2Vec represents words as dense numerical vectors.
- Cosine similarity measures the directional similarity between word vectors.
- Words used in similar contexts may have higher similarity scores.

The actual similarity scores and most similar word pairs depend on the trained model.

## Conclusion
The experiment demonstrates text preprocessing, vocabulary generation, word frequency analysis, and word embedding generation using NLTK and Gensim. The trained Word2Vec model is used to analyze semantic relationships between words through cosine similarity.


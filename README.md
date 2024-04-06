# Phishing Link Detection Model

This repository contains a machine learning model for detecting phishing links using logistic regression. The model is trained on a dataset of approximately 600,000 links, labeled as either 'Safe Link' or 'Phish Link'.

## Dataset

The dataset consists of two columns:

1. **Safe Link**: URLs that are safe and legitimate.
2. **Phish Link**: URLs that are suspected to be phishing links.

## Preprocessing

To preprocess the data, we employ Natural Language Processing (NLP) techniques and tokenization. Here's an overview of the process:

1. Import the necessary libraries, including NLP libraries like NLTK or spaCy.
2. Load the dataset into a pandas DataFrame.
3. Define a function to preprocess the links by separating the words from the text using tokenization techniques. This step is crucial because words in URLs can be important features for identifying phishing links.
4. Tokenize the URLs by splitting them into individual words or tokens using regular expressions or specialized tokenizers from NLP libraries. This step helps extract meaningful features from the URLs, such as domain names, subdomains, and specific keywords or patterns.
5. After tokenization, vectorize the URLs by converting them into numerical representations that can be fed into the machine learning model. This can be done using techniques like TF-IDF (Term Frequency-Inverse Document Frequency) or word embeddings (e.g., Word2Vec or GloVe).

## Model Training

1. Once the data is preprocessed and vectorized, split it into training and testing sets.
2. Train a logistic regression model on the training data, using the vectorized URLs as input features and the corresponding labels ('Safe Link' or 'Phish Link') as target variables.
3. Evaluate the model's performance on the test set using appropriate metrics.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

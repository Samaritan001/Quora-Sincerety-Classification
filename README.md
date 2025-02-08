# Quora-Sincerety-Classification
## Dataset
The dataset comes from Kaggle Competition Nov. 2018 "Quora Insincere Questions Classification".\
Dataset contains only 1 file train.csv with labeled question-sincerety pair.\
Labels are 0's and 1's, proposing a binary classification problem.\
https://www.kaggle.com/competitions/quora-insincere-questions-classification

## Word Embedding
### NLPL
The word embedding used in the model is NLPL Word Embedding Repository.\
https://vectors.nlpl.eu/repository/
### nn.Embedding
Can also use nn.Embedding to train the embedding along with the LSTM model, which increases approximately 8% in testing.\
self.embedding_layer = nn.Embedding(vocab_size+2, embedding_dim)

## LSTM Model
The NLP Classification problem is solved using bidirectional multi-layer LSTM model and is trained in PyTorch.\
The training is done on Google Colab, and the highest evaluation accuracy has reached 93.78%

## Google Chrome Extension: Quora Question Classifier
The Google Chrome Extension is built in JavaScript (HTML+CSS).\
The extension is a web application interface of the classification model. When the extension is running, it extracts the Quora question automatically from a Quora page and process the model locally to generate a real-time judgement upon the sincerety of the question.

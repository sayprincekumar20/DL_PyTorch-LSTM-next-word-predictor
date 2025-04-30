# DL_PyTorch-LSTM-next-word-predictor

PyTorch LSTM Next Word Predictor
================================

This project demonstrates how to build and train a next-word prediction model using an LSTM neural network in PyTorch. 
The model learns from a given text corpus and predicts the most likely next word in a sequence.

Project Overview
----------------
- Task: Predict the next word based on a sequence of previous words.
- Framework: PyTorch
- Techniques Used: LSTM (Long Short-Term Memory), Tokenization, Text Preprocessing

Key Concepts
------------
- Text Tokenization: Using nltk.word_tokenize() to split text into individual tokens (words).
- Vocabulary Building: Creating word-to-index and index-to-word mappings.
- Dataset Creation: Generating input-target sequences for the model.
- Model Architecture:
    * Embedding Layer
    * LSTM Layer
    * Fully Connected (Linear) Output Layer
- Training Loop:
    * Loss Function: CrossEntropyLoss
    * Optimizer: Adam
- Inference: Given a few words, predict the next likely word.

Installation & Requirements
---------------------------
Install required libraries:
    pip install torch nltk

Example Input Text
------------------
The text used for training comes from a passage in a Sherlock Holmes story, like:

"To Sherlock Holmes she is always the woman. I have seldom heard him mention her under any other name..."

This corpus is used to train the model to predict continuations of sentences.

Example Usage
-------------
After training, you can run:

    predict("To Sherlock Holmes")

And get output like:

    ['she']

Training Parameters
-------------------
- Epochs: e.g., 100
- Batch size: e.g., 32
- Sequence Length: 3
- Embedding Dim: 10
- Hidden Dim: 128

Files in the Project
--------------------
pytorch_lstm_next_word_predictor.ipynb : Full notebook with model, training, and testing
README.txt                            : Notes and documentation (this file)

Future Improvements
-------------------
- Add support for longer sequences and beam search
- Include punctuation handling and better token normalization
- Save and load trained models for reuse

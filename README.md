# Introduction

This repository contains code for performing part-of-speech (POS) tagging on the Penn Treebank dataset. The code is
written in Python and uses the PTBPosLoader class for loading and preprocessing the dataset, the Viterbi algorithm
implemented in the POSTagger class for POS tagging, and the RecurrentPOSTagger class for performing POS tagging using a
recurrent neural network. The code also includes functionality for exploring the dataset and evaluating different
models.

## Penn Treebank Dataset

The Penn Treebank dataset is a widely used corpus of English text consisting of over 4 million words, annotated with
part-of-speech tags. The dataset is commonly used for training and evaluating models for natural language processing
tasks such as POS tagging.

## Viterbi Algorithm

The Viterbi algorithm is a dynamic programming algorithm used for finding the most likely sequence of hidden states in a
hidden Markov model (HMM). In the context of POS tagging, the Viterbi algorithm is used to find the most likely sequence
of part-of-speech tags given a sequence of words.

The algorithm works by recursively computing the probability of each possible tag sequence ending in a given tag at each
position in the sentence. The most likely tag sequence is then found by backtracking through the best tag sequences at
each position.

## Summary of Classes

- ### PTBPosLoader Class

    The `PTBPosLoader` class is designed for loading and preprocessing the Penn Treebank Part of Speech (POS) dataset. It
provides functionality to split the dataset into training, validation, and testing sets, as well as extract word-tag
pairs from these sets. The class also offers methods to retrieve the vocabulary and tag set of the training set, as well
as access to the individual sets.

- ### POSTagger Class

    The `POSTagger` class implements the Viterbi algorithm for POS tagging using the Penn Treebank dataset. The class takes
in an instance of the `PTBPosLoader` class and provides methods to set up the transition and emission matrices based on
the training set, apply the Viterbi algorithm for tagging, and evaluate the accuracy of the tagging results.
Additionally, the class includes functionality for handling out-of-vocabulary words with smoothing and saving/loading
the emission matrix to/from a CSV file.

- ### RecurrentPOSTagger Class

    The `RecurrentPOSTagger` class is a Python class that can be used to perform part-of-speech (POS) tagging using a
recurrent neural network. The class offers methods to prepare the data for training and testing, build the recurrent
neural network model, train the model using the training set, predict the POS tags for the input data, and evaluate the
accuracy of the model on the test data.

# Conclusion

The code provided in this repository offers functionality for loading, preprocessing, and exploring the Penn Treebank
dataset, as well as implementing the Viterbi algorithm and a recurrent neural network for performing POS tagging.
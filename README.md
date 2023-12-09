Overview

The goal of this project is to develop machine and mostly deep learning models to classify utterances in professional dialogues. It is a binary classification on whether the utterance is important or not.


Table of Contents

Project Structure
Usage
Data
Models
Evaluation


Project Structure

- /test: Contains dialogue datasets for the testing with the graph structure in the TXT files and the utterances in the JSON files.
- /training: Contains dialogue datasets for the training with the graph structure in the TXT files and the utterances in the JSON files.
- /.: Contains: - the labels for the utterances of the training dialogues;
                - the scripts for the feature extractions, data processing, models training and testing, results shaping for submission;
                - the pre-trained models from the scripts that produce good results.


Installation

In the beginning of each notebook, the list of required libraries is provided in the first cell where they are imported.


Usage

Every jupyter notebook is independent from the others. In each notebook, you have:
1) The imports of the required libraries
2) The feature extraction
3) The feature reshaping depending on the model used
4) The tokenization of the text
5) The batching of the inputs
6) The description of the model
7) The definition of the hyperparameters and the training
8) The evaluation of the testing datasets

You can execute these different cells in this order and you will get our results.


Data

For the different dialogue datasets, we have a JSON files with the utterances, their speaker and index in the dialogue. Additionally, we have a TXT file describing the graph structure of the dialogue. The utterances are the nodes described by their index and the edges are categorical variables explaining the relationships between the utterances.


Models

We have 4 jupyter notebooks:
- jupyter_ML_model : One is about classic machine learning models such as RandomForest or SVM.
- jupyter_best_f1 : One contains our deep learning models giving the best results. They use various neural networks.
- jupyter_pretrained_embedding : One also develops neural networks but with other data embedding steps.
- jupyter_GNN : One develops a graph neural network.


Evaluation

Firstly, we divided the training set into a train set and a validation set to get intermediary results during the training step and to approximate the results we might have on the testing set.
During the numerous epochs of the training step, we used the loss and F1-score of the validation set.
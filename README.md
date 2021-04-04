# COVID-19 Cough Classification using PyTorch

## Overview

The aim of this project is to classify audio recordings of coughs into COVID-19 positive and negative.

## Installation

### Install required libraries

```
pip install -r requirements.txt
```

### Download dataset from kaggle

The dataset used for training and evaluation can be found on kaggle:
https://www.kaggle.com/himanshu007121/coughclassifier-trial
Download and extract the content of the zip file into the ./data/ directory.

## Running the code

The code is split into three notebooks:

1. 001_prepare_data.ipynb: This notebook extracts the features of the wav files and writes them to a new csv file.
2. 002_training.ipynb: Trains and evaluates the CoughNet using the extracted features. Finally a checkpoint is saved.
3. 003_inference.ipynb: Uses the saved checkpoint to predict on an input wav file. There is also a pretrained checkpoint available.

## Results

The complete dataset is divided into a train (67%) and test (33%) subset.
The model converges after 15 epochs of training.

| Results  | Training |  Test |
| -------- | -------: | ----: |
| Accuracy |     100% | 94.7% |

## Credits

The PyTorch implementation is based on a Keras notebook by Himanshu which can be found here:
https://www.kaggle.com/himanshu007121/covid-19-cough-classification

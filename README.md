# LSTM and GRU Language Modeling on Penn Treebank

## Overview

This project implements and trains LSTM and GRU models on the Penn Treebank dataset to predict the next word in a sequence. Several regularization techniques are applied to improve model generalization and avoid overfitting. The models compared include:

- **LSTM without Dropout**: A baseline LSTM model with no regularization.
- **LSTM with Dropout**: Dropout applied after the recurrent layers to prevent overfitting.
- **GRU without Dropout**: A baseline GRU model with no regularization.
- **GRU with Dropout**: Dropout applied after the recurrent layers in the GRU.

## Files

The root of the repository is organized as follows:

```
LSTM_GRU_PennTreebank/
│
├── LSTM_GRU_PennTreebank.ipynb        
├── README.md                           
├── LSTM_dropout_0.pth        
├── LSTM_dropout_dot5.pth     
├── GRU_dropout_0.pth          
├── GRU_dropout_dot5.pth    
├── .git/                             
├── data/                            
│   ├── ptb.train.txt
│   ├── ptb.valid.txt
│   ├── ptb.test.txt
```

### File Descriptions

- **LSTM_GRU_PennTreebank.ipynb**: The main notebook containing the implementation of LSTM and GRU models, training routines, and analysis of results. This notebook is organized into the following sections:

  1. **Load and preprocess the dataset**: 
     - Prepares the Penn Treebank dataset for training and evaluation. The data is loaded, tokenized, and converted into sequences of word-level tokens.

  2. **Create Dataset and Dataloader**: 
     - Sets up the `Dataset` and `DataLoader` classes to efficiently load and batch the dataset for training, validation, and testing.

  3. **Define the LSTM and GRU Models**: 
     - Implements the LSTM and GRU models.

  4. **Training and Validation Functions**: 
     - Contains functions for training the models and calculating perplexity on the validation set. 

  5. **Training the Models**: 
     - Trains the LSTM and GRU models with and without dropout, comparing the results after each epoch.

  6. **Test with Saved Weights**: 
     - Provides code to load pre-trained models (with and without dropout) and test them on the validation or test sets using saved weights.

## How to Run

To run the notebook and reproduce the results:

**Run the notebook**:
   - Open `LSTM_GRU_PennTreebank.ipynb` in Jupyter or Google Colab.
   - Follow the steps in the notebook to run each experiment.

### Steps:

1. **Data Preparation And Model Definition**:
   - Run the cells under the first 4 section to preprocess the Penn Treebank dataset and define the RNN models. That is from section "Load and preprocess the dataset" to "Training and Validation Functions".

2. **Test With Saved Weights**:
   - To test with the pre-trained models (without re-training), run all cells under "Test with saved weights" sections to load weights from ".pth" files and then do the testing.

3. **If you want to train your own models and save weights**:
    - Run all cells under "Training the Models" sections.


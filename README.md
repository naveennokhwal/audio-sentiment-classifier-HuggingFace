## Overview

This repository contains code and resources for testing a Hugging Face model on two different datasets for speech emotion detection. The model was evaluated using the Shemo Persian Speech Emotion Detection Database and the RAVDESS Emotional Speech Audio dataset. The core code is written in two Jupyter Notebook files: `main.ipynb` and `newdataset_model.ipynb`.

## Datasets

1. **Shemo Persian Speech Emotion Detection Database**  
   - **Source**: [Kaggle](https://www.kaggle.com/datasets/mansourehk/shemo-persian-speech-emotion-detection-database/data)  
   - This dataset is used for training the model and includes various emotional speech samples in Persian.

2. **RAVDESS Emotional Speech Audio**  
   - **Source**: [Kaggle](https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio)  
   - This dataset contains emotional speech recordings in English, providing a different linguistic context for model evaluation.

## Code Structure

The code is organized in two main Jupyter Notebook files:

1. **`main.ipynb`**  
   - This notebook is used for evaluating the Shemo dataset.
   - It includes code for handling the dataset, making predictions using the model, and evaluating the results.

2. **`newdataset_model.ipynb`**  
   - This notebook is used for evaluating the RAVDESS dataset.
   - It contains separate code for handling the RAVDESS dataset, making predictions, and evaluating the results.

The `src` folder contains two files referenced from the original GitHub repository of the model used. These files are used to support the Hugging Face model functionality.

## Model
The Hugging Face model used in this project is: m3hrdadfi/hubert-base-persian-speech-emotion-recognition. This pre-trained model is used for emotion recognition in Persian speech using the HuBERT architecture.

## Results

The results obtained from testing the model on both datasets are as follows:

- **Shemo Dataset Results**:
- for female audio: 
|    Emotions   | precision | recall | f1-score | accuracy     |
|:-------------:|:---------:|:------:|:--------:|:------------:|
|   Anger       |   0.98    |   1.0  |   0.99   |     0.98     |
|   Fear        |   0.59    |   1.0  |   0.74   |     0.59     |
|   Hapiness    |   0.94    |   1.0  |   0.97   |     0.94     |
|   Neutral     |   0.99    |   1.0  |   1.0    |     0.99     |
|   Sadness     |   0.85    |   1.0  |   0.92   |     0.85     |
|   Surprise    |   0.87    |   1.0  |   0.93   |     0.87     |

-for male audio:
|    Emotions   | precision | recall | f1-score | accuracy     |
|:-------------:|:---------:|:------:|:--------:|:------------:|
|   Anger       |   0.97    |   1.0  |   0.99   |     0.97     |
|   Fear        |   0.69    |   1.0  |   0.81   |     0.69     |
|   Hapiness    |   0.96    |   1.0  |   0.98   |     0.96     |
|   Neutral     |   0.99    |   1.0  |   0.99   |     0.99     |
|   Sadness     |   0.78    |   1.0  |   0.88   |     0.78     |
|   Surprise    |   0.79    |   1.0  |   0.88   |     0.79     |
  
- **RAVDESS Dataset Results**:
|    Emotions   | precision | recall | f1-score | accuracy     |
|:-------------:|:---------:|:------:|:--------:|:------------:|
|   Anger       |   0.92    |   1.0  |   0.96   |     0.92     |
|   Fear        |   0.02    |   1.0  |   0.04   |     0.02     |
|   Hapiness    |   0.15    |   1.0  |   0.26   |     0.15     |
|   Neutral     |   0.81    |   1.0  |   0.9    |     0.81     |
|   Sadness     |   0.64    |   1.0  |   0.78   |     0.64     |
|   Surprise    |   0.18    |   1.0  |   0.31   |     0.18     |

These results demonstrate the model's performance across different linguistic contexts and emotional expressions.

## Installation

To run the code, ensure you have the following prerequisites installed:

- Python 3.x
- Required libraries: torchaudio, tranformers

You can install the required libraries using pip:

```bash
pip install -r requirements.txt
```
## Usage
To test the model on the Shemo dataset, open and run the main.ipynb notebook.
To test the model on the RAVDESS dataset, open and run the newdataset_model.ipynb notebook.

## Conclusion
This repository showcases the application of Hugging Face models for speech emotion detection using two different datasets. The results obtained provide insights into the model's performance and adaptability to various linguistic contexts.

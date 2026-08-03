# Kaggle NLP with Disaster Tweets - BERTweet

This repository contains my solution for the Kaggle Natural Language Processing with Disaster Tweets competition, where the goal is to classify whether a tweet describes a real disaster or not using a pretrained transformer model.

Competition Link: https://www.kaggle.com/competitions/nlp-getting-started

## Results

| Model | Public Leaderboard |
|-------|-------------------:|
| BERTweet | **0.81397** |

## Project Structure

```
.
├── second_submission_(bertweet).ipynb
├── train.csv
├── test.csv
├── submission.csv
└── README.md
```

## Exploratory Data Analysis

Before training the model, I explored the dataset to better understand the characteristics of the tweets and the target labels.

The analysis includes:

- Distribution of disaster and non-disaster tweets
- Class balance inspection
- Tweet length analysis
- Common words and phrases

## Data Preprocessing

The preprocessing pipeline consists of:

- Splitting the labeled data into training and validation sets
- Tokenizing tweets using the pretrained **BERTweet tokenizer**
- Padding and truncating sequences to a fixed maximum length
- Converting tweets into transformer input tensors
- Creating PyTorch datasets for training and validation

## Model

The model is implemented using Hugging Face's pretrained **BERTweet** transformer model.

Training pipeline:

1. Load the pretrained BERTweet tokenizer
2. Tokenize all tweets
3. Fine-tune the pretrained BERTweet model
4. Evaluate on the validation dataset
5. Generate predictions for the Kaggle test dataset
6. Export predictions as `submission.csv`

## Technologies Used

- Python
- Pandas
- PyTorch
- Hugging Face Transformers
- Scikit-Learn

## Future Improvements

Possible improvements include:

- Hyperparameter optimization
- Learning rate scheduling
- Longer training with early stopping
- K-Fold cross-validation
- Model ensembling
- RoBERTa
- DeBERTa
- Larger BERTweet variants

## Lessons Learned

Through this project I gained practical experience with:

- Transformer-based Natural Language Processing
- BERTweet
- Hugging Face Transformers
- Tokenization
- Fine-tuning pretrained language models
- Binary text classification
- PyTorch training workflow
- Kaggle competition workflow

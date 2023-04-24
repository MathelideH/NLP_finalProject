# NLP_finalProject
Goal: sarcasm detection using trained BERT and distilBERT language models

Datasets: 
1/Traning dataset: 80% of the headlines from Onion(labelled as sarcastic), HuffPuff(labelled as non-sarcastic)
2/Dev dataset: 10% of the same dataset as mentioned above, used to tune hyperparameters (epoch_num and batch_size = 2)
3/In-distribution test: 10% of the same dataset as mentioned above
4/Out-of-distribution test: use Twitter, Reddit datasets


Data Preprocessing:
1/ Pull data from Tweets and Reddits, manually drop posts that are non-sense or contain minimal amount of meaningful content while make sure the number of sarcastic and non-sarcastic tweets are relatively balanced
2/ Preprocessing data by deleting unnecessary information (article link, tag, emoji, etc.)
and storing the data into a csv or excel file in this format: "label 1=sarcastic, 0=non-sarcastic", "data".

Model Training:
1/ Finetuning the simple BERT and distilBERT models




# NLP_finalProject
Goal: sarcasm detection using trained BERT and distilBERT language models

Datasets: 
1/Traning dataset: 80% of the headlines from Onion(labelled as sarcastic), HuffPuff(labelled as non-sarcastic)
2/Dev dataset: 10% of the same dataset as mentioned above, used to tune hyperparameters (epoch_num and batch_size = 2)
3/In-distribution test: 10% of the same dataset as mentioned above
4/Out-of-distribution test: use Twitter, Reddit datasets

Model Training
1/ Finetuning the simple BERT and distilBERT models




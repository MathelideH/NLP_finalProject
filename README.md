# NLP_finalProject
Goal: sarcasm detection using trained BERT and distilBERT language models and a bigram model as baseline.

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
1/ No need to train the bigram model
2/ Finetuning the distilBERT models
   Lambda layer: 1
   Dense layer: 128 nodes, with activation function - relu (1)
   Dropout rate: 0.2
   Output layer: activation function - sigmoid
   Optimizer: Adam, learning rate - 1e-5, loss function - binary_crossentropy, metrics - accuracy
   

Tuning hyperparameters:
1/ With the bigram model, we tried different k values and picked the one that yielded best performance.
2/ The hyperparameters for our DistilBERT model is epochnum = 3, batchsize = 32, and learning rate = 1e-5. Each of us tried running a different combination of these hyperparameters on the dev dataset to 
see which set of hyperparameters yield the best output, then we used that set for the final testing. 


Testing models' performance:

DistilBERT:
  Baseline testing (accuracy): 
    In-distribution:
      News Headlines: 47.45%
    Out-of distribution:
      Reddit: 50.94%
      Tweet: 47.79%
      
  Post-training testing (accuracy):    
    In-distribution:
      News Headlines: 87.84%
    Out-of distribution:
      Reddit: 48.76%
      Tweet: 51.52%




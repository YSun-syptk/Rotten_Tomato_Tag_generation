# Rotten_Tomato_Tag_generation
Utilizing Bert for movie review sentiment analysis and tag generation

## Summary of idea:

We will utilize DistilBert(a smaller version of the common Bert trained using distilled learning) as the base model to be adapted/transferred.  
(The effect of distilled learning vs direct learning is not explored here but could be of future interest).  
We will first explore and find the best way of achieving sentiment prediction with different common ways of transfer learning on a sample movies review dataset available @[here](https://github.com/clairett/pytorch-sentiment-classification/raw/master/data/SST2/train.tsv).     
Then, we will utilize the top-most output states of the decoders as our contextualized word embeddings of each review as input for a downstream word-level sentiment prediction model, which will be receive a polarity label and weight constructed using Vader and Textblob polarity scores.  
We will explore whether or not to add POS tags as input for the model to improve its word level sentiment prediction.   
We then define custom "NOUN-PHRASE" structures to extract the most salient adjective-noun pairs and clauses as summary of the reviews, which will constrast the usage of downstream scores of words (model-identified keywords) to construct different summaries of movie reviews.   
(Another way to go is to merge the two to have weighted sampling of noun phrases based on model scores of keywords and sentences).  

We added a custom movie/show review extraction pipeline for Rotten Tomato scraping using Google search backend and BeautifulSoup for fun of presentation.

Happy NLP exploration, you movie/show lovers!  


## Model used ([DistilBert](https://huggingface.co/transformers/model_doc/distilbert.html) provided by HuggingFace) 
## Notebook 1:  

Exploration of various fine-tuning techniques of transformer model on sample movie sentiment dataset. 
  
(Constrasted with Word2Vec + BiDirectional LSTM).   
  
Exploration of Summarization generation.   
  
Exploration of POS tags and dependency tree generation.  
  
Generation of Word-level sentiment dataset using Bert Embeddings (hidden states from selective heads)
 


## Notebook 2:
Construction of Word-level sentiment prediction model with hyperparameter tunings.
  
Exploration of POS tags for Word embedding improvements (undergoing)
  
Custom-function Web-scraping for movie/show review and label (Rotten Tomato)
  
Word cloud visualization (of Tags) with polarity (POS/NEG sentiments based summaries, custom NOUN PHRASE structure extraction)
  
Word cloud visualization (of Tags) with most important sentiment words (Using word POS tag, attention weights and classifier-based ranking)
  
Construction of Category-based Movies for movie category prediction using tags
  
Link for downloading IMDB dataset:
https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews (merged, csv file)
or
https://ai.stanford.edu/~amaas/data/sentiment/ (pre-merged, individual reviews)

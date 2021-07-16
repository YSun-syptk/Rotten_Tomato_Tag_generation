# Rotten_Tomato_Tag_generation
Utilizing Bert for movie review sentiment analysis and tag generation

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

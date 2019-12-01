# NLP Group Project
## Contributors: Atulya Shetty and Payton Walker

*GitHub Repository for all documents related to NLP final group project.

## Project Description

The aim of this project was to build a sentiment classifier for product reviews using state-of-the-art language models such as BERT and XLNET. The classifiers were trained with data from one domain and evaluated using data from a different domain to identify whether consumers express their sentiments in a similar fashion across different types of products.

## Libraries and Modules

Flair - Embeddings for XLNET

Transformers - For the Pre-trained BERT model 

Keras - To add padding sequences for the BERT model input

Pytorch - For utility classes to load the dataset and setup iterables

Pandas - To read, filter and manipulate the data

scikit-learn - For train/test splits and metric modules

Pickle and Gzip - To store and compress the amazon dataset

 
## Datasets

Amazon - 190k Electronic Reviews

IMDB - 50k Movie Reviews

Yelp - 10k Business Reviews

## Code Structure 
### Development code folder

This folder contains the various model we experimented with before implementing the final models.

### Final Classifiers folder

This folder contains the code for the final classifiers and code used to setup our datasets

### Flair implementation

#### S1_Classifier.ipynb

Train: IMDB

Test: Amazon 
#### S2_Classifier.ipynb

Train: Yelp

Test: Amazon

#### S3_Classifier.ipynb

Train: IMDB+Yelp

Test: Amazon

#### S4_Classifier.ipynb

Train: IMDB+Yelp+Amazon

Test: Amazon

### Transformer implementation 

#### Bert_Transformers.ipynb

Train: Amazon

Test: Amazon, Yelp, IMDB

#### DataLoader.ipynb

Logic to setup the datasets

# NLP Group Project
## Contributors: Atulya Shetty(tuly1, atulya22) and Payton Walker (paytonross).

*GitHub Repository for all documents related to NLP final group project.

## Project Description

The aim of this project was to build a sentiment classifier for product reviews using state-of-the-art language models such as BERT and XLNET. The classifiers were trained with data from one domain and evaluated using data from a different domain to identify whether consumers express their sentiments in a similar fashion across different types of products.

## Libraries and Modules

Flair - Embeddings for XLNET

Transformers (HuggingFace) - For the Pre-trained BERT model 

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

## Results

### Flair

| ID | Train Data           | Test Data | Label              | Accuracy                   | Precision                  | Recall                     | F1-score                   |
|----|----------------------|-----------|--------------------|----------------------------|----------------------------|----------------------------|----------------------------|
| S1 | IMDB (pre-trained)   | Amazon    | -                  | 0.6796                     | 0.6962                     | 0.6374                     | 0.6655                     |
| S2 | Yelp                 | Amazon    | NEG<br>----<br>POS | 0.5475<br>------<br>0.5565 | 0.7170<br>------<br>0.7060 | 0.6984<br>------<br>0.7244 | 0.7076<br>------<br>0.6964 |
| S3 | IMDB + YELP          | AMAZON    | NEG<br>----<br>POS | 0.5343<br>------<br>0.5783 | 0.7474<br>------<br>0.6914 | 0.6520<br>------<br>0.7796 | 0.6964<br>------<br>0.7329 |
| S4 | IMDB + YELP + AMAZON | AMAZON    | NEG<br>---<br>POS  | 0.6143<br>------<br>0.5971 | 0.7415<br>------<br>0.7692 | 0.7818<br>------<br>0.7274 | 0.7611<br>------<br>0.7477 |

### BERT 

| ID | Train Data | Test Data | Accuracy | Precision | Recall | F1-score |
|----|------------|-----------|----------|-----------|--------|----------|
| H1 | Amazon     | Amazon    | 0.8895   | 0.9531    | 0.9030 | 0.9274   |
| H2 | Amazon     | Yelp      | 0.6465   | 0.8641    | 0.6975 | 0.772    |
| H3 | Amazon     | IMDB      | 0.5517   | 0.6353    | 0.698  | 0.665    |

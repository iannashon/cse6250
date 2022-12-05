# CSE6250
## Introduction
This repository is for CSE6259 project. The main objective for this project is to predict the likelihood of readmission for heart failure in patients that have presented to the hospital ICU. We evaluate each hospital admission to predict the risk of the patient being readmitted in two scenarios:  
- 30 day readmission risk  
- Any readmission during the dataset timeframe  
This project aims to replicate findings from X, Liu et al. in 2019 (https://arxiv.org/abs/1912.10306)

## Dependencies
In our project we have used the following dependencies
- Pyspark, pandas
- Keras, sklearn
- Numpy
- Gensim
- Seaborn
- Tensorflow
- word2vec pre trained model by PubMed
## Data
The dataset we are using is MIMIC-3 (Medical Information Mart for Intensive Care III version 1.4) which is a compilation of admissions to the intensive care unit at Beth Israel Deaconess Centre (Boston).The data consists of 58,976 separate hospital admissions between the years 2001 and 2012, involving 46,520 patients.The MIMIC-3 database has 26 tables linked by identifiers. Key identifiers including Subject ID and Hospital admission ID. This enabled linking of the various tables.
## Codes
The project was devceloped using Google Colab notebooks. Those notebooks were exported and committed on this repo. Following is description of each notebook
- Data - This is used to MIMIC-3 data exctraction and preparation, the MIMIC-3 dataset is large so for our case we had to store it to Google drive and link it to our notebook. The final output of this notebook is a clean dataset in csv format.
- CNN - This notebook read outpuut of previous notebook and use to train our CNN model. The same codes can be used for general readmission and 30-days readmission but you have to change target label name while splitting dataset.
- OtherClassifier - This notebook implement the rest of the models we have used in our report to comapare with CNN. We have Random Forest, KNN and SVC.
## How to run the codes
You can run these notebook in google colab or even jupyter notebooks, you have to make sure all dependencies are installed first. Run the notebook in the same order, start with Data then CNN and final OtherClassfier.

CNN model require alot computing power, for our case we used Google Colab Pro plan and also we have added a fuction to control dataset size

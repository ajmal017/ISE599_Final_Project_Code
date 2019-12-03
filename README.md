# ISE599_Final_Project_Code

## 1. Dataset

There are two dataset used in this project. However, both of them are too big to repo. Therefore, we will provide the data link here for you to download.

##### 10K_Files: http://www.cs.cmu.edu/~ark/10K/
##### Kaggle_stock_prices: https://www.kaggle.com/tsaustin/us-historical-stock-prices-with-earnings-data#stock_prices_latest.csv


# Archive Folder 

## 1. All_prices_10k_features

In the All_prices_10k_features folder, it contains the dataset for our final combined features model, which include both 10K contents and Stock price features.

## 2. Data preprocessing

In the Data preprocessing folder, it includes the csv files, and code for our data preparation. We first extract the CIK for each 10K file and tried to match them with right stock price features. We tested different methods to match our 10K files with the right stock symbol. The nasdaqlisted and otherlisted were used for first experiment, but finally we found more comprehensive document 'cik_ticker.csv' on the internet. Therefore, our 'Final_code_Mapping.ipynb' using the cik_ticker.csv for our final mapping. Then we also created a stopword list through observing the frequency of words in random chosen 10K files, which detail code explanation in 'Final_Stop_words.ipynb'

##### a. cik_ticker.csv ---- include the correspondend stock symbol with their CIK
##### b. nasdaqlisted.txt --- include all of the CIK of companies listed in NASDAQ
##### c. otherlisted.txt --- include CIK of companies not in NASDAQ
##### d. CIK --- CIk of all 10K files 
##### e. finance digit --- experiement on extracting financial ratios in 10K files
##### f. Final_code_Mapping.ipynb --- code for merging CIK and Stock symbol
##### g. FInal_mapping_Previous.ipynb --- experiment on mapping using nasdaqlisted and otherlisted.
##### h. Final_Stop_words.ipynb --- code for creating stopword list.


## 3. Document Embedding Folder

In the Document_Embedding_model_build.ipynb, it includes our all of our models with 10K predictors processed by Document embedding. The detail model explained in the code.

##### a. Document Embedding Parameter Tuning
##### b. Baseline Model -- Document Embedding
##### c. Baseline model -- Price feature
##### d. MSE plot of baseline modelse. Build All-feature Predictors
##### f. Parameter tuning of regression model

There are two csv files contains the MSE results of e. Build All-feature Predictors  and f.Parameter tuning of regression model


## 4. TF-IDF Folder 

The TF-IDF folder contains two sub-folder, TF-IDF_Baseline and TF-IDF_all_feature.
##### a.TF-IDF_Baseline contains the code for TF-IDF baseline model builder, After-preprocessing data, and stopword list.
##### b.TF-IDF_all_feature contains the code for TF-IDF all features model builder, After-preprocessing data, and stopword list.

## 5. plot Folder

In this folder, it includes our final results for combined features model with both Document embedding and TF-IDF. We also include the plotting code for our project.

##### a. docu_embedding_all_feature_mse 1.csv
##### b. docu_embedding_all_feature_mse.csv
##### c. tfidf_all_feature_mse 1.csv
##### d. tfidf_all_feature_mse.csv
##### e. plot.ipynb

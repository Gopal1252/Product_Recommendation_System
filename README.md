# Product_Recommendation_System

This simple recommendation system consists of 4 different types of Retrieval Models:
1. Generating Candidate Vector Embeddings Using Text Descriptions
2. Generating Candidate Vector Embeddings Using Images
3. Generating Candidate Vector Embeddings Using Product Features
4. Generating Candidate Vector Embeddings Using Tensorflow Recommenders

These Vector Embeddings are them Passed to KNN which finds similar items making use of dot product as the similarity metric.<br />
Scores are generated for each of the recommended article as: (1 - cosine_similarity) {cosine similarity can be understood as the distance b/w two recommendations}

One more set of recommendations were generated corresponding to combining all the embeddings.

## Dataset Used

The dataset used in this project can be found on kaggle at: https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations/data

## Replicating Any Notebook From The Project

I made use of google colab for each of my notebooks due to my system limiltations and also because it is much easier to load this huge dataset from Kaggle on Colab.<br/>
Also I saved the generated Pickle files of embeddings and the KNN models for each of the model on my drive, so I would recommend you to mount your google drive on the notebook.<br />

To replicate the my notebook and to understand the role of first few lines of each notebook:<br />

1. Go to your account, Scroll to API section and Click Expire API Token to remove previous tokens

2. Click on Create New API Token - It will download kaggle.json file on your machine.

3. Now whenever you start to work on any notebook, first upload the API token to the colab notebook and also mount your google drive if required.

4. Enter these commands to read the kaggle file
   ```
   import os
   os.environ['KAGGLE_CONFIG_DIR'] = '/content'
   ```
   
5. to download the dataset zip:
   ```
   !kaggle competitions download -c h-and-m-personalized-fashion-recommendations
   ```

6. Make a directory and unzip the dataset there (it takes some time since size of the entire dataset is approximately 35GB
   ```
   !mkdir data
   !unzip h-and-m-personalized-fashion-recommendations.zip -d data
   ```
You are good to go now! <br />
If you want you can also follow the steps given on Kaggle: https://www.kaggle.com/discussions/general/74235

## Replicating The Demo App

To replicate the demo app, just ensure you have the libraries mentioned and you are good to go.


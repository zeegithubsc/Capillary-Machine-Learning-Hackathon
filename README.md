# Capillary-Machine-Learning-Hackathon (Rank 34 Solution)

## Competition Link
https://datahack.analyticsvidhya.com/contest/capillary-machine-learning-hackathon/

## Leader Board link
https://datahack.analyticsvidhya.com/contest/capillary-machine-learning-hackathon/#LeaderBoard

## Problem Statement
Capillary would like to welcome you to build a recommender system for its top fashion retail client to increase the client's user engagement. The main goal is to come up with an algorithm which will recommend best suited items from the inventory to a user in order to improve his/her shopping experience. On the basis of user transaction history, collaborative information and item features, recommend the ranked top 10 items for a user which means that the participant has to rank the recommendations for an user in the order of choice.
 
As part of this challenge, you are provided a retail brand dataset with user transaction details, item tagged fashion images, item attributes and other metadata.
 
## Data Dictionary
1. Train.zip contains the following:
 
•	train.csv
training data contains transaction history of 27778 users for 7 months (April - October)
  
|Variable|	Description|
|---|---|
|UserId|	Unique ID for user
|productid|	Unique ID for product
|Quantity|	Quantity of product bought
|OrderDate|	Timestamp of transaction
 
•	product_attributes.csv
 
|Variable|	Description|
|---|---|
|productid|	Unique ID for product|
|attribute_name|	Name of attribute (fit/sleeve/Fabric….)|
|attributevalue|	Anonymised Attribute Value (unordered)|
 
•	Images Folder
Contains the images corresponding to all items with the format <productid>.jpg
 
2. test.csv
The test data contains the user list for which the participant is supposed to come up with the best recommendations (maximum 10). These users represent a subset of users from the train data who made atleast 1 transaction in the 2 months following the last transaction in the train set.

|Variable|	Description|
|---|---|
|UserId|	Unique ID for user|
 
 ## Evaluation Metric
The evaluation metric for this contest is Mean Average Precision at K  - MAP@K (K = 10)
 
## Baseline Script
To help the participants get started with the problem, Capillary has provided a few scripts at this link.
 
## Public and Private Split

The user IDs in test data is further randomly divided into Public (30%) and Private (70%) data.

Your initial responses will be checked and scored on the Public data.
The final rankings would be based on your private score which will be published once the competition is over.
  
## Rank 34 Solution Description

Public Rank:36, Private Rank: 34
Public Score: 0.0252526736462907, Private Score: 0.0293245310732646

Since, top 10 products needed to be recommended for a user, the problem was modified to predict the product count for each user based on the product features and user purchasing behaviour. The top products based on the highest count was chosen for a user. If the predicted list had less than 10 products. The top commonly used products from the training set based on the count was picked for the user.

5 LightGBM models were trained and used for prediction in k-fold manner.

final_submission_sub4.ipynb contains the entire code.



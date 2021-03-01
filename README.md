# Capillary-Machine-Learning-Hackathon

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
  


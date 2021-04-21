# Shelter Animal Outcomes
## Help improve outcomes for shelter animals

 ## Contents:
 
- [Background](#Background)  
- [Problem Statement](#Problem-Statement)  
- [Data](#Data)
- [Data Analysis](#Data-Analysis)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

## Background:

Every year, approximately 7.6 million companion animals end up in US shelters. Many animals are given up as unwanted by their owners, while others are picked up after getting lost or taken out of cruelty situations. Many of these animals find forever families to take them home, but just as many are not so lucky. 2.7 million dogs and cats are euthanized in the US every year.


## Problem Statement:

Given a dataset comprised of animals brought into a shelter (type, color, age of animal, etc.), I will attempt to predict the outcome of the animal (either adopted, transferred, euthanized, died or returned to owner).

## Data

* [datafile 1](/Users/edwardmendoza/Documents/GA/Projects/project_4_hackathon/data/train.csv): Train Dataset

## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|AnimalID|object|Train|ID of Animal|
|Name|object|Train|Name of Animal|
|DateTime|object|Train|Date of Animal Being Admitted|
|OutcomeType|object|Train|Outcome of Animal|
|OutcomeSubtype|object|Train|Subtype outcome of Animal|
|AnimalType|object|Train|Animal Type|
|SexuponOutcome|object|Train|Animal Sex|
|AgeuponOutcome|object|Train|Animal Age|
|Breed|object|Train|Animal Breed|
|Color|object|Train|Animal Color|

## Data Analysis

What I have found in the data are that dogs are adopted more than cats, while most cats were transferred out of the animal shelter. 

The majority of animals are more than likely to be adopted or transferred to another animal shelter, while roughly 2000 animals were either euthanized or died in the shelter. 

I used 5 models for my predictions, and the results on the training and testing sets were the following:

|Model|Training Score|Testing Score
|---|---|---|
|Random Forest|0.632|0.643|
|Single Decision Tree|0.610|0.616|
|Logistic Regression|0.633|0.643|
|Extra Trees|0.610|0.617|
|Bagging Classifier|0.681|0.645|

## Conclusions and Recommendations

The scores of all my models would be considered relatively medium bias and of medium variance, since most of my scores ranged between the sixties. The bagging classifier edged out the rest of my models, of which the concept of bootstrapping the data and aggregating it mitgates the problem of the model learning the highly irregular patterns and exposes the trees to different sub-samples of the training set. 

To further improve on my models, I would have to create multiple dummy variables for the breed and color column, which may assist in improving on my testing score. 

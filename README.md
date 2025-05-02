# DATA3402FinalProject

# Project Title

* **One Sentence Summary**:
  The goal of this challenge is to identify characteristics of mushrooms that are indicitive of whether or not it is poisonous using data from the "Mushroom Classification" data Kaggle challenge.

  https://www.kaggle.com/datasets/uciml/mushroom-classification

## Overview

The task of this challence is to use observations of different mushrooms and their characteristics to determine whether or not we can predict if a mushroom is poisonous by its features alone. In the notebook, we initially trained a Random Forest Classifier model as it helps prevent overfitting, making the model more likely to be accurate. The Random Forest model returned a score of 1.0, which then prompted two more models (Logistic Regression and Neural Network) to be trained to see if the data was overtrained in the Random Forest model. The Logistic Regression model and the Neural Network model both returned scores of 1.0 as well. While all models point to the data being perfectly represented, having a perfect 1.0 raises some alarm bells indicating overfitting of the data or something of the like.

## Summary of Workdone



### Data

* 8124 rows/observations
* 374 kB data set
* 80% of observations for training, 20% for testing

#### Preprocessing / Clean up

? symbols were replaced with NaN values so that they could be recognized by the .isnull().sum() funciton. 2480 null observations were found for the stalk-root feature. These null values were then filled with the most frequent value. The features were then all one-hot encoded so that the categorical variables would be binary.

#### Data Visualization

![image](https://github.com/user-attachments/assets/b556ca68-cdc7-40e6-b567-3194ad2e4cc7)


### Problem Formulation



### Training



### Performance Comparison



### Conclusions



### Future Work



## How to reproduce results



### Overview of files in repository



### Software Setup



### Data



### Training



#### Performance Evaluation



## Citations



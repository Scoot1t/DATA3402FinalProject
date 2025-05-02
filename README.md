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

? symbols were replaced with NaN values so that they could be recognized by the .isnull().sum() funciton. 2480 null observations were found for the stalk-root feature. These null values were then filled with the most frequent value. The features were then all one-hot encoded so that the categorical variables would be binary. This was used for the Random Forest model. Then the data was converted into numerical values so that the Logisitic Regression and Neural Network models could be trained.

#### Data Visualization

The following 3 histograms show a few features that are important to the training of the model.

![image](https://github.com/user-attachments/assets/0d0be1f4-4c53-4a26-8112-bf85eb90470e)

![image](https://github.com/user-attachments/assets/3385120e-d70f-4f79-b85c-aebea821c12d)

![image](https://github.com/user-attachments/assets/b5f7ed79-e270-45d5-8f75-8e93ff27978a)

Now, the next 2 histograms are examples of features that are not as important to the training of the model:

![image](https://github.com/user-attachments/assets/43f1db04-240f-4c33-bbf1-43a104ba929b)

![image](https://github.com/user-attachments/assets/397892fa-0fa9-433f-ba7e-1741b99f1cbe)


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



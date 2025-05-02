# DATA3402FinalProject

# Classificaion of mushrooms: what implies poisonous?

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

? symbols were replaced with NaN values so that they could be recognized by the .isnull().sum() funciton. 2480 null observations were found for the stalk-root feature. These null values were then filled with the most frequent value. The features were then all one-hot encoded so that the categorical variables would be binary. This new dataset was used for the Random Forest model. Then the data was converted into numerical values so that the Logisitic Regression and Neural Network models could be trained.

#### Data Visualization

The following 3 histograms show a few features that are important to the training of the model.

![image](https://github.com/user-attachments/assets/0d0be1f4-4c53-4a26-8112-bf85eb90470e)

![image](https://github.com/user-attachments/assets/3385120e-d70f-4f79-b85c-aebea821c12d)

![image](https://github.com/user-attachments/assets/b5f7ed79-e270-45d5-8f75-8e93ff27978a)

Now, the next 2 histograms are examples of features that are not as important to the training of the model:

![image](https://github.com/user-attachments/assets/43f1db04-240f-4c33-bbf1-43a104ba929b)

![image](https://github.com/user-attachments/assets/397892fa-0fa9-433f-ba7e-1741b99f1cbe)


### Problem Formulation

There were 23 features considered in the dataset, one of which is called "class" which describes if an observation is edible or poisonous. As stated before, the Random Forest Classification model was used first because of its resistance to overtraining. When a perfect 1.0 was returned, two more tests were tried (Logistic Regression and Neural Network) to verify the Random Forest model's results.

### Training

The software and hardware used was jupyter notebook on Ubuntu OS ran on a Windows laptop.

### Performance Comparison


![image](https://github.com/user-attachments/assets/dac8137c-d51c-4e7e-b7e5-84737623baa5)


### Conclusions

Given the heat map above, it appears that no one feature is contributing larger than all others to the model. There are bright lines at veil-type since that feature seems to not contribute at all.


## How to reproduce results

* Load the mushroom.csv file into your notebook.
* First, check the number of rows and features so make sure the data is correct. Then check the type of the features to make sure they are all categorical. And last for the data review, check how many p vs e are in the class feature.
* Next, you'll want to create a histogram for each feature and how the two classes measure up to eachother. To make it more clear which features are more important to the model, use the pd.Series function to lay out all of the features and their importance in one graph.
* Check for null values by changing ?s into NaN. Then replace all NaN values with the most frequent value.
* Encode the data so that each feature has binary responses.
* Train the Random Forest Classification model with the new encoded data.
* For an extra step, encode the data into numerical values and the train the Logistic and Neural Network.
* You may also create a heat map to visualize the data.

### Overview of files in repository

KaggleWorkbook.ipynb: The main file for the challenge. All of the code for the models and the graphs are in this file.
mushrooms.csv: The data file for the challenge

### Software Setup

The following packages were used:
* pandas
* LabelEncoder from sklearn.preprocessing
* matplotlib.pyplot
* RandomForestClassifier from sklearn.ensemble
* train_test_split from sklearn.model_selection
* seaborn
* numpy
* StandardScalar from sklearn.preprocessing
* LogisticRegression from sklearn.linear_model
* MLPClassifier from sklearn.neural_network

### Data

The data can be downloaded from the website listed at the beginning of this document.

### Training

To train the model, use the imported command for whichever model you would like to look at first. This could look something like this "model_rfc = RandomForestClassifier" and then "model_rfc.fit(x_train, y_train)" after you have appropriately defined x_test, x_train, y_test, and y_train.

#### Performance Evaluation

To run the performance evaluation for your model, simply use .score() to get the score for that model. An example usage would be, after training the model for RandomForestClassifier, "model_rfc.score(x_test, y_test)"

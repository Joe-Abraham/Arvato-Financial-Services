# Arvato-Financial-Services

# Machine Learning Engineer Nanodegree
## Capstone Project
Joe Abraham  
September 20, 2020

## Project Motivation :

This project is done to apply machine learning alogirithms in supervised and un-supervised manner, and to come to meaningful conclusions. I have analysed demographics data of a mail order sales company in Germany. Comparing customers with general public, to find a correlation between customer and general population.

The whole project is divided into 4 parts:

- Part 0 : Know the data, where you try to understand the data
- Part 1 : Customer Segmentation (Unsupervised Learning)
- Part 2 : Supervised Learning
- Part 3 : Kaggle competition

The main pre-requisite for applying some machine-learning algorithm is that you need a clean dataset. Understanding and cleaning the dataset is the most critical task that I did.
While processing data we should make sure that we lose important informations. So data pre-processing is the most important  stage.

### Data Pre-Processing

I have done the following steps in pre-processing

- Took the help of excel sheet to exactly know how unknown data is represented
- Filled the unknown data with NaNs
- Replaced birth year to NaN, if it is zero.
- Dropped the columns, if most of the values are NaNs(only for unsupervised learning)
- Replaced NaN with most frequent value in that particular column
- Performed feature scaling

### Un-supervised Learning

There was no constrain of elements in PCA and after doing PCA on the cleaned data, I found that variance almost become 0 after 200 components (graph available inside the notebook) 

To find the right amount of cluster KMeans was applied in a loop from 1 to 19 and after that elbow methid is used and 10 was my best choice to differentiate between customer and general public.

### Supervised Learning

plot_learning_curve was taken from sklearn official site. And plotterd for XGBoost, Random Forest, AdaBoost and Decision Tree. And I found that XGBoost is performing good.
Hyperparameter tuning is done to XGBoost and it was giving a cross validation score of 0.987

### Kaggle competition

The model was run of a provided dataset and then submitted on Kaggle and my model performed with score 0.80596. And I grabbed 24th place in leadershipboard as on 20-09-2020 (Screenshot attached in the notebook)

-----------

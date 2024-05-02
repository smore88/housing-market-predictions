# House Prices Prediction Project

## My Motivation 

Having completed CS 441 (Applied Machine Learning) at UIUC, along with certifications in Machine Learning from Andrew Ng's DeepLearning.AI, I embarked on this project to both revisit and deepen my understanding of machine learning principles through hands-on practice. Additionally, this past week at my internship I was assigned a new task of developing a production Machine Learning model to analyze a SQL database of financial data. This further inspired me to engage with Machine Learning frameworks.

## Overview

I found a comprehensive dataset from Kaggle that details the sales prices of houses in Ames, Iowa, accompanied by 81 varied features. The dataset is split into 1,460 training instances and 1,459 test instances. My approach involves dividing the training set into an 80% training subset (X_train) and a 20% validation subset (X_val). The aim is to develop diverse predictive models to accurately forecast house sales prices and to optimize these models through rigorous hyperparameter tuning and sophisticated feature engineering. The project's challenge is to adeptly handle and analyze high-dimensional data. I plan to utilizing the following tools that are not limited too: GridSearchCV, Support Vector Regression(SVR), Random Forest, Gradient Boosting, K-Nearest Neighbors, and Multi-Layers Perceptrons(MLPs). Each model I build will be evaluated based on the root-mean-squared error (RMSE) between the logarithm of the predicted value and the logarithm of the observed sales prices. Such a transformation ensures that errors in predicting expensive houses and cheap houses will affect the result equally.

## Dataset

The dataset includes a comprehensive set of features about the physical attributes of residential homes. Key features include:

- `OverallQual`: Overall material and finish quality
- `GrLivArea`: Above grade (ground) living area square feet
- `GarageCars`: Size of garage in car capacity
- `TotalBsmtSF`: Total square feet of basement area
- `FullBath`: Full bathrooms above grade
- `YearBuilt`: Original construction date

The target variable is `SalePrice`, which we aim to predict.

## File Descriptions

- `train.csv` - the training set containing details of houses and their sale prices.
- `test.csv` - the test set where predictions are to be made, without the sale prices.
- `data_description.txt` - full description of each column.

## Short Summary: Development Process

I explored three different machine learning models: Random Forest, Support Vector Regression (SVR), and Multi-Layer Perceptron (MLP). Each model underwent rigorous testing with various hyperparameters to determine the optimal configurations. For instance, the Random Forest model was tested with different numbers of trees, tree depths, and minimum samples per split to prevent overfitting and enhance prediction accuracy. To make sure that all the models were trained on correctly processed data I built various pipelines for the stages of training and evaulated metrics at the ends of each step of the pipeline. I did this for all 3 models. AFter doing this I found that Support Vector Regression had the best results with the lowest RMSE, but I became interested in the affects of handling missing data and how that changes the results. In my preprocessing I handled categorical missing data by converting the non-missing data into one-hot vectors and I used an imputer to put in the median of values, I did the same for the numerical as well, but I became interested in generated these missing data points using ML models. This is where gradient boosting, random forest regressors, and K-nearest neighbors came into play. I found that if I use ML models to impute missing data the RMSE scores actually lower which is what we wanted in the first place. Overall, the work was highly iterative, involving continuous refinement of models based on validation set performance. I used Google Colab in facilitating coding and testing phases which allowed for an efficient workflow. In the final phase of the project, I fine-tuned the best-performing models on the combined training and validation sets and then used these models to predict house prices on the unseen test set. These predictions were submitted to the Kaggle platform for external validation, providing a real-world measure of the model's effectiveness. This meticulous approach to model development not only enhanced my machine learning skills but also deepened my understanding of complex data analytics challenges in real-world scenarios.

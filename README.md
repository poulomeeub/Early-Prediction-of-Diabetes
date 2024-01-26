# Objective:  
 -According to WHO by the year 2025, Diabetes will directly attribute to 1.5 million death per year around the world and become one of the four most prevalent non-communicable diseases around the world.
 -To predict diabetes early we in our current project we are trying to identify the factors underlying the disease.
![image](https://github.com/poulomeeub/Prediction-of-Diabetes/assets/143571669/3fd84961-b1ba-4104-89af-bac3b6a55094)

# Description:
 - This project runs multiple classifier models and come up with the best classification algorithm for the dataset

# Dataset:
 - Download the datasetb from Kaggle BRFSS 2015 Dataset https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset
 - # Data_description:
   - We have taken the dataset namely BRFSS 2015 Diabetes Survey Data set which has 253680 records and 22 columns, one of which are response variables and rest are predictor variables.
   - For our analysis purposes, the pre-diabetes records has been excluded from the dataset to form a distinct classification model which has 24909 records.
   - ![image](https://github.com/poulomeeub/Prediction-of-Diabetes/assets/143571669/a182d1c5-17f1-4d46-872b-211039515bab)

# Project Flow chart:
   ![image](https://github.com/poulomeeub/Prediction-of-Diabetes/assets/143571669/bf887e17-0723-4d8e-883b-38ab8569fe53)

# Data Pre-processing:
 -As a first step of pre-processing, we have excluded all the pre-diabetes patients from the dataset. Thereafter, we have converted every variable in the dataset into integer values.
 -After converting each value, we have checked for null values in each column and in this dataset no null records existed.
 -Again, we checked for duplicate records and based on that we have excluded ~23k duplicate records. 
 -Also, we have checked for outliers in the dataset and found out there are not any outliers in the dataset.
 -As observed in the dataset, the response variable is skewed. Almost 85% of the responses are 0 corresponding to non-diabetic and 16% of the dataset is for diabetic patients. To handle that we have used ‘NearMiss’ algorithms.
 - ## Data Scaling
 - After that, we have performed data scaling. Data scaling is a crucial step before the model creation.
    •	Standardization: Standardizing features ensures that they have a mean of 0 and a standard deviation of 1.This helps in bringing all features to a similar scale, preventing some features from dominating others during model training.
    •	Algorithm Sensitivity: Many machine learning algorithms are sensitive to the scale of input features. For example, gradient descent-based optimization algorithms converge faster when features are on a similar scale.
    •	Interpretability: Standardized features make it easier to interpret the coefficients in linear models since they represent the change in the output variable for a one-standard-deviation change in the input variable.
  In summary, data scaling is a preprocessing step that helps improve the performance and stability of machine learning models, especially when using algorithms that are sensitive to the scale of input features.
  In our research ‘StandardScaler’ library is used for the data scaling.
 - ## Data Splitting
 - For our machine learning model training purpose, we have split our data into **20%** of data into test data and **80%** of data into training data. For neural network model training purpose we have split the data by **30%** test and **70%** train.
 - The training data is used to train the data through its trend and pattern and test data is used to evaluate its performance to predict unseen test cases.

 - ## Reshaping features and target variables forneural network
 - Reshaping of features are required before giving input to neural networks, every feature need to be converted into a separate channel followed by reshaping it into PyTorch tensor. Here we are reshaping the features into 3D tensors.
 - Similarly, we have converted our response variable into 2D tensors followed by PyTorch tensor conversion.

# Predictive modeling:
In this study we have employed multiple machine learning models for classification. 
 - Various machine learning models such as Logistic Regression, Decision Trees, KNN classification, Random Forest, XgBoost, SVM models have been explored on this regard.
 - Apart from the machine learning model some deep learning method including ANN, Recurrent Neural Network, Feedforward Neural Network (with or without PyTorch) have been used here.

# Requirements:
- Python 3.8
- Pytorch 1.1+
- # Python libraries
  - pandas
  - numpy
  - seaborn
  - catboost
  - lightgbm
  - imbalanced-learn
  - tensorflow
  - mlxtend
  - pandas-profiling
  - matplotlib
  - xgboost
  - torch   

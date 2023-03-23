# Ryerson_Final_Project

Study step:
1. Data Exploration
•	Discover the shape of the dataset (569 X 32). It is for feature selection and the percentage of training and test split.
•	Explore the data type of features. It is to decide if the dataset needs further transformation (Convert non-numeric to numerical values). 
•	Count the unique values of the class to see if the dataset balanced or not.
•	Statistical summary including average, standard deviation, minimum, maximum and quarterly percentiles. 
•	Use histograms to check distribution of all the columns. The histograms can help to see if an attribute normal, left skewed or right skewed.
•	Draw a heatmap to see the correlation between attributes, especially between features and the class. It is important for feature selection.

2. Data cleaning & preparation
•	Import the dataset. The data was saved in CSV format. It was imported and converted to a dataframe type.
•	Drop the noise. “id” column is the unique identify numbers of patients. It does not affect the class. So “id” column is a noise should be dropped.
•	Convert data type. “diagnosis” column which is also the class has 2 unique string values: M and B. Models in sklearn package can only be fit by numerical values. So I convert the values to integer type: M to 1 and B to 0.

3. Feature selection
A combination of methods to select features: correlation and Gain Ratio.
Selecting the right features is for avoiding overfitting or underfitting.

4. Scale data
Features values are not at the same level. It is necessary to scale data.

5. Split the dataset
Before fitting models, the dataset needs to be split into training set and test set. 
The training set is for fitting models. The test set is for evaluating models.
Each record was randomly chosen to be in either training set or test set. 

6. Build models
Simply initial 5 models with sklearn package: Logistic Regression, Decision Tree, Random Forest, KNN and Gaussian Naïve Bayes.
Then fit the models with training data and make predictions with test data.
The predictions are a list of predicted values with the same size as the test data. The list can be used to compare to the test data to evaluate models.

7. Evaluate models
Accuracy and cross validation score were used to evaluate models in this study.

8.Repeat the process
Repeat the process from split dataset to models evaluation to see if the result will be stable or not. In this study, it was repeated 5 times.



Content of the repository:
This repository has 3 files: breast-cancer.csv, EDA.ipynb and code.ipynb.

The breast-cancer.csv is the dataset file downloaded from Kaggle: https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset
https://github.com/checkming00/Ryerson_Final_Project/blob/main/breast-cancer.csv

The EDA.ipynb is an EDA report with codes. It shows overview of the dataset such as statistical summary, distribution and correlationship and so on.
https://github.com/checkming00/Ryerson_Final_Project/blob/main/EDA.ipynb

The code.ipynb is the coding file to clean data, create machine learning models, make predictions and evaluate models' performances.
https://github.com/checkming00/Ryerson_Final_Project/blob/main/code.ipynb






reference:
Classification and Diagnostic Prediction of Breast Cancers via Different Classifiers by Ahmet Saygılı, aNamık Kemal University, Çorlu Engineering Faculty, Department of Computer Engineering, Tekirdağ, Turkey 

https://dergipark.org.tr/en/download/article-file/615107


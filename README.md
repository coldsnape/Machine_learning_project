# Detect Presence of Heart Disease Through ML
### This repo contains materials from MSDS-691 course, Machine Learning Lab.
Here, I get to apply machine learning concepts and best practices to real world data


### Majority of the work is done in DeepNote, link is listed below:
https://deepnote.com/project/960ce66a-728d-4a49-9d4e-4ed93cf3dd63 (Links to an external site.) 


### Data General Description
The data is a subset of a larger data from the Cleveland database repository, which is approved to be used for ML researchers. This data contains the most relevant attributes that one would find that are related to the health condition of the heart. 

Link to dataset: https://www.kaggle.com/ronitf/heart-disease-uci?select=heart.csv (Links to an external site.) 
- Number of observations: 303
- Number of raw features. 14
- Column names:
age, sex, cp, trestbps, chol, fbs, restecg, thalach,	exang,	oldpeak, slope,	ca, thal,	target
	

### Goal
The goal of this project is to apply Machine Learning concepts to this healthcare data set to see if I can find a predictive model that can effectly detect the presence of heart disease within a significant level of accuracy.

What did you find?
### Steps taken
- EDA: The data is relatively clean to begin with, however the number of records is relatively low to get high accuracy score.

- Feature Engineering: Again the data attributes are quite complete with relatively no significant feature engineering needed. For preprocessing, I applied SimpleImputer, just in case there are missing values, along with OneHotEncoder for categorical features. In addition, I also standardize the numberical features with StandardScaler before applying a variety of machine learning models.

- Split Data: I split the data into 30% test, 20% validation, and 50% train

- Algorithms & Search: First, I ran the data through 9 robust algorithms in default settings that can handle binary classification. Second, I selected the 3 relative high perfoming algorithms from that group and do hyper-peramater search with RandomizedSearchCV. Third, I selected the best model with best hyper-perameter and applied cross validation to evaluate. This would allow my model to potentially see 70% of the entire data for better outcome.

- Evaluation Metrics: Among the evaluation metrics, I decided to go with F1 score for a balance between accuracy and recall. While I care about prediction accuracy, I also want to make sure my model has recall performance to ensure correct prediction.

### Applying different concepts
- Feature engineer with PCA and K-mean clustering with best model
- Stack Models


### Conclusion
- For single model performance, tuned ExtraTreesClassifier model perform best ~ 85% F1 score
- Cross validation is key to improve model training
- Stacked models has slightly more prediction power, at the cost of computation load
- Even though this data set is fairly small, I can still apply a good ML model to help detect a presense of heart disease.
- I would select a simple working model over complexed models that might have little to no gain.

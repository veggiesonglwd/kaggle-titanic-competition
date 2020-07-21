# kaggle-titanic-competition
This competition's goal is to correctly predict if someone survived the Titanic shipwreck considering other features.
You can find the dataset and relative information in this link:
https://www.kaggle.com/c/titanic

# Project Procedure
## Data Exploration
### 1) For numeric data 
* Made histograms to understand distributions 
* Corrplot 
* Pivot table comparing survival rate across numeric variables 


### 2) For Categorical Data 
* Bar charts to understand balance of classes 
* Pivot tables to understand relationship with survival 
* Histograms and boxplots 
* Value counts 
* Missing data 
* Correlation between the metrics 

## Feature Engineering of Categorical data-Steps(Cabin and Ticket messy)

### 1) Simplify cabins (check if cabin letter (cabin_adv) or the purchase of tickets across multiple cabins (cabin_multiple) influenced survival)

### 2) Check if different ticket types impact survival rates

### 3) Check if a person's title is related to survival rates(tranfrom from Name column)

## BaselineModel Building 
1. Check how various different models perform with default parameters. 

2. Try the following models using 5 fold cross validation to get a base submission.
3. With a validation set as a baseline, we can make further attempts to see how much tuning improves each of the models. 
4. For every algorithm, try both date with and without training.
5. **Best Results: Support Vector Classifier (83.4%)**
## Model Tuned Performance 
After getting the baselines, check if we can improve on the indivdual model results!
1. Mainly use grid search to tune the models. 
2. Use Randomized Search for the Random Forest and XG boosted model to simplify testing time. 

## Model Additional Ensemble Approaches 
1. Experimented with a hard voting classifier of three estimators (KNN, SVM, RF) (81.2%)

2. Experimented with a soft voting classifier of three estimators (KNN, SVM, RF) (81.33%)

3. Experimented with soft voting on all estimators performing better than 80% except xgb (KNN, RF, LR, SVC) (82.7%)

4. **Experimented with soft voting on all estimators including XGB (KNN, SVM, RF, LR, XGB) (83.4%)**

## Play with Basic TensorFlow modeling

# Reference
*  https://www.youtube.com/watch?v=I3FBJdiExcg
* https://www.kaggle.com/kenjee/titanic-project-example

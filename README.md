# TIMSS 2019 Modeling

## Sources
#### Trends in Math and Science Study (2019)
[2019 TIMSS Database](https://timss2019.org/international-database/)
The following analysis uses publicly available data from the TIMSS official website.
The program is written to analyze all of the available data, but the scope of this repository is limited to 10 countries for the purposes of storage and run time.

## Purpose
#### Questions of Interest
1. How does a student's environment at home, in the classroom, and at school affect academic understanding?
2. Are there specific teacher behaviors that lead to improved understanding in specific disciplines?
3. What can students and teachers do to improve student academic understanding?

#### Scope of Purpose
The project will cover a variety of analyses regarding data collected. The project will include:
* prediction of student score based on student attitudes and demographics, school characteristics
* prediction of student scores based on teacher attitudes and practices
* recommendation engine for additional study problems for a given student (or group of students from a school or country)

## Methods
#### Packages
- `pandas`
- `numpy`
- `pyreadstat`
- `matplotlib`
- `seaborn`
- `glob`
- `random`
- `re`
- `statsmodels`
- `sklearn`
- `xgboost`

#### Data Gathering and Processing Technique
- gather and organize data for variety of SPSS files (`glob`, `pandas.read_spss`)
- gather item information and metadata (`pandas.read_excel`)
- drop unnecessary/irrelevant columns (`pandas.drop`)
- simplify and combine assessment scores for easier application
- average student assessment scores to a single number
- explore data structure (`pandas.info()`, `pandas.describe()`)
- visualize basic relationships (`matplotlib`, `seaborn`)
- record initial observation and plan for data preparation
- perform data preparation on each dataset
  - drop irrelevant information for that specific data (`pandas.drop`)
  - convert datatypes for appropriate analysis (`pandas.astype`)
  - give columns more descriptive names (`pandas.rename`)
  - perform any necessary transformations (`pandas.apply`)
  - average columns into like groups (`pandas.groupby`)
  - join data from other tables when helpful to the analysis (`pandas.join`)
- store processed data (`pandas.to_csv`)

#### Data Models
_** Regression **_
- identifying variables of interest
- create dummy variables for string objects (`pandas.get_dummies`)
- split the data for training and testing (`sklearn.model_selection.train_test_split`)
- create and train the linear regression models (`statsmodels.api.OLS`)
- explore relative weights of variables in regression models
- create predictions and confidence intervals for test dataset (`statsmodels.api.OLS.predict`, `statsmodels.api.OLS.get_prediction`)
- evaluate effectiveness of models and confidence intervals
- visualize models (`seaborn`, `matplotlib`)

_** Classification **_
- identifying and gathering variables of interest
- split the data for training and testing (`sklearn.model_selection.train_test_split`)
- create base models
  - `sklearn.ensemble.RandomForestClassifier`
  - `xgboost.XGBClassifier`
  - `sklearn.neighbors.KNeighborsClassifier`
- set up parameter grids for optimization
- fit and optimize base model with grid search of parameters (`sklearn.model_selection.GridSearchCV`)
- display results and accuracy (`sklearn.metrics.confusion_matrix`)
- compare similarity between different models

_** Recommendation **_
- gather assessment item information
- drop irrelevant information to construct user_item dataframe
- create collection of helper functions to:
  - identify similar users (`find_similar_users`)
  - gather specific item information (`get_item_info`)
  - gather items assessed by a user (`get_user_items`)
  - create ranked user-to-user recommendations for new items (`user_user_recs`)
  - implement FunkSVD to estimate score on previously unknown items (`FunkSVD`)
  - estimate scores for unassessed items for a user (`user_item_predict`)
  - implement custom sigmoid activation function for smoother predictions (`sig`)
- test recommendation engine

#### Evaluation


## Conclusion
#### Context


#### Findings


#### Summary

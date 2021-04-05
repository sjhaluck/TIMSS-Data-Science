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


#### Evaluation


## Conclusion
#### Context


#### Findings


#### Summary

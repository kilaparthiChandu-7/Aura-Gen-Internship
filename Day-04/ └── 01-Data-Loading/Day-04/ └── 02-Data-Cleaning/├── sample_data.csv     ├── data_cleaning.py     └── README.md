id,name,age,score
1,Alice,21,85
2,Bob,,78
3,Charlie,20,
4,David,23,74
5,Eva,,88


import pandas as pd

# Load dataset
data = pd.read_csv("sample_data.csv")

print("Missing values before cleaning:")
print(data.isnull().sum())

# Fill missing numerical values with column mean
data["age"] = data["age"].fillna(data["age"].mean())
data["score"] = data["score"].fillna(data["score"].mean())

print("\nMissing values after cleaning:")
print(data.isnull().sum())

print("\nCleaned Dataset:")
print(data)


EXPECTED OUTPUT :

Missing values before cleaning:
id       0
name     0
age      2
score    1

Missing values after cleaning:
id       0
name     0
age      0
score    0



# Day 4 – Topic 2: Data Cleaning

## Objective
Understand basic data cleaning and missing-value handling.

## Work Completed
- Loaded a dataset containing missing values.
- Identified missing values using Pandas.
- Replaced missing numerical values with the column mean.
- Verified the cleaned dataset.

## Technology Used
- Python
- Pandas

## Key Learning
Data cleaning is an important preprocessing step before performing
analysis or building machine learning models.

## Status
✅ Data cleaning completed.

id,name,age,score
1,Alice,21,85
2,Bob,22,78
3,Charlie,20,92
4,David,23,74
5,Eva,21,88



import pandas as pd

# Load dataset
data = pd.read_csv("data.csv")

# Display dataset
print("Dataset:")
print(data)

# Display basic information
print("\nDataset Shape:")
print(data.shape)

print("\nColumn Names:")
print(data.columns.tolist())

print("\nBasic Statistics:")
print(data.describe())

EXPECTED OUTPUT:

Dataset Shape:
(5, 4)

Column Names:
['id', 'name', 'age', 'score']



# Day 4 – Topic 1: Data Loading and Inspection

## Objective
Learn how to load and inspect data using Python and Pandas.

## Work Completed
- Created a sample dataset.
- Loaded the dataset using Pandas.
- Checked the number of rows and columns.
- Displayed column names.
- Generated basic statistical information.

## Technology Used
- Python
- Pandas

## Status
✅ Data loading and inspection completed.

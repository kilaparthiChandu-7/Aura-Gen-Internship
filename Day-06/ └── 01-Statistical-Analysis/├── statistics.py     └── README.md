Program

import pandas as pd

# Sample dataset
data = {
    "Name": ["Alice", "Bob", "Charlie", "David", "Eva"],
    "Score": [85, 78, 92, 74, 88]
}

df = pd.DataFrame(data)

# Statistical analysis
mean_score = df["Score"].mean()
median_score = df["Score"].median()
minimum_score = df["Score"].min()
maximum_score = df["Score"].max()
std_score = df["Score"].std()

print("Statistical Analysis")
print("--------------------")
print("Mean Score:", round(mean_score, 2))
print("Median Score:", median_score)
print("Minimum Score:", minimum_score)
print("Maximum Score:", maximum_score)
print("Standard Deviation:", round(std_score, 2))


Expected Outout


Statistical Analysis
--------------------
Mean Score: 83.4
Median Score: 85.0
Minimum Score: 74
Maximum Score: 92
Standard Deviation: 7.06


# Day 6 – Statistical Analysis

## Objective

Perform basic statistical analysis on the prepared dataset.

## Work Completed

- Calculated the mean.
- Calculated the median.
- Identified minimum and maximum values.
- Calculated standard deviation.
- Used Pandas for statistical analysis.

## Technologies Used

- Python
- Pandas

## Key Learning

Statistical measures help understand the distribution and characteristics
of numerical data.

## Status

✅ Statistical analysis completed.

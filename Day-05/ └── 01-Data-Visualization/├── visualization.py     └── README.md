import pandas as pd
import matplotlib.pyplot as plt

# Sample dataset
data = {
    "Name": ["Alice", "Bob", "Charlie", "David", "Eva"],
    "Score": [85, 78, 92, 74, 88]
}

df = pd.DataFrame(data)

# Display data
print("Student Data:")
print(df)

# Create bar chart
plt.figure(figsize=(8, 5))
plt.bar(df["Name"], df["Score"])

plt.title("Score Comparison")
plt.xlabel("Students")
plt.ylabel("Score")

plt.tight_layout()
plt.show()


Expected output:

Student Data:

      Name  Score
0    Alice     85
1      Bob     78
2  Charlie     92
3    David     74
4      Eva     88


# Day 5 – Data Visualization

## Objective

Learn how to visualize data using Python and Matplotlib.

## Work Completed

- Created a sample dataset using Pandas.
- Converted the data into a DataFrame.
- Created a bar chart using Matplotlib.
- Added chart title and axis labels.
- Analyzed the data visually.

## Technologies Used

- Python
- Pandas
- Matplotlib

## Key Learning

Data visualization helps in understanding patterns and relationships
within a dataset more easily.

## Status

✅ Data visualization completed.

# NumPy Aggregations and Statistics

## Overview
This project demonstrates how to use NumPy to calculate basic statistical measures on numerical datasets.

## Objectives
- Calculate sum, mean, median, minimum, and maximum.
- Calculate standard deviation and variance.
- Perform row-wise and column-wise statistical analysis using `axis=0` and `axis=1`.
- Interpret the results of a numerical dataset.

## Tools Used
- Python
- NumPy
- Google Colab or Jupyter Notebook

## Dataset 1: Student Marks
```python
import numpy as np

marks = np.array([70, 80, 90, 60, 100, 85, 75])

print("Student Marks:", marks)
print("Sum:", np.sum(marks))
print("Mean:", np.mean(marks))
print("Median:", np.median(marks))
print("Minimum:", np.min(marks))
print("Maximum:", np.max(marks))
print("Standard Deviation:", np.std(marks))
print("Variance:", np.var(marks))
```

### Expected Results
- Sum: `560`
- Mean: `80.0`
- Median: `80.0`
- Minimum: `60`
- Maximum: `100`
- Standard deviation: approximately `12.2474`
- Variance: `150.0`

NumPy's `std()` and `var()` use population formulas by default (`ddof=0`).

## Dataset 2: Row-wise and Column-wise Analysis
```python
import numpy as np

data = np.array([
    [70, 80, 90],
    [60, 75, 85],
    [90, 95, 100],
    [80, 85, 75]
])

print("Dataset:")
print(data)

print("Column-wise mean:", np.mean(data, axis=0))
print("Row-wise mean:", np.mean(data, axis=1))
print("Column-wise maximum:", np.max(data, axis=0))
print("Column-wise minimum:", np.min(data, axis=0))
print("Column-wise standard deviation:", np.std(data, axis=0))
print("Column-wise variance:", np.var(data, axis=0))
```

### Understanding `axis`
- `axis=0`: calculates the result down each column (for example, each subject's statistics across students).
- `axis=1`: calculates the result across each row (for example, each student's average across subjects).

## Interpretation
- The mean gives the average value.
- The median gives the middle value after sorting the data.
- Minimum and maximum identify the smallest and largest values.
- Standard deviation describes spread around the mean.
- Variance measures spread using squared deviations.
- Column-wise analysis helps compare subjects; row-wise analysis helps compare students.

## Interview Question: What is the difference between mean and median?
**Mean** is the sum of all values divided by the number of values. **Median** is the middle value after sorting the data (or the average of the two middle values when the number of values is even). The mean is more affected by extreme values, while the median is generally more resistant to them.

## How to Run
1. Open Google Colab or Jupyter Notebook.
2. Create a new Python notebook.
3. Copy and run the code sections in order.
4. Review the outputs and write your interpretation.
5. Upload the notebook and this `README.md` file to your GitHub repository.

## Suggested GitHub Repository Name
`numpy-aggregations-statistics`

# Fundamental Pandas Commands for DataFrames

## 1. Importing Pandas and Creating a DataFrame

```python
import pandas as pd

data = {
    "Name": ["Alice", "Bob", "Charlie", "David"],
    "Age": [25, 30, 35, 40],
    "Salary": [50000, 60000, 70000, 80000]
}

df = pd.DataFrame(data)
```

---

## 2. Basic Statistics

### Display General Information
```python
df.info()
```

### Summary Statistics
```python
df.describe()
```

### Mean, Median, and Standard Deviation
```python
mean_age = df["Age"].mean()
median_age = df["Age"].median()
std_salary = df["Salary"].std()
```

### Minimum and Maximum Values
```python
min_age = df["Age"].min()
max_age = df["Age"].max()
```

---

## 3. Data Manipulations

### Sorting Data
```python
df_sorted = df.sort_values(by="Salary", ascending=False)
```

### Filtering Data
```python
filtered_df = df[df["Age"] > 30]
```

### Selecting Columns
```python
names_and_salaries = df[["Name", "Salary"]]
```

### Selecting Rows by Index
```python
first_row = df.iloc[0]  # First row
specific_rows = df.iloc[1:3]  # Second and third rows
```

### Selecting Rows by Condition
```python
high_salary = df[df["Salary"] > 60000]
```

### Adding a New Column
```python
df["Bonus"] = df["Salary"] * 0.10
```

### Dropping a Column
```python
df = df.drop(columns=["Bonus"])
```

---

## 4. Handling Missing Data

### Checking for Missing Values
```python
df.isnull().sum()
```

### Filling Missing Values
```python
df.fillna(value={"Salary": df["Salary"].mean()}, inplace=True)
```

### Dropping Rows with Missing Values
```python
df.dropna(inplace=True)
```

---

## 5. Grouping and Aggregation

### Group by a Column and Compute Aggregates
```python
df_grouped = df.groupby("Age")["Salary"].mean()
```

### Multiple Aggregations
```python
df_agg = df.groupby("Age").agg({"Salary": ["mean", "max", "min"]})
```

---

This guide covers essential pandas commands for statistical analysis and data manipulation. Let me know if you need additional explanations or examples!


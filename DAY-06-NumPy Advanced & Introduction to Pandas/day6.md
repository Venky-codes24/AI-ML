# 📘 Day 6 Notes – NumPy Advanced & Introduction to Pandas

## 📅 Day 6 Topics

* Indexing in NumPy
* Slicing in NumPy
* Working with 2D & 3D Arrays
* Joining Arrays
* NumPy Random Module
* Introduction to Pandas
* Reading Data from CSV, Excel, and JSON Files
* Exploring DataFrames

---

# 1️⃣ Indexing in NumPy

Indexing is used to access a specific element from an array.

## 1D Array

```python
import numpy as np

arr = np.array([10, 20, 30, 40])

print(arr[2])
```

**Output**

```text
30
```

---

## 2D Array

Syntax

```python
array[row, column]
```

Example

```python
arr2D = np.array([
    [1,2,3,4],
    [5,6,7,8]
])

print(arr2D[1,3])
print(arr2D[0,1])
```

**Output**

```text
8
2
```

---

## 3D Array

Syntax

```python
array[block, row, column]
```

Example

```python
arr3D = np.array([
    [[1,2],[3,4]],
    [[5,6],[7,8]]
])

print(arr3D[1,1,0])
```

**Output**

```text
7
```

---

# 2️⃣ Slicing in NumPy

Slicing is used to select a range of elements.

## Syntax

```python
array[start:end]
```

* Start → Included
* End → Excluded

---

### Example (2D Array)

```python
arr2D[:,1:4]
```

This means:

* Select all rows (`:`)
* Select columns from index 1 to 3

---

# 3️⃣ Quick Rules for Indexing

| Array Type | Syntax                    |
| ---------- | ------------------------- |
| 1D         | `arr[index]`              |
| 2D         | `arr[row, column]`        |
| 3D         | `arr[block, row, column]` |

---

# 4️⃣ Joining Arrays

NumPy provides multiple ways to combine arrays.

## Using `concatenate()`

```python
arr1 = np.array([1,2,3])

arr2 = np.array([4,5,6])

joined = np.concatenate((arr1, arr2))

print(joined)
```

Output

```text
[1 2 3 4 5 6]
```

---

## Using `vstack()`

Used to join arrays vertically.

```python
arr1 = np.array([[1,2],
                 [3,4]])

arr2 = np.array([[5,6],
                 [7,8]])

joined = np.vstack((arr1, arr2))

print(joined)
```

Output

```text
[[1 2]
 [3 4]
 [5 6]
 [7 8]]
```

---

# 5️⃣ NumPy Random Module

The `random` module generates random numbers.

Example

```python
from numpy import random

x = random.randint(100)

print(x)
```

This generates a random integer between **0 and 99**.

---

# 6️⃣ Introduction to Pandas

**Pandas** is a Python library used for handling and analyzing structured data.

It is mainly used for:

* Reading datasets
* Cleaning data
* Filtering data
* Data Analysis
* Machine Learning preprocessing

Import Pandas

```python
import pandas as pd
```

---

# 7️⃣ Reading CSV Files

```python
import pandas as pd

df = pd.read_csv("students_dirty_data.csv")
```

`read_csv()` reads CSV files into a **DataFrame**.

---

# 8️⃣ Reading Excel Files

```python
df = pd.read_excel("flipkart_sales_data.xlsx")
```

Used to load Excel spreadsheets.

---

# 9️⃣ Reading JSON Files

### From a URL

```python
df = pd.read_json("https://jsonplaceholder.typicode.com/todos")
```

---

### From a Local File

```python
df = pd.read_json("okay_json.json")
```

---

# 🔟 Viewing Data

## First 5 Rows

```python
df.head()
```

---

## First 10 Rows

```python
df.head(10)
```

---

## Last 5 Rows

```python
df.tail()
```

These methods help quickly inspect a dataset.

---

# 1️⃣1️⃣ Shape of Data

```python
df.shape
```

Returns

```text
(rows, columns)
```

Example

```text
(100, 5)
```

Meaning:

* 100 Rows
* 5 Columns

---

# 1️⃣2️⃣ Dataset Information

```python
df.info()
```

Provides:

* Number of rows
* Number of columns
* Column names
* Data types
* Missing values
* Memory usage

### Note

If a column's data type is **object**, it usually contains text (strings or labels).

---

# 1️⃣3️⃣ Statistical Summary

```python
df.describe()
```

Displays statistics for numerical columns such as:

* Count
* Mean
* Standard Deviation
* Minimum
* Maximum
* 25%
* 50% (Median)
* 75%

---------

# ⭐ Key Takeaways

* Learned indexing and slicing for **1D, 2D, and 3D NumPy arrays**.
* Understood how to join arrays using `concatenate()` and `vstack()`.
* Used NumPy's `random` module to generate random numbers.
* Learned the basics of **Pandas** for data analysis.
* Read datasets from **CSV, Excel, and JSON** files.
* Explored datasets using `head()`, `tail()`, `shape`, `info()`, and `describe()`.

---

# 📚 Day 6 Summary

Today I explored advanced **NumPy operations**, including indexing, slicing, joining arrays, and generating random numbers. I also started learning **Pandas**, a powerful library for data analysis. I learned how to load datasets from CSV, Excel, and JSON files, inspect data using `head()` and `tail()`, understand dataset dimensions with `shape`, check data types using `info()`, and generate statistical summaries with `describe()`. These concepts are the foundation of data preprocessing in AI, Machine Learning, and Data Science.

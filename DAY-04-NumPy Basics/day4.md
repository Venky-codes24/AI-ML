# 📘 Day 4 Notes – NumPy Basics (AI & ML Training)

## 📅 Day 4 Topics

* Why NumPy?
* List vs Tuple vs NumPy Array
* Memory Allocation
* Shape and Dimensions
* Creating NumPy Arrays
* Reshape
* Flatten
* Indexing & Slicing
* Joining Arrays

---

# 1️⃣ Why NumPy?

**NumPy (Numerical Python)** is a Python library used for performing mathematical and numerical operations efficiently.

### Advantages

* Faster than Python Lists
* Uses less memory
* Better performance
* Used in AI, Machine Learning, Data Science, and Deep Learning

---

# 2️⃣ List vs Tuple vs NumPy Array

| Feature           | List  | Tuple  | NumPy Array                 |
| ----------------- | ----- | ------ | --------------------------- |
| Mutable           | ✅ Yes | ❌ No   | ✅ Yes                       |
| Stores References | ✅ Yes | ✅ Yes  | ❌ Stores values efficiently |
| Memory Efficient  | ❌     | Better | ✅ Best                      |
| Speed             | Slow  | Medium | Fast                        |

### Important Points

* Lists use **over-allocation** (extra memory is reserved).
* Tuples reduce over-allocation but still store object references.
* NumPy arrays store data in continuous memory, making them much faster.

---

# 3️⃣ Memory Allocation

Python Lists increase their memory size automatically when new elements are added.

Example:

```python
my_list = []

my_list.append(10)
my_list.append(20)
my_list.append(30)
```

Each append may increase allocated memory.

NumPy arrays do not over-allocate memory like lists, making them more memory efficient.

---

# 4️⃣ Creating NumPy Arrays

```python
import numpy as np

arr = np.array([1,2,3,4])
```

### Creating Different Dimensions

### 1D Array

```python
arr1 = np.array([1,2,3,4])
```

### 2D Array

```python
arr2 = np.array([
    [1,2,3],
    [4,5,6]
])
```

### 3D Array

```python
arr3 = np.array([
    [[1,2],[3,4]],
    [[5,6],[7,8]]
])
```

---

# 5️⃣ Shape and Dimensions

### shape

Returns the number of elements in each dimension.

Example

```python
arr.shape
```

Output

```
(2,3)
```

Meaning:

* 2 Rows
* 3 Columns

---

### ndim

Returns the number of dimensions.

```python
arr.ndim
```

Example

| Array         | ndim |
| ------------- | ---- |
| [1,2,3]       | 1    |
| [[1,2],[3,4]] | 2    |
| [[[1]]]       | 3    |

---

# 6️⃣ Creating NumPy Array from Tuple

```python
tup = (10,20,30)

arr = np.array(tup)
```

NumPy can easily convert tuples into arrays.

---

# 7️⃣ Reshape

Used to change the dimensions of an array without changing its data.

Syntax

```python
array.reshape(rows, columns)
```

Example

```python
arr = np.array([1,2,3,4,5,6])

arr.reshape(2,3)
```

Output

```
[[1 2 3]
 [4 5 6]]
```

### Rule

```
Rows × Columns = Total Elements
```

Example

12 elements can become

* 3 × 4
* 4 × 3
* 2 × 6
* 6 × 2
* 1 × 12
* 12 × 1

---

# 8️⃣ Flatten

Converts a multi-dimensional array into a 1D array.

Example

```python
arr.flatten()
```

Input

```
[[1,2],
 [3,4]]
```

Output

```
[1 2 3 4]
```

---

# 9️⃣ Indexing

Used to access individual elements.

Example

```python
arr = np.array([10,20,30])

print(arr[0])
```

Output

```
10
```

For 2D arrays

```python
arr[1][0]
```

---

# 🔟 Slicing

Used to access multiple elements.

Example

```python
arr[1:4]
```

Output

```
[20 30 40]
```

For 2D arrays

```python
arr[:,1]
```

Returns the second column.

---

# 1️⃣1️⃣ Joining Arrays

Used to combine two or more arrays.

Example

```python
arr1 = np.array([1,2,3])

arr2 = np.array([4,5,6])

np.concatenate((arr1, arr2))
```

Output

```
[1 2 3 4 5 6]
```

---

# ⭐ Key Takeaways

* NumPy is faster and more memory-efficient than Python lists.
* Lists over-allocate memory, while NumPy uses continuous memory.
* `shape` gives the size of each dimension.
* `ndim` gives the number of dimensions.
* `reshape()` changes the array's dimensions without changing the data.
* `flatten()` converts any array into a 1D array.
* Indexing accesses individual elements.
* Slicing accesses a range of elements.
* `concatenate()` joins multiple arrays.

---

## 📚 Day 4 Summary

Today I learned the basics of **NumPy**, including why it is preferred over Python lists for AI and ML. I explored the differences between **Lists, Tuples, and NumPy Arrays**, understood **memory allocation**, created **1D, 2D, and 3D arrays**, learned about **shape** and **dimensions**, practiced **reshape()**, **flatten()**, **indexing**, **slicing**, and finally learned how to **join arrays**. These concepts form the foundation for working with data efficiently in Machine Learning.

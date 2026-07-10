# Day 2: Python Data Structures and Functions

## 1. Python Data Structures

Data structures are ways to store and organize data efficiently in Python.

### List
A list is an ordered, changeable collection of items.

```python
numbers = [10, 20, 30]
print(numbers)
```

### Tuple
A tuple is an ordered, unchangeable collection of items.

```python
tuple_example = (1, 2, 3)
print(tuple_example)
```

### Dictionary
A dictionary stores data as key-value pairs.

```python
student = {"name": "Venky", "age": 21}
print(student["name"])
```

### Set
A set is an unordered collection of unique items.

```python
colors = {"red", "green", "blue"}
print(colors)
```

---

## 2. Functions in Python

A function is a block of reusable code that performs a specific task.

### Defining a Function

```python
def greet(name):
    print("Hello, " + name)


greet("Alice")
```

### Function with Return Value

```python
def add(a, b):
    return a + b

result = add(3, 5)
print(result)
```

---

## 3. Parameters and Arguments

- Parameters are variables listed inside the function definition.
- Arguments are the values passed to the function.

```python
def multiply(x, y):
    return x * y

print(multiply(4, 6))
```

---

## 4. Built-in Functions

Python provides many built-in functions such as:

- `len()`
- `max()`
- `min()`
- `sum()`
- `type()`

```python
numbers = [1, 2, 3, 4]
print(len(numbers))
print(sum(numbers))
```

---

## 5. Summary

Today we learned about:

- Lists
- Tuples
- Dictionaries
- Sets
- Functions
- Parameters and return values

These concepts are the foundation for writing organized and reusable Python programs.

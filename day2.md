# Day 2: Python Data Structures and Functions

## 1. Set in Python

### Definition

A **set** is an unordered and mutable collection of unique elements.

### Characteristics

* Mutable: Yes
* Duplicates: No
* Ordered: No

### Syntax

```python
my_set = {1, 2, 3}
```

### Example

```python
fruits = {"apple", "banana", "mango"}
print(fruits)
```

### Output

```text
{'banana', 'apple', 'mango'}
```

> Note: The order may vary because sets are unordered.

### Duplicate Example

```python
numbers = {1, 2, 3, 2, 1}
print(numbers)
```

### Output

```text
{1, 2, 3}
```

### Adding Elements

```python
s = {1, 2, 3}
s.add(4)
print(s)
```

### Output

```text
{1, 2, 3, 4}
```

---

# 2. Dictionary in Python

## Definition

A dictionary is an unordered and mutable collection of key-value pairs.

### Characteristics

* Mutable: Yes
* Keys: Must be unique
* Values: Duplicates allowed
* Stores data in key-value format

### Syntax

```python
student = {
    "name": "Venky",
    "age": 21,
    "course": "AIML"
}
```

### Example

```python
print(student["name"])
```

### Output

```text
Venky
```

### Adding a New Item

```python
student["cgpa"] = 8.5
print(student)
```

### Output

```text
{'name': 'Venky', 'age': 21, 'course': 'AIML', 'cgpa': 8.5}
```

### Duplicate Keys

```python
d = {
    "a": 1,
    "a": 2
}
print(d)
```

### Output

```text
{'a': 2}
```

---

# 3. Loops in Python

## Definition

A loop is used to execute a block of code repeatedly.

## Types of Loops

1. for loop
2. while loop

---

## for Loop

### Syntax

```python
for variable in sequence:
    # code
```

### Example

```python
for i in range(5):
    print(i)
```

### Output

```text
0
1
2
3
4
```

---

## while Loop

### Syntax

```python
while condition:
    # code
```

### Example

```python
i = 1

while i <= 5:
    print(i)
    i += 1
```

### Output

```text
1
2
3
4
5
```

---

# 4. Functions in Python

## Definition

A function is a reusable block of code that performs a specific task.

### Syntax

```python
def function_name():
    # code
```

### Example

```python
def greet():
    print("Hello, Python!")

greet()
```

### Output

```text
Hello, Python!
```

---

## Function with Parameters

```python
def greet(name):
    print("Hello,", name)

greet("Venky")
```

### Output

```text
Hello, Venky
```

---

## Function with Return Value

```python
def add(a, b):
    return a + b

result = add(10, 20)
print(result)
```

### Output

```text
30
```

---

# 5. Default Parameters

## Definition

A default parameter is a parameter that has a predefined value.

### Syntax

```python
def function_name(parameter=default_value):
    # code
```

### Example

```python
def greet(name="Guest"):
    print("Hello,", name)

greet()
greet("Venky")
```

### Output

```text
Hello, Guest
Hello, Venky
```

---

# 6. Mutable and Immutable Objects

## Mutable Objects

Objects that can be changed after creation.

### Examples

* List
* Dictionary
* Set

```python
numbers = [1, 2, 3]
numbers.append(4)
print(numbers)
```

### Output

```text
[1, 2, 3, 4]
```

---

## Immutable Objects

Objects that cannot be changed after creation.

### Examples

* Integer
* Float
* String
* Tuple
* Boolean

```python
name = "Python"
name = name + " Programming"

print(name)
```

### Output

```text
Python Programming
```

---

## Mutable vs Immutable

| Feature      | Mutable                | Immutable                       |
| ------------ | ---------------------- | ------------------------------- |
| Modification | Allowed                | Not Allowed                     |
| Memory       | Same object can change | New object created              |
| Examples     | List, Dict, Set        | String, Tuple, Int, Float, Bool |

---

# Homework: How to Avoid the Mutable Default Parameter Pitfall?

## Problem

```python
def add_item(item, my_list=[]):
    my_list.append(item)
    return my_list

print(add_item(1))
print(add_item(2))
```

### Output

```text
[1]
[1, 2]
```

The same list is reused in every function call.

---

## Correct Way

```python
def add_item(item, my_list=None):
    if my_list is None:
        my_list = []

    my_list.append(item)
    return my_list

print(add_item(1))
print(add_item(2))
```

### Output

```text
[1]
[2]
```

### Why?

Using `None` creates a new list every time the function is called.

---

# Day 2 Summary

✔ Set in Python
✔ Dictionary in Python
✔ for Loop and while Loop
✔ Functions in Python
✔ Function Parameters and Return Values
✔ Default Parameters
✔ Mutable and Immutable Objects
✔ Mutable Default Parameter Pitfall and Its Solution

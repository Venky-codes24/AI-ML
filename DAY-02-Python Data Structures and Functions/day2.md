# Day 2: Python Data Structures and Functions

## 1. Set in Python

### Definition
A **set** is an unordered and mutable collection of unique elements.

### Characteristics

- Mutable: Yes
- Duplicates: No
- Ordered: No

### Syntax

```
my_set = {1, 2, 3}
```

### Example

```
fruits = {"apple", "banana", "mango"}
print(fruits)
```

### Output

```
{'banana', 'apple', 'mango'}
```

> Note: The order may vary because sets are unordered.

### Duplicate Example

```
numbers = {1, 2, 3, 2, 1}
print(numbers)
```

### Output

```
{1, 2, 3}
```

### Adding Elements

```
s = {1, 2, 3}
s.add(4)
print(s)
```

### Output

```
{1, 2, 3, 4}
```

---

# 2. Dictionary in Python

## Definition
A dictionary is an unordered and mutable collection of key-value pairs.

### Characteristics

- Mutable: Yes
- Keys: Must be unique
- Values: Duplicates allowed
- Stores data in key-value format

### Syntax

```
student = {
    "name": "Venky",
    "age": 21,
    "course": "AIML"
}
```

### Example

```
print(student["name"])
```

### Output

```
Venky
```

### Adding a New Item

```
student["cgpa"] = 8.5
print(student)
```

### Output

```
{'name': 'Venky', 'age': 21, 'course': 'AIML', 'cgpa': 8.5}
```

### Duplicate Keys

```
d = {
    "a": 1,
    "a": 2
}
print(d)
```

### Output

```
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

```
for variable in sequence:
    # code
```

### Example

```
for i in range(5):
    print(i)
```

### Output

```
0
1
2
3
4
```

---

## while Loop

### Syntax

```
while condition:
    # code
```

### Example

```
i = 1

while i <= 5:
    print(i)
    i += 1
```

### Output

```
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

```
def function_name():
    # code
```

### Example

```
def greet():
    print("Hello, Python!")

greet()
```

### Output

```
Hello, Python!
```

---

## Function with Parameters

```
def greet(name):
    print("Hello,", name)

greet("Venky")
```

### Output

```
Hello, Venky
```

---

## Function with Return Value

```
def add(a, b):
    return a + b

result = add(10, 20)
print(result)
```

### Output

```
30
```

---

# 5. Default Parameters

## Definition
A default parameter is a parameter that has a predefined value.

### Syntax

```
def function_name(parameter=default_value):
    # code
```

### Example

```
def greet(name="Guest"):
    print("Hello,", name)

greet()
greet("Venky")
```

### Output

```
Hello, Guest
Hello, Venky
```

---

# 6. Mutable and Immutable Objects

## Mutable Objects
Objects that can be changed after creation.

### Examples

- List
- Dictionary
- Set

```
numbers = [1, 2, 3]
numbers.append(4)
print(numbers)
```

### Output

```
[1, 2, 3, 4]
```

---

## Immutable Objects
Objects that cannot be changed after creation.

### Examples

- Integer
- Float
- String
- Tuple
- Boolean

```
name = "Python"
name = name + " Programming"

print(name)
```

### Output

```
Python Programming
```

---

## Mutable vs Immutable
FeatureMutableImmutableModificationAllowedNot AllowedMemorySame object can changeNew object createdExamplesList, Dict, SetString, Tuple, Int, Float, Bool
---

# Homework: How to Avoid the Mutable Default Parameter Pitfall?

## Problem

```
def add_item(item, my_list=[]):
    my_list.append(item)
    return my_list

print(add_item(1))
print(add_item(2))
```

### Output

```
[1]
[1, 2]
```
The same list is reused in every function call.

---

## Correct Way

```
def add_item(item, my_list=None):
    if my_list is None:
        my_list = []

    my_list.append(item)
    return my_list

print(add_item(1))
print(add_item(2))
```

### Output

```
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

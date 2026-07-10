# Day 1: Python Fundamentals

## What is Python?
Python is a high-level, interpreted, general-purpose, and object-oriented programming language created by Guido van Rossum and released in 1991.

Python is known for:

- Simple and readable syntax
- Easy to learn and use
- Large collection of libraries and frameworks
- Cross-platform support (Windows, Linux, macOS)
- Rapid application development

---

## Why is Python Popular?
Python is widely used in:

- Web Development
- Data Science and Analytics
- Artificial Intelligence (AI)
- Machine Learning (ML)
- Automation and Scripting
- Software Development
- Game Development
- Testing and DevOps

---

## Features of Python

1. Simple and Easy to Learn
2. High-Level Language
3. Interpreted Language
4. Object-Oriented Programming Support
5. Dynamically Typed
6. Portable and Platform Independent
7. Open Source and Free
8. Large Standard Library
9. Automatic Memory Management
10. Supports Multiple Programming Paradigms

---

# How Python Works

## Step 1: Write Python Code

```python
print("Hello, World!")
```

## Step 2: Compilation to Bytecode
Python first converts the source code into Bytecode (.pyc).

## Step 3: Python Virtual Machine (PVM)
The Python Virtual Machine (PVM) executes the bytecode line by line and produces the output.

### Flow:

```text
Source Code (.py)
        ↓
Bytecode (.pyc)
        ↓
Python Virtual Machine (PVM)
        ↓
Output
```

---

# Interpreter

## Definition
An interpreter is a program that translates and executes code line by line.

## Advantages

- Easy debugging
- Immediate error reporting
- Platform independent

## Disadvantages

- Slower execution than compiled languages

---

# Why is Python Slow?
Python is slower because:

1. It is an interpreted language.
2. It is dynamically typed.
3. It performs automatic memory management.
4. Code executes through the Python Virtual Machine (PVM).
5. High-level abstractions introduce additional overhead.

---

# Disadvantages (Cons) of Python

1. Slower execution speed
2. Higher memory consumption
3. Not commonly used for mobile app development
4. Less suitable for high-performance systems programming
5. Some errors are detected only at runtime
6. Global Interpreter Lock (GIL) limitations
7. Weaker performance for CPU-intensive multithreading

---

# Global Interpreter Lock (GIL)

## Definition
The Global Interpreter Lock (GIL) is a mechanism in CPython that allows only one thread to execute Python bytecode at a time.

## Effect

- CPU-bound tasks do not get true parallel execution using threads.
- I/O-bound tasks still benefit from multithreading.

---

# Compile-Time Error vs Run-Time Error

| Compile-Time Error | Run-Time Error |
|--------------------|----------------|
| Occurs before execution | Occurs during execution |
| Prevents program execution | Program starts and then crashes |
| Example: Syntax Error | Example: Division by Zero |

## Example: Compile-Time Error

```python
print("Hello"
```

Output:

```text
SyntaxError
```

## Example: Run-Time Error

```python
a = 10
b = 0
print(a / b)
```

Output:

```text
ZeroDivisionError
```

---

# Variables in Python

## Definition
A variable is a name used to store data in memory.

## Syntax

```python
name = "Venky"
age = 21
cgpa = 8.5
```

## Multiple Assignment

```python
a, b, c = 1, 2, 3
x = y = z = 100
```

## Rules

- Must start with a letter or underscore
- Cannot start with a number
- Can contain letters, numbers, and underscores
- Case-sensitive

## Dynamic Typing

```python
x = 10
x = "Hello"
```

---

# String Concatenation

## Definition
Concatenation means joining two or more strings.

## Example

```python
first = "Hello"
second = "World"

print(first + " " + second)
```

Output:

```text
Hello World
```

---

# Slicing in Python

## Definition
Slicing extracts a portion of a sequence.

## Syntax

```python
sequence[start:stop:step]
```

## Examples

```python
text = "Python"

print(text[0:3])   # Pyt
print(text[:4])    # Pyth
print(text[2:])    # thon
print(text[::2])   # Pto
print(text[::-1])  # nohtyP
print(text[0:-2])  # Pyth
```

### Negative Indexing

```text
 P   y   t   h   o   n
 0   1   2   3   4   5
-6  -5  -4  -3  -2  -1
```

---

# Boolean in Python

## Definition
Boolean is a data type that has only two values:

- True
- False

## Examples

```python
print(10 > 5)
print(10 < 5)
```

Output:

```text
True
False
```

## Boolean Values

```python
print(bool([]))
print(bool(""))
print(bool(0))
print(bool(369))
```

Output:

```text
False
False
False
True
```

## Important Point

```python
True = 1
False = 0
```

Example:

```python
print(True + False + True)
```

Output:

```text
2
```

## Equality Examples

```python
print(True == 1)
print(False == 0)
```

Output:

```text
True
True
```

## Difference Between `==` and `is`

```python
print(True == 1)   # True
print(True is 1)   # False
```

- `==` → Checks value equality
- `is` → Checks object identity

---

# Short-Circuit Evaluation

## Definition
Python stops evaluating a logical expression when the final result is already determined.

## Examples

```python
print(False and (10 / 0))
```

Output:

```text
False
```

```python
print(True or (10 / 0))
```

Output:

```text
True
```

---

# Difference Between List and Array

| Feature | List | Array |
|--------|------|-------|
| Data Types | Different types allowed | Same type only |
| Memory Usage | More | Less |
| Performance | Slower | Faster |
| Built-in | Yes | Requires `array` module |

---

# Tuple in Python

## Definition
A tuple is an ordered and immutable collection of elements.

## Example

```python
t = (10, "Python", 3.14, True)
print(t)
```

Output:

```text
(10, 'Python', 3.14, True)
```

## Characteristics

- Ordered
- Immutable
- Allows duplicate values
- Supports indexing and slicing
- Can store different data types

## Single-Element Tuple

```python
t = (10,)
print(type(t))
```

Output:

```python
<class 'tuple'>
```

---

# Day 1 Summary

✔ What is Python
✔ Features of Python
✔ Applications of Python
✔ How Python Works (Bytecode and PVM)
✔ Interpreter
✔ Why Python is Slow
✔ Disadvantages of Python
✔ Global Interpreter Lock (GIL)
✔ Compile-Time Error vs Run-Time Error
✔ Variables and Dynamic Typing
✔ String Concatenation
✔ Slicing and Negative Indexing
✔ Boolean Data Type
✔ `==` vs `is`
✔ Short-Circuit Evaluation
✔ Difference Between List and Array
✔ Tuple and Its Characteristics

# Python Basics

This folder contains my Python fundamentals for Machine Learning.

## Topics

- [Comments](#comments)
- [Variables & Data Types](#variables--data-types)
- [In-Depth Strings](#in-depth-strings)
- [Print Statements](#print-statements)
- [Type Conversion & Boolean Values](#type-conversion--boolean-values)
- [Input Statements](#input-statements)
- [Loops](#loops)
- [Functions](#functions)
- [Data Structures](#data-structures)
- [File I/O](#file-io)
- [Tell, Seek & Read Position](#tell-seek--read-position)
- [Error Handling](#error-handling)
- [Object-Oriented Programming (OOP)](#object-oriented-programming-oop)


# Comments

-Explain what comments are in Python and why they are used.

Comments are notes in your code that Python ignores. They help explain what your code does.

## Single-Line Comments

Use `#` for single-line comments:

```python
# This is a comment

name = "Nijhum"  # This is also a comment

# Comments can be on their own line
age = 25
```
### Explanation


- `#` is used to start a comment in Python.
- Python ignores everything after `#` on the same line.
- Comments help make your code easier to read and understand.

## Multi-Line comments

Use triple quotes """ or ''' for multi-line comments:
```python
"""
This is a multi-line comment.
It can span multiple lines.
Useful for documentation.
"""

print("Hello, World!")
```

### Explanation


- Triple quotes (`"""` or `'''`) are used to write text on multiple lines.
- They are commonly used to describe functions, classes, or modules.
- They make your code easier to understand and maintain.

---

# Variables & Data Types

-Learn how variables store data and explore Python's built-in data types.

Variables store data values. In Python, you don't need to declare variable types.

```python
# Assigning values
name="Nijhum"
age=25
height=5.3
is_student=True

print(name)    # Output: Nijhum
print(age)     # Output: 25
print(height)  # Output: 5.3
print(is_student)  # Output: True
```

## Variable Naming Rules

### 1.Must start with a letter or underscore - Cannot start with a number
```python
valid_name = "OK"
_valid = "OK"
# 2invalid = "Error!"  # This will cause an error
```
### 2.Can contain letters, numbers, and underscores - No spaces or special characters (except _)
```python
user_name = "OK"
user_name_2 = "OK"
# user name = "Error!"  # Spaces not allowed
# user-name = "Error!"  # Hyphens not allowed
```

### 3.Case-sensitive - name and Name are different variables
```python
name = "Noshin"
Name = "Nijhum"
print(name)  # Output: Noshin
print(Name)  # Output: Nijhum
```

### 4.Cannot use Python keywords - Don't use words like if, for, def, class, etc
```python
# if = 10  # Error! 'if' is a keyword
# def = "test"  # Error! 'def' is a keyword

```

## Common Python Keywords
```python
# These are reserved words in Python
# False, None, True, and, as, assert, async, await, break, class, continue, def, del, elif, else, except, finally, for, from, global, if, import, in, is, lambda, nonlocal, not, or, pass, raise, return, try, while, with, yield
```

## Data type

### 1.Numbers
```python
# Integers
x = 10
y = -5

# Floats (decimals)
pi = 3.14
temperature = -10.5

# Complex numbers
z = 3 + 4j

# Type checking
print(type(x))  # Output: <class 'int'>
print(type(pi))  # Output: <class 'float'>
```

### 2.Strings
```python
# Single or double quotes
name1 = "Nijhum"
name2 = 'Noshin'

# String operations
full_name = name1 + " " + name2  # Concatenation
print(full_name)  # Output: Nijhum Noshin

# String methods
text = "Hello World"
print(text.upper())      # Output: HELLO WORLD
print(text.lower())      # Output: hello world
print(text.replace("World", "Python"))  # Output: Hello Python
print(len(text))         # Output: 11
```

### 3. Booleans
```python
is_true = True
is_false = False

# Boolean operations
result = is_true and is_false  # False
result = is_true or is_false   # True
result = not is_true           # False
```

### 4.Type Conversion

```python
# Convert between types
x = "123"
y = int(x)      # Convert to integer: 123
z = float(x)    # Convert to float: 123.0
w = str(123)    # Convert to string: "123"
```
---

# In-Depth Strings

-Understand string creation, indexing, slicing, methods, formatting, and operations.

Strings are sequences of characters. Each character has an index (position).

### Positive Indexing(Left to right)
```python
text = "hello"
# Index:  0  1  2  3  4
# Value:  h  e  l  l  o

print(text[0])  # Output: h
print(text[1])  # Output: e
print(text[4])  # Output: o
```

### Negative Indexing (Right to Left):
```python
text = "hello"
# Index:  -5 -4 -3 -2 -1
# Value:   h  e  l  l  o

print(text[-1])  # Output: o (last character)
print(text[-2])  # Output: l (second to last)
print(text[-5])  # Output: h (first character)
```
### string slicing

[start:stop:step]:
```python
text = "yoo brother"

# Basic slicing
print(text[0:3])    # Output: yoo (indices 0, 1, 2)
print(text[4:11])   # Output: brother (indices 4 to 10)
print(text[:3])     # Output: yoo (from start to index 2)
print(text[4:])     # Output: brother (from index 4 to end)
print(text[:])      # Output: yoo brother (entire string)

# With step
print(text[0:11:2])  # Output: yo rte (every 2nd character)
print(text[::2])     # Output: yo rte (every 2nd character from start to end)
print(text[::-1])    # Output: rehtorb ooy (reverse string)
```

### String Immutability

Strings are immutable - they cannot be changed after creation:

```python
text = "hello"
# text[0] = "H"  # Error! Cannot modify string

# Instead, create a new string
text = "H" + text[1:]  # Creates new string: "Hello"
print(text)  # Output: Hello
```

##  Why Are Strings Immutable?

### Explanation
- **Data Safety:** The original string cannot be changed by mistake.
- **Better Performance:** Python can reuse the same string in memory, making programs more efficient.
- **Reliable Behavior:** Strings stay the same throughout the program, reducing unexpected bugs.
- **Dictionary Keys:** Immutable strings can safely be used as dictionary keys.
- **Thread Safety:** Multiple parts of a program can use the same string without changing it.



---

# Print Statements

Learn how to display output using the `print()` function.

### Basic Print
```python
print("Nijhum")
print(100)
print(3.14)
```

### print multiple items
```python
name = "Alice"
age = 25
print("Name:", name, "Age:", age)  # Output: Name: Alice Age: 25
```

### slicing concatenation
```python
first_name = "Noshin"
last_name = "Nijhum"
full_name = first_name + " " + last_name
print(full_name)  # Output: Noshin Nijhum

# Note: Can only concatenate strings with strings
# print("Age: " + 25)  # Error! Need to convert to string
print("Age: " + str(25))  # Output: Age: 25
```

### Formatted Strings (f-strings)

```python
name = "Alice"
age = 25
city = "New York"

# f-string syntax
message = f"Hello, {name}! You are {age} years old and live in {city}."
print(message)  # Output: Hello, Alice! You are 25 years old and live in New York.

# Can include expressions
print(f"Next year you'll be {age + 1}")  # Output: Next year you'll be 26

# Formatting numbers
pi = 3.14159
print(f"Pi is approximately {pi:.2f}")  # Output: Pi is approximately 3.14
```

### Raw Strings
```python
# Regular string
path1 = "C:\\Users\\Alice\\Documents"  # Need double backslashes
print(path1)  # Output: C:\Users\Alice\Documents

# Raw string (prefix with 'r')
path2 = r"C:\Users\Alice\Documents"  # No need to escape
print(path2)  # Output: C:\Users\Alice\Documents

# Useful for regex patterns
import re
pattern = r"\d+"  # Matches one or more digits
```


---

# Type Conversion & Boolean Values

Understand type casting and how Boolean values work in Python.

### Type Conversion Functions
```python
# Convert to integer
x = int("123")      # 123
x = int(3.14)       # 3 (truncates decimal)
# x = int("abc")    # Error! Cannot convert

# Convert to float
y = float("3.14")   # 3.14
y = float(5)        # 5.0

# Convert to string
z = str(123)        # "123"
z = str(3.14)       # "3.14"
z = str(True)       # "True"

# Convert to boolean
w = bool(1)         # True
w = bool(0)         # False
w = bool("hello")   # True
w = bool("")        # False
```

## Truthy and Falsy Values
-In Python, values are evaluated as True or False in boolean contexts

### Falsy Values (evaluate to False):

```python
# All of these are falsy
bool(False)      # False
bool(None)       # False
bool(0)          # False
bool(0.0)        # False
bool(0j)         # False (complex zero)
bool("")         # False (empty string)
bool([])         # False (empty list)
bool({})         # False (empty dictionary)
bool(())         # False (empty tuple)
bool(set())      # False (empty set)
```
### Truthy Values (evaluate to True):
```python
# Everything else is truthy
bool(True)       # True
bool(1)          # True
bool(-1)         # True
bool(3.14)       # True
bool("hello")    # True
bool([1, 2, 3])  # True
bool({"a": 1})   # True
```

---

# Input Statements

Learn how to take user input using the `input()` function.

---

# Loops

Explore `for` loops, `while` loops, and loop control statements.

---

# Functions

Learn how to create reusable functions using `def`.

---

# Data Structures

Understand Lists, Tuples, Sets, Dictionaries, and their operations.

---

# File I/O

Learn how to create, read, write, and append files in Python.

---

# Tell, Seek & Read Position

Understand file pointer operations using `tell()` and `seek()`.

---

# Error Handling

Learn how to handle exceptions using `try`, `except`, `else`, and `finally`.

---

# Object-Oriented Programming (OOP)

Learn Classes, Objects, Constructors, Inheritance, Encapsulation, Polymorphism, and Abstraction.

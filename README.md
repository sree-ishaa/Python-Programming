# Python Programming Concepts:

## Table of Contents
- [Introduction](#introduction)
  
  -[Comments](#Comments)
  
- [Why Indentation Matters in Python](#Why-Indentation-Matters-in-Python)
- [Indentation](#indentation)
- [List-of-Python-Data-Types](#List-of-Python-Data-Types)
  
  -[Dictionary](#Dictionary)
  
  -[list-and-tuple](#list-and-tuple)

  -[Type-of-loops-in-python](#Type-of-loops-in-python)

  -[for-loops-and-while-loops](#for-loops-and-while-loops)

  -[Declaring-Functions-in-Python](#Declaring-Functions-in-Python)

    
- [Python-is-a-dynamically-typed-language](#python-is-a-dynamically-typed-language)
- [Concatenating-Strings-with-Other-Data-Types](#Concatenating-Strings-with-Other-Data-Types)

## Introduction

## 🐍 Introduction to Python

**Python** is a high-level, interpreted, general-purpose programming language known for its simplicity, readability, and versatility. It was created by **Guido van Rossum** and first released in **1991**. Python emphasizes code readability and allows developers to express concepts in fewer lines of code compared to many other languages.

---

## ✨ Key Features of Python

- **Simple and Easy to Learn**: Clean syntax that mimics natural language.
- **Interpreted Language**: No need to compile; code runs line by line.
- **Dynamically Typed**: No need to declare variable types explicitly.
- **High-Level Language**: Abstracts away low-level details like memory management.
- **Extensive Standard Library**: Comes with modules for everything from math to web development.
- **Cross-Platform**: Runs on Windows, macOS, Linux, and more.
- **Large Community**: Tons of resources, libraries, and frameworks.

---

## 🧰 What Can You Do with Python?

- **Web Development**: Using frameworks like Django and Flask.
- **Data Science & Machine Learning**: With libraries like NumPy, pandas, scikit-learn, TensorFlow.
- **Automation & Scripting**: Automate repetitive tasks and system operations.
- **Game Development**: Using libraries like Pygame.
- **Desktop Applications**: With toolkits like Tkinter or PyQt.
- **Networking, APIs, and Web Scraping**: Using `requests`, `BeautifulSoup`, and `asyncio`.

---

## 📦 Popular Python Libraries

| Category            | Libraries                             |
|---------------------|----------------------------------------|
| Web Development     | Flask, Django                          |
| Data Science        | pandas, NumPy, matplotlib               |
| Machine Learning    | scikit-learn, TensorFlow, PyTorch      |
| Automation          | Selenium, pyautogui, schedule          |
| APIs & Web Scraping | requests, BeautifulSoup, Scrapy        |

---

## 🚀 Why Learn Python?

- Beginner-friendly and widely taught in schools and universities.
- In-demand skill in tech, data science, AI, and automation.
- Huge ecosystem and community support.
- Great for prototyping and rapid development.

---
### Comments
**Comments in python**
In Python, **comments** are used to explain code, make it more readable, and help others (or your future self!) understand what the code is doing. Comments are ignored by the Python interpreter—they don’t affect how the program runs.

---

## 🗨️ Types of Comments in Python

### 1. **Single-Line Comments**
Use the `#` symbol to write a comment on a single line.

```python
# This is a single-line comment
x = 5  # This is an inline comment
```

📌 Use case: Explaining a line of code or marking a section.

---

### 2. **Multi-Line Comments (Block Comments)**
Python doesn’t have a specific syntax for multi-line comments, but you can use multiple `#` symbols:

```python
# This is a multi-line comment
# that spans several lines
# to explain something in detail
```

📌 Use case: Describing a block of logic or a function.

---

### 3. **Docstrings (Documentation Strings)**
Triple quotes (`'''` or `"""`) are used to document functions, classes, and modules. These are not technically comments—they are string literals—but they serve a similar purpose and can be accessed with tools like `help()`.

```python
def greet(name):
    """
    This function greets the user by name.
    """
    print(f"Hello, {name}!")
```

📌 Use case: Providing documentation for functions, classes, or modules.

---

## 🧠 Why Use Comments?

- ✅ Improve code readability
- ✅ Explain complex logic
- ✅ Mark TODOs or future improvements
- ✅ Help with debugging and maintenance

---

## ❌ What to Avoid

- Don’t over-comment obvious code:
  ```python
  x = 10  # Set x to 10  ← unnecessary
  ```
- Don’t leave outdated or misleading comments.
- Don’t use comments as a substitute for clean code.

---


## Python is a dynamically typed language

In Python, the interpreter automatically determines the data type of a variable at runtime based on the value you assign to it.
**Example**
x = 10        # Python knows this is an integer
x = "hello"   # Now x is a string
x = [1, 2, 3] # Now x is a list

### Optional Type Hints (Python 3.5+)
If you want more clarity or are working on a large project, you can use type hints to indicate expected types:
def greet(name: str) -> str:
    return "Hello, " + name

These hints don’t enforce types at runtime but help with readability and tools like linters or IDEs.

**Python allows you to assign values to multiple variables in a single line, which can make your code cleaner and more concise.**

Example:
x, y, z = 1, 2, 3
print(x, y, z)  # Output: 1 2 3

## Indentation
**Python Takes Indentation Seriously**

Unlike many other programming languages that use braces {} or keywords to define code blocks, Python uses indentation (whitespace at the beginning of a line) to define the structure of the code.
 ### ✅ Example:
if True:
    print("This is indented correctly")
    print("Still inside the if block")
print("Outside the if block")


### ❌ Incorrect Indentation:
if True:
print("This will cause an IndentationError")


Python will raise an IndentationError if the indentation is inconsistent or missing. This strictness enforces clean, readable code and avoids ambiguity.

🔧 Best Practices for Indentation
- Use 4 spaces per indentation level (the Python standard).
- Be consistent—don’t mix tabs and spaces.
- Most modern code editors handle this automatically.

In Python, you can concatenate (combine) different data types, but you need to be careful—Python doesn’t automatically convert types for you in all cases. Here's a breakdown of how to do it properly:

---

## Concatenating Strings with Other Data Types

If you try to directly concatenate a string with a non-string (like an integer or float), Python will raise a `TypeError`.

#### ❌ This will cause an error:
```python
name = "Alice"
age = 30
print("Name: " + name + ", Age: " + age)  # TypeError!
```

#### ✅ Correct way: Convert non-string to string using `str()`
```python
print("Name: " + name + ", Age: " + str(age))
```

---

### 🧩 Using f-strings (Recommended for Readability)

Python 3.6+ supports **f-strings**, which are a clean and powerful way to concatenate different data types:

```python
print(f"Name: {name}, Age: {age}")
```

This automatically converts variables to strings and inserts them into the sentence.

---

### 🧮 Concatenating Numbers

If you're working with numbers (integers, floats), you can add them directly:

```python
a = 10
b = 5.5
result = a + b  # result is 15.5
```

But if you try to concatenate a number with a string, you’ll need to convert one of them, depending on your goal.

---

### 📦 Concatenating Lists with Other Types

You can concatenate lists with other lists:

```python
list1 = [1, 2]
list2 = [3, 4]
combined = list1 + list2  # [1, 2, 3, 4]
```

But you can’t directly add a list and a string or number—you’d need to wrap the other value in a list first:

```python
list1 = [1, 2]
list1 += [3]  # OK
list1 += "a"  # Adds each character as an element: [1, 2, 3, 'a']
```

---

**Format()-Method**

The format() method in Python allows you to insert values into a string using placeholders {}. It automatically converts non-string data types (like integers, floats, or even objects) into strings when formatting.

**Example**
```python
price = 49.99
item = "Book"
print("The price of the {} is ${:.2f}".format(item, price))
```
**output**

The price of the Book is $49.99

**Example**

While format() is powerful and works in Python 2.7+, f-strings (Python 3.6+) are more concise:
f"I have {x} {y}"  # Equivalent to the format() example above

---

In Python, the built-in function type() is used to determine the data type of an object. It's a simple but powerful tool for debugging, introspection, and understanding how Python interprets your variables.
```python
x = 10
print(type(x))  # Output: <class 'int'>
```
```python
print(type("hello"))       # <class 'str'>
print(type(3.14))          # <class 'float'>
print(type([1, 2, 3]))     # <class 'list'>
print(type((1, 2)))        # <class 'tuple'>
print(type({"a": 1}))      # <class 'dict'>
print(type(True))          # <class 'bool'>
print(type(None))          # <class 'NoneType'>
```
---
## List of Python Data Types

## 🔢 1. List of Python Data Types (Grouped by Category)

**Python’s built-in data types with examples:**

### **A. Numeric Types**
Used for numbers.

| Type     | Description                  | Example         |
|----------|------------------------------|-----------------|
| `int`    | Integer                      | `x = 42`        |
| `float`  | Floating-point number        | `pi = 3.14`     |
| `complex`| Complex number               | `z = 2 + 3j`    |

---

### **B. Sequence Types**
Ordered collections of items.

| Type     | Description                  | Example                          |
|----------|------------------------------|----------------------------------|
| `str`    | String (text)                | `name = "Alice"`                |
| `list`   | Mutable sequence             | `colors = ["red", "green"]`     |
| `tuple`  | Immutable sequence           | `point = (10, 20)`              |
| `range`  | Sequence of numbers          | `r = range(5)`                  |

---

### **C. Set Types**
Unordered collections of unique items.

| Type        | Description              | Example                      |
|-------------|--------------------------|------------------------------|
| `set`       | Mutable set              | `s = {1, 2, 3}`              |
| `frozenset` | Immutable set            | `fs = frozenset([1, 2, 3])` |

---

### **D. Mapping Type**
Key-value pairs.

| Type   | Description                  | Example                              |
|--------|------------------------------|--------------------------------------|
| `dict` | Dictionary                   | `person = {"name": "Bob", "age": 30}`|

---

### **E. Boolean Type**
Truth values.

| Type   | Description                  | Example         |
|--------|------------------------------|-----------------|
| `bool` | Boolean                      | `is_valid = True` |

---

### **F. Binary Types**
Used for binary data.

| Type        | Description              | Example                    |
|-------------|--------------------------|----------------------------|
| `bytes`     | Immutable byte sequence  | `b = b"hello"`             |
| `bytearray` | Mutable byte sequence    | `ba = bytearray(5)`        |
| `memoryview`| Memory view object       | `mv = memoryview(b'abc')`  |

---

### **G. None Type**
Represents the absence of a value.

| Type       | Description               | Example         |
|------------|---------------------------|-----------------|
| `NoneType` | Represents no value       | `x = None`      |

---

## 📦 2. The `list` Data Type in Python

The `list` is one of the most commonly used data types in Python. It is:

- **Ordered**: Items have a defined order.
- **Mutable**: You can change, add, or remove items.
- **Heterogeneous**: Can contain different data types.

### Example:
```python
my_list = [1, "hello", 3.14, True]
```

### Common Operations:
```python
my_list.append("new")     # Add item
my_list[1] = "world"      # Modify item
del my_list[0]            # Delete item
print(len(my_list))       # Length of list
```
---
**In Python, injecting or adding a new value into a list can be done in several ways depending on where and how you want to insert the value.** 

---

## 🔧 Ways to Inject a New Value into a List

### 1. **Append to the End**
Adds a new element at the end of the list.

```python
fruits = ["apple", "banana"]
fruits.append("cherry")
print(fruits)  # ['apple', 'banana', 'cherry']
```

---

### 2. **Insert at a Specific Index**
Inserts a new element at a specified position.

```python
fruits = ["apple", "banana"]
fruits.insert(1, "orange")  # Insert at index 1
print(fruits)  # ['apple', 'orange', 'banana']
```

---

### 3. **Extend with Another List**
Adds multiple elements from another iterable (like a list or tuple).

```python
fruits = ["apple", "banana"]
fruits.extend(["grape", "melon"])
print(fruits)  # ['apple', 'banana', 'grape', 'melon']
```

---

### 4. **List Concatenation**
Creates a new list by combining two lists.

```python
fruits = ["apple", "banana"]
new_fruits = fruits + ["kiwi"]
print(new_fruits)  # ['apple', 'banana', 'kiwi']
```

---

### 5. **Using Slice Assignment**
Injects elements at a specific slice of the list.

```python
fruits = ["apple", "banana"]
fruits[1:1] = ["pear"]  # Insert at index 1
print(fruits)  # ['apple', 'pear', 'banana']
```

---

### 6. **Using a Loop (for multiple insertions)**
Useful when inserting based on conditions or dynamically.

```python
fruits = ["apple", "banana"]
for fruit in ["kiwi", "mango"]:
    fruits.append(fruit)
print(fruits)  # ['apple', 'banana', 'kiwi', 'mango']
```
---
**In Python, both `list` and `tuple` are used to store collections of items. However, they have key differences in terms of mutability, performance, and usage. Here's a detailed comparison:**

---
### list and tuple
## 🆚 Difference Between `list` and `tuple`

| Feature           | `list`                             | `tuple`                            |
|------------------|-------------------------------------|------------------------------------|
| **Mutability**    | Mutable (can be changed)            | Immutable (cannot be changed)      |
| **Syntax**        | Square brackets `[]`                | Parentheses `()`                   |
| **Performance**   | Slower (more flexible)              | Faster (less overhead)             |
| **Methods**       | Many built-in methods (`append`, `remove`, etc.) | Fewer methods (`count`, `index`)   |
| **Use Case**      | When you need to modify data        | When data should not change        |
| **Memory Usage**  | Uses more memory                    | Uses less memory                   |
| **Hashable**      | Not hashable (can’t be dict keys)   | Hashable if all elements are hashable |

---

## 🧪 Examples

### List Example:
```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")  # ✅ Works
print(fruits)  # ['apple', 'banana', 'cherry', 'orange']
```

### Tuple Example:
```python
colors = ("red", "green", "blue")
# colors.append("yellow")  ❌ Error: 'tuple' object has no attribute 'append'
print(colors)  # ('red', 'green', 'blue')
```

---

## 🔐 When to Use What?

- Use a **list** when:
  - You need to add, remove, or change items.
  - The data is dynamic and may grow or shrink.

- Use a **tuple** when:
  - You want to ensure the data remains constant.
  - You need to use the collection as a key in a dictionary or store it in a set.

---

**Some practical and real-world use cases where lists and tuples shine in Python.**

---

## 🧺 Use Cases for Lists

Lists are ideal when you need a flexible, dynamic collection of items that may change over time.

### 1. 📋 To-Do List App
```python
tasks = ["Buy groceries", "Call mom", "Read book"]
tasks.append("Go for a walk")
tasks.remove("Call mom")
print(tasks)
```

### 2. 📊 Collecting User Input
```python
user_inputs = []
for _ in range(3):
    name = input("Enter a name: ")
    user_inputs.append(name)
print(user_inputs)
```

### 3. 🔄 Sorting and Filtering Data
```python
scores = [88, 92, 79, 93, 85]
high_scores = [score for score in scores if score > 90]
print(sorted(high_scores))  # [92, 93]
```

### 4. 🧪 Storing Results from a Loop
```python
squares = []
for i in range(5):
    squares.append(i ** 2)
print(squares)  # [0, 1, 4, 9, 16]
```

---

## 🧊 Use Cases for Tuples

Tuples are great when you want to ensure data integrity and use fixed collections of items.

### 1. 📍 Coordinates or GPS Data
```python
location = (51.5074, -0.1278)  # Latitude and Longitude of London
```

### 2. 🧾 Returning Multiple Values from a Function
```python
def get_min_max(numbers):
    return (min(numbers), max(numbers))

result = get_min_max([3, 7, 2, 9])
print(result)  # (2, 9)
```

### 3. 🗝️ Dictionary Keys
```python
location_data = {
    ("New York", "USA"): 8419000,
    ("Tokyo", "Japan"): 13960000
}
```

### 4. 🧱 Fixed Configuration Settings
```python
config = ("v1.0", "production", True)
# Immutable, so it won't accidentally change
```

---

## Summary

- Use **lists** when your data is expected to change.
- Use **tuples** when your data should remain constant or needs to be hashable (e.g., dictionary keys).

---
We can use either **single quotes** (`'`) or **double quotes** (`"`) to define the string. Both are perfectly valid and functionally equivalent.

---

## ✅ Examples of Strings in a List

```python
# Using double quotes
fruits = ["apple", "banana", "cherry"]

# Using single quotes
colors = ['red', 'green', 'blue']

# Mixing both (allowed, but not recommended for consistency)
mixed = ["hello", 'world']
```

---

## 🧠 So, Do You Have to Use Double Quotes?

**No**, you don’t have to. You can use either, but here are some tips:

### ✔️ Use double quotes when:
- Your string contains a single quote:
  ```python
  sentence = ["It's a sunny day"]
  ```

### ✔️ Use single quotes when:
- Your string contains double quotes:
  ```python
  dialogue = ['He said, "Hello!"']
  ```

### ✔️ Use consistent style:
- Pick one style and stick with it throughout your code for readability.
- Most Python style guides (like [PEP 8](https://peps.python.org/pep-0008/)) don’t enforce one over the other, but consistency is key.

---

## 🧪 Bonus: Triple Quotes for Multiline Strings
```python
story = [
    """Once upon a time,
    in a land far away..."""
]
```
---

### Dictionary: 
Dictionaries are ideal for:
- Storing structured data (like user profiles, settings, or records).
- Grouping related values under a common key.
- Fast lookups and updates.

```python
students = {}
for i in range(2):
    name = input("Enter student name: ")
    age = int(input("Enter age: "))
    grade = input("Enter grade: ")
    students[name] = {"age": age, "grade": grade}

print(students)
```

### 🧪 Example Run (with sample input):

```
Enter student name: Alice
Enter age: 14
Enter grade: A
Enter student name: Bob
Enter age: 15
Enter grade: B
```

### 🖨️ Output:
```python
{
    'Alice': {'age': 14, 'grade': 'A'},
    'Bob': {'age': 15, 'grade': 'B'}
}
```

### 🔍 Explanation:
- The dictionary `students` is built dynamically.
- Each student's name becomes a key.
- The value is another dictionary containing their age and grade.

---
Indentation in Python is not just about style—it's a fundamental part of the language's syntax. Unlike many other programming languages that use braces `{}` or keywords to define code blocks, Python uses indentation to group statements. This makes code more readable and enforces a clean, consistent structure.

---

##  Why Indentation Matters in Python

### ✅ 1. Defines Code Blocks
In Python, indentation is used to define the scope of loops, conditionals, functions, classes, and more.

```python
if True:
    print("This is indented and part of the if block")
print("This is outside the if block")
```

Without proper indentation, Python will raise an error.

---

### ❌ 2. Incorrect Indentation Causes Errors

```python
def greet():
print("Hello")  # ❌ IndentationError
```

This will raise:
```
IndentationError: expected an indented block
```

---

### 📏 3. Standard Indentation Rules

- Use 4 spaces per indentation level (recommended by [PEP 8](https://peps.python.org/pep-0008/)).
- Be consistent—don’t mix tabs and spaces.

---

### 🧱 4. Nested Structures

Proper indentation helps manage nested logic clearly:

```python
for i in range(3):
    if i % 2 == 0:
        print(f"{i} is even")
    else:
        print(f"{i} is odd")
```

---

### 🧼 5. Improves Readability

Python’s enforced indentation makes code easier to read and understand, which is one of the reasons it's so popular for beginners and professionals alike.

---

## 🛠 Tips for Managing Indentation

- Use a code editor that shows invisible characters (like spaces and tabs).
- Enable auto-indentation and linting tools (e.g., flake8, pylint).

---
### Type of loops in python

---

### ✅ 1. Iterating Over a List

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

**Output:**
```
apple
banana
cherry
```

---

### ✅ 2. Summing Numbers with a `for` Loop

```python
total = 0
for num in range(1, 6):
    total += num
print("Sum:", total)
```

**Output:**
```
Sum: 15
```

---

### ✅ 3. Validating Input with a `while` Loop

```python
password = ""
while password != "secret":
    password = input("Enter password: ")
print("Access granted!")
```

**Output (example interaction):**
```
Enter password: 1234
Enter password: letmein
Enter password: secret
Access granted!
```

---

### ✅ 4. Nested Loops for Grids or Tables

```python
for row in range(3):
    for col in range(3):
        print(f"({row}, {col})", end=" ")
    print()
```

**Output:**
```
(0, 0) (0, 1) (0, 2) 
(1, 0) (1, 1) (1, 2) 
(2, 0) (2, 1) (2, 2) 
```

---

### ✅ 5. Looping with `enumerate()`

```python
colors = ["red", "green", "blue"]
for index, color in enumerate(colors):
    print(f"{index}: {color}")
```

**Output:**
```
0: red
1: green
2: blue
```

---

### ✅ 6. Breaking Out of a Loop

```python
for num in range(10):
    if num == 5:
        break
    print(num)
```

**Output:**
```
0
1
2
3
4
```

---

### ✅ 7. Skipping Iterations with `continue`

```python
for num in range(5):
    if num == 2:
        continue
    print(num)
```

**Output:**
```
0
1
3
4
```
---
In Python, you can "jump" or skip iterations in a loop using the built-in control statements like `continue` and `range()` with a step value. If you want to jump every 2 or 3 iterations, you can do this in a few different ways depending on your goal.

---

## 🔁 Use Case: Jumping Every 2 or 3 Iterations

### ✅ 1. Using `range()` with a Step

This is the cleanest way to jump over iterations.

```python
# Jump every 2 iterations
for i in range(0, 10, 2):
    print(i)
```

**Output:**
```
0
2
4
6
8
```

📌 Use case: Processing every second item (e.g., even-indexed elements).

---

### ✅ 2. Using `continue` to Skip Specific Iterations

```python
# Skip every 3rd iteration
for i in range(1, 11):
    if i % 3 == 0:
        continue
    print(i)
```

**Output:**
```
1
2
4
5
7
8
10
```

📌 Use case: Skipping items based on a condition (e.g., skip every 3rd record).

---

### ✅ 3. Using Indexing to Jump Over Elements in a List

```python
items = ['a', 'b', 'c', 'd', 'e', 'f']
for i in range(0, len(items), 3):
    print(items[i])
```

**Output:**
```
a
d
```

📌 Use case: Sampling every 3rd item from a dataset.

---

### ✅ 4. Using a Counter Inside a Loop

```python
count = 0
for i in range(10):
    count += 1
    if count == 3:
        print(f"Jump at {i}")
        count = 0
```

**Output:**
```
Jump at 2
Jump at 5
Jump at 8
```

📌 Use case: Triggering an action every 3 iterations (e.g., batch processing).

---
### for loops and while loops

**In Python, both `for` loops and `while` loops are used to repeat a block of code, but they serve different purposes and are best suited for different types of tasks.**

---

## 🔁 `for` Loop vs `while` Loop in Python

| Feature               | `for` Loop                                      | `while` Loop                                  |
|-----------------------|--------------------------------------------------|------------------------------------------------|
| **Purpose**           | Iterate over a sequence (like list, range, etc.)| Repeat as long as a condition is `True`       |
| **Best for**          | Known number of iterations                      | Unknown or conditional number of iterations   |
| **Control**           | Automatically handles iteration                 | Requires manual control (e.g., incrementing)  |
| **Risk of Infinite Loop** | Low                                         | Higher if condition is not updated properly   |

---

## ✅ Use Cases with Examples

### 🧾 1. `for` Loop Use Case: Iterating Over a List

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

📌 Use case: When you know the number of items to process.

---

### 🔢 2. `for` Loop Use Case: Counting with `range()`

```python
for i in range(5):
    print(i)
```

📌 Use case: Repeating a task a specific number of times.

---

### 🔄 3. `while` Loop Use Case: Waiting for a Condition

```python
password = ""
while password != "secret":
    password = input("Enter password: ")
print("Access granted!")
```

📌 Use case: Repeating until a condition is met (e.g., user input validation).

---

### ⏳ 4. `while` Loop Use Case: Countdown Timer

```python
count = 5
while count > 0:
    print(count)
    count -= 1
```

📌 Use case: When the stopping condition depends on a variable that changes inside the loop.

---

## 🧠 Summary

- Use a `for` loop when:
  - You’re iterating over a sequence.
  - You know how many times the loop should run.

- Use a `while` loop when:
  - You don’t know how many times the loop should run.
  - You’re waiting for a condition to become false.

---
###  Declaring Functions in Python
In Python, a **function** is a reusable block of code that performs a specific task. Functions help organize code, reduce repetition, and improve readability.

---

We declare a function using the `def` keyword, followed by the function name and parentheses `()` which may include parameters.

### 📌 Basic Syntax:
```python
def function_name(parameters):
    # code block
    return result  # optional
```

---

## ✅ Examples with Output

### 1. **Function Without Parameters**

```python
def greet():
    print("Hello, world!")

greet()
```

**Output:**
```
Hello, world!
```

---

### 2. **Function With Parameters**

```python
def greet_user(name):
    print(f"Hello, {name}!")

greet_user("Alice")
```

**Output:**
```
Hello, Alice!
```

---

### 3. **Function With Return Value**

```python
def add(a, b):
    return a + b

result = add(5, 3)
print(result)
```

**Output:**
```
8
```

---

### 4. **Function With Default Parameters**

```python
def greet(name="Guest"):
    print(f"Welcome, {name}!")

greet()
greet("Bob")
```

**Output:**
```
Welcome, Guest!
Welcome, Bob!
```

---

### 5. **Function With Multiple Return Values**

```python
def get_stats(numbers):
    return min(numbers), max(numbers), sum(numbers)

low, high, total = get_stats([3, 7, 2, 9])
print(low, high, total)
```

**Output:**
```
2 9 21
```

---

### 6. **Function With Variable Number of Arguments**

```python
def print_items(*items):
    for item in items:
        print(item)

print_items("apple", "banana", "cherry")
```

**Output:**
```
apple
banana
cherry
```

---


---














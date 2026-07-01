# Python Basics for Agentic AI & Generative AI

> A practical Python guide covering the fundamentals required before learning Agentic AI, LLMs, RAG, AI Agents, and Generative AI frameworks such as LangChain, LlamaIndex, CrewAI, AutoGen, OpenAI SDK, and more.

---

# Table of Contents

1. Introduction
2. Variables and Data Types
3. Operators
4. Input and Output
5. Type Casting
6. Strings
7. Lists
8. Tuples
9. Sets
10. Dictionaries
11. Conditional Statements
12. Loops
13. Functions
14. Lambda Functions
15. List Comprehension
16. Exception Handling
17. Modules and Packages
18. File Handling
19. Object-Oriented Programming
20. Decorators
21. Iterators and Generators
22. *args and **kwargs
23. Virtual Environment
24. Pip Package Management
25. Useful Built-in Functions
26. Python Tips for AI Developers
27. Mini Practice Exercises

---

# 1. Introduction

Python is one of the easiest and most popular programming languages.

It is widely used in

- Artificial Intelligence
- Machine Learning
- Deep Learning
- Data Science
- Web Development
- Automation
- Generative AI
- Agentic AI

Example:

```python
print("Hello, AI World!")
```

Output

```
Hello, AI World!
```

---

# 2. Variables and Data Types

Variables store values.

```python
name = "Alice"
age = 25
salary = 75000.50
is_student = False
```

### Common Data Types

| Type | Example |
|------|---------|
| int | 10 |
| float | 10.5 |
| str | "Hello" |
| bool | True |
| list | [1,2,3] |
| tuple | (1,2,3) |
| dict | {"name":"John"} |
| set | {1,2,3} |

Check type

```python
print(type(age))
```

Output

```
<class 'int'>
```

---

# 3. Operators

## Arithmetic

```python
a = 10
b = 3

print(a+b)
print(a-b)
print(a*b)
print(a/b)
print(a//b)
print(a%b)
print(a**b)
```

---

## Comparison

```python
print(a > b)
print(a < b)
print(a == b)
print(a != b)
```

---

## Logical

```python
print(True and False)
print(True or False)
print(not True)
```

---

# 4. Input and Output

```python
name = input("Enter name: ")

print("Welcome", name)
```

---

# 5. Type Casting

```python
age = "25"

age = int(age)

print(age + 5)
```

Other conversions

```python
str()
int()
float()
bool()
list()
tuple()
set()
```

---

# 6. Strings

Strings store text.

```python
text = "Generative AI"
```

Access characters

```python
print(text[0])
print(text[-1])
```

Slicing

```python
print(text[:10])
print(text[11:])
```

Useful methods

```python
text.lower()
text.upper()
text.title()
text.replace("AI","Intelligence")
text.split()
```

Formatting

```python
name = "John"

print(f"Hello {name}")
```

---

# 7. Lists

Lists are ordered and mutable.

```python
languages = ["Python","Java","C++"]
```

Access

```python
print(languages[0])
```

Add

```python
languages.append("Go")
```

Insert

```python
languages.insert(1,"Rust")
```

Remove

```python
languages.remove("Java")
```

Loop

```python
for lang in languages:
    print(lang)
```

---

# 8. Tuples

Immutable collections.

```python
colors = ("Red","Green","Blue")
```

Access

```python
print(colors[1])
```

---

# 9. Sets

Stores unique values.

```python
numbers = {1,2,3,3,4}

print(numbers)
```

Output

```
{1,2,3,4}
```

Operations

```python
numbers.add(10)
numbers.remove(2)
```

---

# 10. Dictionaries

Store key-value pairs.

```python
student = {
    "name":"Alice",
    "age":22,
    "city":"Delhi"
}
```

Access

```python
print(student["name"])
```

Add

```python
student["grade"] = "A"
```

Loop

```python
for key,value in student.items():
    print(key,value)
```

---

# 11. Conditional Statements

```python
age = 18

if age >= 18:
    print("Adult")
else:
    print("Minor")
```

Multiple conditions

```python
marks = 85

if marks >= 90:
    print("A")
elif marks >= 75:
    print("B")
else:
    print("C")
```

---

# 12. Loops

## For Loop

```python
for i in range(5):
    print(i)
```

---

## While Loop

```python
count = 1

while count <= 5:
    print(count)
    count += 1
```

Loop through list

```python
fruits = ["Apple","Banana","Orange"]

for fruit in fruits:
    print(fruit)
```

---

# 13. Functions

Functions make reusable code.

```python
def greet(name):
    return f"Hello {name}"

print(greet("Alice"))
```

Default parameter

```python
def welcome(name="Guest"):
    print(name)
```

Multiple return

```python
def calculate(a,b):
    return a+b,a-b
```

---

# 14. Lambda Functions

```python
square = lambda x: x*x

print(square(5))
```

Sorting

```python
students = [
    ("John",25),
    ("Alice",20)
]

students.sort(key=lambda x:x[1])
```

---

# 15. List Comprehension

Traditional

```python
numbers = []

for i in range(10):
    numbers.append(i)
```

Pythonic

```python
numbers = [i for i in range(10)]
```

Condition

```python
even = [i for i in range(20) if i%2==0]
```

---

# 16. Exception Handling

```python
try:
    num = 10/0
except ZeroDivisionError:
    print("Cannot divide by zero")
finally:
    print("Done")
```

---

# 17. Modules and Packages

Import module

```python
import math

print(math.sqrt(25))
```

Specific import

```python
from math import pi
```

Create your own module

math_utils.py

```python
def add(a,b):
    return a+b
```

main.py

```python
from math_utils import add

print(add(10,20))
```

---

# 18. File Handling

Write

```python
with open("data.txt","w") as file:
    file.write("Hello AI")
```

Read

```python
with open("data.txt","r") as file:
    print(file.read())
```

Append

```python
with open("data.txt","a") as file:
    file.write("\nNew Line")
```

---

# 19. Object-Oriented Programming

## Class

```python
class Student:

    def __init__(self,name):
        self.name = name

    def greet(self):
        print(f"Hello {self.name}")
```

Create object

```python
student = Student("Alice")

student.greet()
```

Inheritance

```python
class Animal:

    def sound(self):
        print("Animal Sound")

class Dog(Animal):

    def bark(self):
        print("Woof")
```

---

# 20. Decorators

```python
def logger(func):

    def wrapper():
        print("Started")
        func()
        print("Finished")

    return wrapper

@logger
def hello():
    print("Hello")

hello()
```

---

# 21. Iterators and Generators

Generator

```python
def numbers():

    for i in range(5):
        yield i

for num in numbers():
    print(num)
```

Generators save memory.

---

# 22. *args and **kwargs

```python
def add(*args):
    return sum(args)

print(add(1,2,3,4))
```

Keyword arguments

```python
def profile(**kwargs):
    print(kwargs)

profile(name="John",age=25)
```

---

# 23. Virtual Environment

Create

```bash
python -m venv venv
```

Activate

Windows

```bash
venv\Scripts\activate
```

Mac/Linux

```bash
source venv/bin/activate
```

Deactivate

```bash
deactivate
```

---

# 24. Pip Package Management

Install

```bash
pip install pandas
```

Upgrade

```bash
pip install --upgrade pandas
```

Requirements

```bash
pip freeze > requirements.txt
```

Install from requirements

```bash
pip install -r requirements.txt
```

---

# 25. Useful Built-in Functions

```python
len()
sum()
min()
max()
sorted()
zip()
enumerate()
map()
filter()
any()
all()
range()
```

Example

```python
numbers = [5,3,8]

print(max(numbers))
print(min(numbers))
print(sum(numbers))
```

---

# 26. Python Tips for AI Developers

## Use Virtual Environments

Every AI project should have its own environment.

---

## Follow PEP 8

```python
user_name = "John"
```

Not

```python
UserName="John"
```

---

## Use Meaningful Variable Names

Good

```python
user_prompt
llm_response
conversation_history
```

Bad

```python
a
b
c
```

---

## Learn These Libraries

| Library | Purpose |
|----------|----------|
| NumPy | Numerical Computing |
| Pandas | Data Analysis |
| Matplotlib | Visualization |
| Requests | API Calls |
| JSON | Handle JSON |
| pathlib | File Paths |
| os | Operating System |
| asyncio | Async Programming |
| typing | Type Hints |

---

## Learn JSON

Almost every LLM API uses JSON.

```python
import json

data = {
    "question":"What is AI?"
}

print(json.dumps(data, indent=4))
```

---

## Learn API Requests

```python
import requests

response = requests.get("https://example.com")

print(response.status_code)
```

---

## Learn Environment Variables

```python
import os

api_key = os.getenv("OPENAI_API_KEY")
```

Never hardcode API keys.

---

## Learn Async Programming

Many AI SDKs support async.

```python
import asyncio

async def hello():
    print("Hello")

asyncio.run(hello())
```

---

# 27. Mini Practice Exercises

### Beginner

- Reverse a string
- Find factorial
- Count vowels
- Remove duplicates from a list
- Find largest number
- Check palindrome

### Intermediate

- Student Management System
- Calculator
- Todo CLI App
- Expense Tracker
- Contact Book

### AI-Oriented

- Read prompts from a text file
- Save LLM responses into JSON
- Build a chatbot using functions
- Create a prompt template generator
- Parse API responses
- Read PDFs and extract text
- Load CSV data using Pandas

---

# Python Topics Required Before Agentic AI

- Variables
- Data Types
- Functions
- OOP
- Exception Handling
- File Handling
- JSON
- Modules
- APIs
- Async Programming
- Virtual Environment
- Pip
- Decorators
- Generators
- List Comprehension

Master these topics before learning:

- Prompt Engineering
- OpenAI SDK
- LangChain
- LlamaIndex
- CrewAI
- AutoGen
- MCP (Model Context Protocol)
- RAG (Retrieval-Augmented Generation)
- AI Agents
- Multi-Agent Systems

---

# Recommended Learning Path

```
Python Basics
      ↓
Object-Oriented Programming
      ↓
File Handling
      ↓
JSON
      ↓
API Requests
      ↓
Async Programming
      ↓
Virtual Environment
      ↓
Git & GitHub
      ↓
Prompt Engineering
      ↓
LLM APIs
      ↓
LangChain / LlamaIndex
      ↓
Vector Databases
      ↓
RAG
      ↓
Agentic AI
      ↓
Multi-Agent Systems
```

---

# Final Notes

Python is the foundation of modern AI development. Focus on understanding concepts rather than memorizing syntax. Build small projects as you learn, practice reading documentation, and gradually explore AI-specific libraries. A solid grasp of these basics will make it much easier to work with LLM APIs, build AI agents, and develop production-ready Generative AI applications.

Happy Learning!
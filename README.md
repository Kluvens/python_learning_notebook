# Table of Contents
1. [Why Python](#why-python)
    1. [Python history](#python-history)
    2. [Python 2 and Python 3](#python-2-and-python-3)
    3. [Why Python is popular](#why-python-is-popular)
    4. [Why Python is slow](#why-python-is-slow)
2. [Python basic syntax](#python-basic-syntax)
3. [Python advanced syntax](#python-advanced-syntax)
4. [Python Object Oriented Programming](#python-object-oriented-programming)
5. [Python Topics](#python-topics)
6. [Python with data structure and algorithms](#python-with-data-structure-and-algorithms)
7. [Python with other modules](#python-with-other-modules)
    1. [Python with Flask](#python-with-flask)
    2. [Python with Subprocess](#python-with-subprocess)
    3. [Python with Regular expression](#python-with-regular-expression)
    4. [Python with Database](#python-with-database)
    5. [Python with Statistics](#python-with-statistics)
    6. [Python with Math](#python-with-math)

# Why Python
## Python history
Python was conceived in the late 1980s by Guido van Rossum at Centrum Viskunde & Informatica (CWI) in the Netherlands as a successor to the ABC programming language, 
which was inspired by SETL, 
capable of exception handling and interfacing with the Amoeba operating system.
## Python 2 and Python 3
Python 2.0 was released on 16 October 2000, and Python 3.0 was released on 3 December 2008.
As of January 1st, 2020, no new bug reports, fixes or changes will be made to Python 2 and Python 2 is no longer supported.

There are several major differences between Python 2 and Python 3:
- Python 3 syntax is simpler and easily understandable whereas Python 2 syntax is comparatively difficult to understand.
- Python 3 default storing of strings is Unicode whereas Python 2 stores need to define Unicode string value with “u.”
- Python 3 value of variables never changes whereas in Python 2 value of the global variable will be changed while using it inside for-loop.
- Python 3 exceptions should be enclosed in parenthesis while Python 2 exceptions should be enclosed in notations.
- Python 3 rules of ordering comparisons are simplified whereas Python 2 rules of ordering comparison are complex.
- Python 3 offers Range() function to perform iterations whereas, In Python 2, the xrange() is used for iterations.
## Why Python is popular
1. Python is easy to learn and use which means Python can have higher productivity
2. Python is handy for web development purposes
3. Python is extensively used in data science and artificial intelligence
4. Python has multiple libraries and frameworks
5. Python can be used in ML tool
6. Python has a highly supportive community
7. Python programs or portable
## Why Python is slow
Unlike native languages like C/C++, Python code gets interpreted at runtime instead of being compiled to native code at compile time. Python is an interpreted language, which means that the Python code we write must go through many, many stages of abstraction before it can become executable machine code.

Python code is first compiled into python Byte Code. The Byte Code interpreter conversion happens internally and most of it is hidden from the developer.Byte code is platform-independent and lower-level programming. Compilation of byte code is to ramp up the execution of source code. The source code compiled to byte code is then executed in Python’s virtual machine one by one, to carry out the operations. The virtual machine is an internal component of Python. Internally Python code is interpreted during run time rather than being compiled to native code hence it is a bit slower. 

# Python basic syntax
## Python Comments
### Single-line comments
A comment in Python starts with the hash character(#), and extends to the end of the physical line. In other words, all contents after # are invlaid except the # is inside a string.
``` python
# define the general structure of the product with default values
product = {
    "productId": 0,          # product reference id, default: 0
    "description": "",       # item description, default: empty
    "categoryId": 0,         # item category, default: 0
    "price": 0.00            # price, default: 0.00
}
```
### Multi-line comments
There are two versions of multi-line comments.

Version 1: combines single-line comments as follows:
``` python
# LinuxThingy version 1.6.5
#
# Parameters:
#
# -t (--text): show the text interface
# -h (--help): display this help
```
Version 2: It's originally intended to be used for creating documentation (see more about this below), but it can also be used for multi-line comments. The commented contents inside """ """.
``` python
"""
LinuxThingy version 1.6.5

Parameters:

-t (--text): show the text interface
-h (--help): display this help
"""
```
## Python Variables
### Variables
A variable is a value that can change, depending on conditions or on information passed to the program. We can understand it as a container for storing data values.
### Creating variables
Python has no command for declaring a variable.
A variable is created the moment you first assign a value to it.

**Information:** A declaration of a variable is where a program says that it needs a variable whereas initializing a variable means specifying an initial value to assign to it.
``` python
x = 5           # we are creating a variable called x and the value stored is 5
y = "John"      # we are creating a variable called y and the value stored is "John"
```
## Python Data types
Variables can store data of different types, and different types can do different things.
### Python built-in data types
- Test type: ```str```
- Numeric types: ```int```, ```float```, ```complex```
- Sequence types: ```list```, ```tuple```, ```range```
- Mapping type: ```dict```
- Set types: ```set```, ```frozenset```
- Boolean type: ```bool```
- Binary types: ```bytes```, ```bytearray```, ```memoryview```
- None type: ```NoneType```

More specifically:
- ```int```: means integer or whole number, can be 0, positive or negative, without decimals, of unlimited length
- ```float```: means floating point number, is a number, positive or negative, containing one or more decimals. Float can also be scientific numbers with an "e" to indicate the power of 10. ```35e3``` means 35*(10^3).
### Getting the type of a variable
We can use Python built-in function ```type()``` to get the type of a variable.
``` python
print(type(5))          # <class 'int'>, means it is an integer
print(type(5.1))        # <class 'float'>, means it is a floating point number
print(type("5.1"))      # <class 'str'>, means it is a string
print(type(True))       # <class 'bool'>, means it is a boolean value
```
### Python type casting
Python is an object-prientated language, and as such it uses classes to define data types, including its primitive types. Casting can specify a type on to a variable.
``` python
x = int(1)              # specify the type of x as int, x will be 1
y = int(2.8)            # specify the type of y as int, y will be 2
z = int("3")            # specify the type of z as int, z will be 3
x = float(1)            # x will be 1.0
y = float(2.8)          # y will be 2.8
z = float("3")          # z will be 3.0
w = float("4.2")        # w will be 4.2
x = str("all5all")      # x will be 'all5all'
y = str(1)              # y will be '1'
z = str(5.6)            # z will be '5.6'
x = int("Justin")       # will give ValueError, could not convert from string to int
x = float("Justin")     # will give ValueError, could not convert from string to float
x = bool(1)             # x will be True
x = bool(0)             # x will be False
x = int(True)           # x will be 1
x = float(True)         # x will be 1.0
x = str(True)           # x will be 'True'
```
## Python Operators
There are several groups of operators that Python provides:
- Arithmetic operators
- Assignment operators
- Comparison operators
- Logical operators
- Identity operators
- Membership operators
- Bitwise operators

### Python Arithmetic Operators
``` python
# '+' means addition
print(3 + 2)            # 5
print(3 + 2.0)          # 5.0
print(3 + True)         # 4 because True acturally means 1 and False means 0

# '-' means subtraction
print(3 - 2)            # 1
print(3 - 2.0)          # 1.0

# '*' means multiplication
print(3 * 2)            # 6

# '/' means division. Division gives a float value as result
print(3 / 2)            # 1.5
print(4 / 2)            # 2.0

# '%' means modulus
print(3 % 2)            # 1
print(4 % 2)            # 0

# '**' means exponentiation
print(3 ** 2)           # 9
print(3 ** 2.0)         # 9.0

# '//' means floor division. This is the same as '/' in C.
print(3 // 2)           # 1
print(4 // 2)           # 2
print(3 // 2.0)         # 1.0
```

### Python Assignment Operators
``` python
# '=' is an assignment operator, it puts the value on the right hand side to the left hand side
x = 5                   # assign 5 to variable x
print(x)                # 5

# '+='
x += 3                  # the same as x = x + 3
print(x)                # 8

# '-='
x -= 3                  # the same as x = x - 3
print(x)                # 5

# '*='
x *= 3                  # the same as x = x * 3
print(x)                # 15

# '/='
x /= 3                  # the same as x = x / 3
print(x)                # 5.0 instead of 5

# '%='
x %= 3                  # the same as x = x % 3
print(x)                # 2.0

# '//='
x = 5
x //= 3                 # the same as x = x // 3
print(x)                # 1

# '**='
x = 5
x **= 3                 # the same as x = x ** 3
print(x)                # 125

# '&='
x = 5
x &= 3                  # the same as x = x & 3
print(x)                # 0101 & 0011 => 0001 => 1

# '|='
x = 5
x |= 3                  # the same as x = x | 3
print(x)                # 0101 | 0011 => 0111 => 7

# '^='
x = 5
x ^= 3                  # the same as x = x ^ 3
print(x)                # 0101 ^ 0011 => 0110 => 6

# '>>='
x = 5
x >>= 2                 # the same as x = x >> 2
print(x)                # 0101 >> 2 => 0001 => 1

# '<<='
x = 5
x <<= 1                 # the same as x = x << 1
print(x)                # 0101 << 1 => 1010 => 10
```

### Python Comparison Operators
Comparison operators are used to compare two values
``` python
# '=='
x = 5
y = 5
print(x == y)           # True
z = 5.0
print(x == z)           # True
print(1 == True)        # True

# '!='
print(False != True)    # True
print(1 != 1)           # False

# '>'
print(5 > 5)            # False
print(5 > 4)            # True
print(5 > 4.2)          # True
print(5 > True)         # True

# '<'
print(5 < 4)            # False
print(5 < 4.2)          # False
print(5 < True)         # False

# '>='
print(5 >= 5)           # True
print(5 >= 4)           # True
print(5 >= 4.2)         # True
print(5 >= True)        # True

# '<='
print(5 <= 5)           # True 
print(5 <= 4)           # False
print(5 <= 4.2)         # False
print(5 <= True)        # False
```

### Python Logical Operators
``` python
# 'and', return True if both statements are True
print(1 < 5 and 5 >= 5) # True
print(1 > 5 and 5 >= 5) # False

# 'or', return True if one of the statements is True
print(1 < 5 or 5 >= 5)  # True
print(1 > 5 or 5 >= 5)  # True
print(1 < 5 or 5 > 5)   # False

# 'not', reverse the result, returns False if the result is True
print(not(5 <= 5))      # False
print(not(1 > 5))       # True
```

### Python Identity Operators
The is operator determines whether two variables reference the same object.
``` python
# 'is'
a = [1, 2]
b = a 
print(a is b)           # True
print(5 is 5)           # True
print(5 is int(5))      # True
print(5.0 is float(5))  # False
print([1, 2] is [1, 2]) # False
print([] is list())     # False
print(1 is True)        # False

# 'is not'
a = [1, 2]
b = a 
c = [1, 2]
print(b is not c)       # True
```

### Python Membership Operators
Membership operators are used to test if a sequence is presented in an object
``` python
# 'in'
a = [1 , 2, 3]
print(1 in a)           # True
b = set([1, 2, 3])
print(1 in b)           # True

# 'not in'
a = [1, 2, 3]
print(1 not in a)       # False
print(5 not in a)       # True
```

## Python Strings
Strings in Python are surrounded by either single quotation marks, or double quotation marks.
```'hello'``` has no difference with ```"hello"```.
We can display a string on standard output with the ```print()``` function.
``` python
print("Hello")
print('Hello')
```
A variable can store string value, we can assign string to a variable.
``` python
a = "Hello"
print(a)
```
Python also surpport multi-line string. We can assign a multi-line string to a variable by using three double quotes or three single quotes.
``` python
a = """Python is a very useful language,
it has many features,
Python is important in data science and AI.
let's get started and learn Python"""
print(a)
```

## Python Booleans
## Python Control flow
### Python If statement
### Python While loop
### Python For loop
### Python Switch statement
## Python Lists
## Python Dictionaries
## Python Tuples
## Python Sets
## Python Functions
## Python Exceptions

# Python advanced syntax
## Python Lambda
## Python Extended Keyword Arguments (*args, **kwargs)
## Python Generators
## Python Iterators
## Python Decorators
## Python Type checking

# Python program testing and debugging

# Python Object Oriented Programming
## Everything in Python is an object
## Python Operator overloading

# Python with data structure and algorithms
## Python Linked lists
## Python Trees
## Python Graphs
## Python Searching algorithms
## Python Sorting algorithms

# Python with other modules
## Python with Flask
## Python with Subprocess
## Python with Regular expression
``` python
import re
```
**Information:**
Regular expressions are patterns used to match character combinations in strings.
For example, we may want to check if an input is an email.
Since every email must be bounded by the pattern, we can use regular expression to help us check this.
## Python with Database
## Python with Statistics
## Python with Math
## Python with OS
``` python
import os
```
## Python with Sys
``` python
import sys
```
## Python with Collections
## Python with Random
## Python with JSON
## Python with CSV
## Python with Pickle

# Python topics
## Style and being Pythonic
## Python pip
## Python virtural environment
## [Python Memory management](https://docs.python.org/3/c-api/memory.html#:~:text=Memory%20management%20in%20Python%20involves,by%20the%20Python%20memory%20manager.)
## Python virtural machine
## Python interpreter

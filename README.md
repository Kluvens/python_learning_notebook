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

***Notice***: Python has its way to deal with floating point number, it's risky if we compare two floating point numbers
``` python
print(0.1 + 0.2 == 0.3)                 # False
print((0.1 + 0.2) - 0.3)                # 5.551115123125783e-17
```

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

### Python Bitwise Operators
``` python
# '&' is AND operator, it sets each bit to 1 if both bits are 1
print(5 & 3)            # 0101 & 0011 => 0001 => 1

# '|' is OR operator, it sets each bit to 1 if one of two bits is 1
print(5 | 3)            # 0101 | 0011 => 0111 => 7

# '^' is XOR operator, it sets each bit to 1 if only one of two bits is 1
print(5 ^ 3)            # 0101 ^ 0011 => 0110 => 6

# '~' is NOT operator, it inverts all the bits
print(~5)               # ~00000101 => 11111010 => -6 

# '>>' is Zero fill left shift, it shifts left by pushing zeros in from the right and let the leftmost bits fall off
print(5 >> 2 )         # 0101 >> 2 => 0001 => 1

# '<<' is Signed right shift, it shifts right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off
print(5 << 1  )        # 0101 << 1 => 1010 => 10
```

## Python Booleans
- Booleans represent one of two values: ```True``` or ```False```.
- We can evaluate any expression in Python and get a boolean value as a result.
- We can use bool() to get a boolean value of anything.
- Almost any value is evaluated as True.
- False, None, int(0), "", (), [], {} will be evaluated as False.

## Python Strings
Strings in Python are surrounded by either single quotation marks, or double quotation marks.
```'hello'``` has no difference with ```"hello"```.
We can display a string on standard output with the ```print()``` function.
``` python
print("Hello")                  # Hello
print('Hello')                  # Hello
```
A variable can store string value, we can assign string to a variable.
``` python
a = "Hello"
print(a)                        # Hello
```
Python also surpport multi-line string. We can assign a multi-line string to a variable by using three double quotes or three single quotes.
``` python
a = """Python is a very useful language,
it has many features,
Python is important in data science and AI.
let's get started and learn Python"""
print(a)
```

More functions and methods about strings:
``` python
string = "Hello hello HeLLo_and$Ok123"

# a string can be treated as an array, with the same way we access element and loop through
print(string[2])                            # l
for i in string:
    print(i)                                # print each element of the string per line

# use len() function to get the length of the string
print(len(string))                          # 27

# we can use membership operation to check if a piece is within a string
print("Hello" in string)                    # True
print("123" not in string)                  # False

# index method to search the first occurence, and return error if not found
print(string.index("llo"))                  # 2
print(string.index("p"))                    # ValueError, substring not found

# rindex method to search the last occurence, and return error if not found(r means from right)
print(string.rindex("llo"))                 # 8

# find method to search the first occurence, and return -1 if not found
print(string.find("llo"))                   # 2
print(string.find("lllo"))                  # -1

# rfind method to search the last occurence, and return -1 if not found
print(string.rfind("llo"))                  # 8
print(string.rfind("lllo"))                 # -1

# we can use '+' to concatenate strings in Python
substr = 'hi'
print(substr)                               # hi
substr = substr + 'harry' + 'potter'
print(substr)                               # hiharrypotter

# id() function returns the identity of the object.
print(id(string))                           # 140378634129696 (but every time you run this command, we get a different result)

# change the string to upper case
print(string.upper())                       # HELLO HELLO HELLO_AND$OK123

# change the string to lower case
print(string.lower())                       # hello hello hello_and$ok123

# first character to be capitalized
print(string.capitalize())                  # Hello hello hello_and$ok123
# every first character of a word to be capitalized
print(string.title())                       # Hello Hello Hello_And$Ok123
# swap lower and upper case
print(string.swapcase())                    # hELLO HELLO hEllO_AND$oK123

# check if a string a digit number
print(string.isdigit())                     # False

# check if a string is alphabetic
print(string.isalpha())                     # False

# check if a string is alphanumeric
print(string.isalnum())                     # False
print("all123good".isalnum())               # True

# check if a string is in upper case
print(string.isupper())                     # False

# check if a string is in lower case
print(string.islower())                     # False

# split the string and return a list (maxsplit from left)
left = string.split(" ")
print(left)                                 # ['Hello', 'hello', 'HeLLo_and$Ok123']
left_max = string.split(" ", maxsplit = 1)
print(left_max)                             # ['Hello', 'hello HeLLo_and$Ok123']
# split the string and return a list (maxsplit from right)
right = string.rsplit(" ")
print(right)                                # ['Hello', 'hello', 'HeLLo_and$Ok123']
right_max = string.rsplit(" ", maxsplit = 1)
print(right_max)                            # ['Hello hello', 'HeLLo_and$Ok123']

# replace method(what we have, what we want, maximum time to be replaced default to all)
print(string.replace("hello", "youh", 1))   # Hello youh HeLLo_and$Ok123
print(string)                               # string itself is not modified

# reverse a string
print(string[::-1])                         # 321kO$dna_oLLeH olleh olleH

# strip() method is to remove the leading and the trailing characters based on the string argument passed
new_string = "    cool and i like it      \n"
print(new_string.strip())                   # cool and i like it
# rstrip() only removes the trailing characters
print(new_string.rstrip())                  #     cool and i like it
# lstrip() only removes the leading characters
print(new_string.lstrip())                  # cool and i like it      \n (\n is interpreted as a newline)
# we can specify a character
new_string = "HHHHHcool and i like itHHHHH"
print(new_string.strip("H"))                # cool and i like it

# check if a string starts with another string
print(string.startswith("Hello"))           # True

# string format
# print specific number of digits
f = 3.1415926
print("{:.3f}".format(f))                   # 3.142
# insert a value to the placeholder
txt = "For only {price:.2f} dollars!"
print(txt.format(price = 49))               # For only 49.00 dollars!
txt = "{today} is {date}"
print(txt.format(today = "Today", date = "Thursday"))   # Today is Thursday
txt = "{0} is {1}"
print(txt.format("Today", "Thursday"))      # Today is Thursday
txt = "{} is {}"
print(txt.format("Today", "Thursday"))      # Today is Thursday
# another print format
today = "Today"
day = "Thursday"
print(f"{today} is {day}")                  # Today is Thursday
```

## Python Control flow
### Python If statement
**if**
- An if statement is written by using the ```if``` keyword.
- Python relies on indentation (whitespace at the beginning of a line) to define scope in the code.
- The code with indentation under if statement will run if the condition is True.

``` python
a = 5
b = 6
if a > b:
    print("5 is greater than 6")    # we will not see this line because the condition is False and the line will not be executed

if a < b:
    print("5 is less than 6")       # we can see this line because the condition is True
```

**elif**

The ```elif``` keyword is pythons way of saying if the previous conditions were false, then try to check this condition.
``` python
a = 33
b = 33
if b > a:
  print("b is greater than a")      # failed this check
elif a == b:
  print("a and b are equal")        # passed this check and print the line
```

**else**

The ```else``` keyword catches anything which isn't caught by the preceding conditions.
``` python
a = 200
b = 33
if b > a:
  print("b is greater than a")      # can't pass the condition
elif a == b:
  print("a and b are equal")        # can't pass the condition
else:
  print("a is greater than b")      # run this line anyway
```

**Short hand if**

if you have only one statement to execute, you can put it on the same line as the if statement
``` python
if a > b: print("a is greater than b")
# this is the same as:
# if a > b:
#     print("a is greater than b")
```

**Short hand if ..else**
``` python
a = 2
b = 330
print("A") if a > b else print("B")
# this is the same as:
# if a > b:
#     print("A")
# else:
#     print("8")
```

The above technique is known as **Ternary Operators**, or **Conditional Expressions**.

**nested if**

We can have ```if``` statement inside ```if``` statement, this is called nested ```if``` statement.
``` python
x = 41

# run the code below, we can get Less than 60, but above 20!
if x < 60:
  print("Less than 60,")
  if x > 20:
    print("but above 20!")
  else:
    print("and also less than 20.")
```

**pass**

The ```pass``` statement basically means do nothing.
```if``` statements cannot be empty, but if we don't want to do anything and also make sure our code compile, we can use ```pass``` statement to avoid getting an error.
``` python
a = 33
b = 200

# execute the code below, we can't get any output, but code compile successfully
if b > a:
  pass
else:
  print("200 is not greater than 33")
```

### Python While loop
With the ```while``` loop we can execute a set of statements as long as a condition is true.
The ```while``` loop requires relevant variables to be ready, so we need to initialize variable first.

``` python
# print i as long as i is less than 6
i = 1
while i < 6:
  print(i)
  i += 1                    # remember to increment i, this is a common mistake for beginners
```

**break**

With the ```break``` statement, we can stop the loop even if the while condition is true.
``` python
i = 1
# we can get from 1 to 3
# since when i == 3, we stop the loop anyway regardless of the condition
while i < 6:
  print(i)
  if i == 3:
    break
  i += 1
```

**continue**

With the ```continue``` statement we can stop the current iteration, and jump to the next iteration.
``` python
i = 1
# we can get 1, 2, 4, 5
# since when i == 3, we stop the current iteration and jump to the next iteration and print 4
while i < 6:
    if i == 3:
        i += 1
        continue
    print(i)
    i += 1
```

**else**

With the ```else``` statement, we can run a block of code once when the condition no longer is True.
``` python
i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i is no longer less than 6")   # print the line after the while loop
```

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

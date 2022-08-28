# Table of Contents
1. [Why Python](#why-python)
    1. [Python history](#python-history)
    2. [Python 2 and Python 3](#python-2-and-python-3)
    3. [Why Python is popular](#why-python-is-popular)
    4. [Why Python is slow](#why-python-is-slow)
2. [Python basic syntax](#python-basic-syntax)
    1. [Python Comments](#python-comments)
    2. [Python Variables](#python-variables)
    3. [Python Data Types](#python-data-types)
    4. [Python Operators](#python-operators)
    5. [Python Booleans](#python-booleans)
    6. [Python Strings](#python-strings)
    7. [Python Control Flow](#python-control-flow)
    8. [Python Lists](#python-lists)
    9. [Python Dictionaries](#python-dictionaries)
    10. [Python Tuples](#python-tuples)
    11. [Python Sets](#python-sets)
    12. [Python Functions](#python-functions)
    13. [Python Errors and Exceptions](#python-errors-and-exceptions)
3. [Python advanced syntax](#python-advanced-syntax)
    1. [Python Recursion](#python-recursion)
    2. [Python Anonymous Function](#python-anonymous-function)
    3. [Python map(), filter() and reduce()](#python-map-filter-and-reduce)
    4. [Python Extended Keyword Arguments](#python-extended-keyword-arguments)
    5. [Python Generators](#python-generators)
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
Unlike C, we cannot have uninitialised variables
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

# := means assignment
x := 5

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

# string join
# join elements in the list with the string together
final_print = " ".join(["hello", "world", "good", "luck"])
# hello world good luck
print(final_print)
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
A ```for``` loop is usually used for iterating over a sequence (either a list, a tuple, a dictionary, a set or a string)

``` python
# loop through a list
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)          # we will get apple, banana, cherry in sequence

# loop through a string
for i in "banana":
    print(i)        # we will get each character per line

# loop through a tuple
for i in ("name", "age"):
    print(i)        # we will get name and age in sequence

# loop through a dictionary
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
# we get the keys in sequence
# namingly brand, model, year
for i in thisdict:
    print(i)
```

**The ```break```, ```continue``` and ```else``` statement are also valid in ```for``` loop.**
``` python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
    if x == "banana":
        break
    print(x)        # only print apple since stop the loop when x == banana

for x in fruits:
    if x == "banana":
        continue
    print(x)        # print apple and cherry, we only stop the iteration when x == banana

for x in fruits:
    print(x)
else:
    print("printed all fruits")     # this line will be printed
```

**The range() Function**

The ```range()``` function returns a sequence of numbers, starting from 0 by default, and increments by by default, and ends at a specified number not including. We can specify by range(start, end, increment).
``` python
for x in range(6):
  print(x)              # we can get numbers from 0 to 5
  
for x in range(2, 30, 3):
  print(x)              # we can get numbers 2, 5, 8, 11, 14, 17, 20, 23, 26, 29
  
# a more C style for loop through a list
items = ['a', 'b', 'c', 'd']
for i in range(len(items)):
    print(items[i])
```

**nested loops**

A nested loop is a loop inside a loop
``` python
adj = ["red", "big", "tasty"]
fruits = ["apple", "banana", "cherry"]

for x in adj:
  for y in fruits:
    print(x, y)

# output is
# red apple
# red banana
# red cherry
# big apple
# big banana
# big cherry
# tasty apple
# tasty banana
# tasty cherry
```
### Python Switch statement
Python ```switch``` statement is only available for Python 3.10 and above.

``` python
match argument:
    case 0:
        return "zero"
    case 1:
        return "one"
    case 2:
        return "two"
    case default:
        return "something"
```
which is the same as:
``` python
if argument == 0:
    print("zero")
elif argument == 1: 
    print("one")
elif argument == 2:
    print("two")
else:
    print("something")
```
## Python Lists
- lists are sequential containers of memory.
- Values are referenced by their integer index that represents their location in an order.
- List items are ordered, changeable, and allow duplicate values.
- List items can be of any data type.

More functions and methods on Python list:
``` python
# list
l = [1, 2, 3, "this", 5.6, False, True]

# append an item at the end of the list
l.append("hello")
print(l)                    # [1, 2, 3, 'this', 5.6, False, True, 'hello']

# get a copy of l called l2
l2 = l.copy()
print(l2)                   # [1, 2, 3, 'this', 5.6, False, True, 'hello']

# get the number of given item
# True is also 1, 1 is also True
print(l.count(1))           # 2
print(l.count(True))        # 2

# get the item at the first appearance
print(l.index(1))           # 0

# append another list at the end of the list
new_l = ["good"]
l.extend(new_l)
print(l)                    # [1, 2, 3, 'this', 5.6, False, True, 'hello', 'good']

# insert at a given position
l.insert(0, 'h')
print(l)                    # ['h', 1, 2, 3, 'this', 5.6, False, True, 'hello', 'good']

# remove at a given position
l.pop(-1)
print(l)                    # ['h', 1, 2, 3, 'this', 5.6, False, True, 'hello']

# reverse a list
l.reverse()
print(l)                    # ['hello', True, False, 5.6, 'this', 3, 2, 1, 'h']

# sort the list
num_l = [5, 1, 3]
num_l.sort()
print(num_l)                # [1, 3, 5]

alpha_l = ["Hello", "hello", "good"]
alpha_l.sort()
print(alpha_l)              # ['Hello', 'good', 'hello']

l.sort()
print(l)                    # receive a TypeError, we need to make sure these are comparable types

# remove the first matching element from the list
l.remove("this")
print(l)                    # ['hello', True, False, 5.6, 3, 2, 1, 'h']

# list slicing (get part of the list)
# start:end but not including the end index
print(l[1:5])              # [True, False, 5.6, 3]

# completely clear a list
l.clear()
print(l)                    # []
```

**enumerate()**

Enumerate() method adds a counter to an iterable and returns it in a form of enumberating object. The syntax is enumberate(iterable, start=0) where iterable is any object that supports iteration, and start means the index value from which the counter is to be started, by default it is 0.
``` python
items = ['a', 'b', 'c', 'd']

# [(0, 'a'), (1, 'b'), (2, 'c'), (3, 'd')]
print(list(enumerate(items)))

# [(5, 'a'), (6, 'b'), (7, 'c'), (8, 'd')]
print(list(enumerate(items, start=5)))
```

## Python Dictionaries
- Dictionaries are associative containers of memory.
- Values are referenced by their string key that maps to a value.
- Dictionaries are used to store data values in key:value pairs.
- Dictionary items are ordered, changeable, and does not allow duplicates.
- The values in dictionary items can be of any data type.

``` python
# dictionary
dic = {
    "COMP1511" : "Programming Fundamentals",
    "COMP1521" : "OS Fundamentals",
    "COMP1531" : "Software Fundamentals"
}

# {'COMP1511': 'Programming Fundamentals', 'COMP1521': 'OS Fundamentals', 'COMP1531': 'Software Fundamentals'}
print(dic)

# get the keys or values of a dictionary
print(dic.keys())               # dict_keys(['COMP1511', 'COMP1521', 'COMP1531'])
print(type(dic.keys()))         # <class 'dict_keys'>
print(dic.values())             # dict_values(['Programming Fundamentals', 'OS Fundamentals', 'Software Fundamentals'])
print(type(dic.values()))       # <class 'dict_values'>

# we can loop through keys and values
for i in dic.keys():
    print(i)                    # print 'COMP1511', 'COMP1521', 'COMP1531' in sequence

# copy a dictionary
dic2 = dic.copy()
print(dic2)                     # {'COMP1511': 'Programming Fundamentals', 'COMP1521': 'OS Fundamentals', 'COMP1531': 'Software Fundamentals'}

# get a matching value of a key
print(dic.get("COMP1511"))      # Programming Fundamentals

# see all items as tuples
# ('COMP1511', 'Programming Fundamentals')
t1 = dic.items()
# dict_items([('COMP1511', 'Programming Fundamentals'), ('COMP1521', 'OS Fundamentals'), ('COMP1531', 'Software Fundamentals')])
print(t1)
# <class 'dict_items'>
print(type(t1))

# t1 is an iterable with tuples, we can loop through it
for i in t1:
    # print ('COMP1511', 'Programming Fundamentals'), ('COMP1521', 'OS Fundamentals'), ('COMP1531', 'Software Fundamentals') in sequence
    print(i)

# pop the last item
dic.popitem()
print(dic)                      # {'COMP1511': 'Programming Fundamentals', 'COMP1521': 'OS Fundamentals'}

# pop a specified item
dic.pop("COMP1521")
print(dic)                      # {'COMP1511': 'Programming Fundamentals'}

# increase an item
dic.update({"COMP1521": "Operating System Fundamentals"})
print(dic)                      # {'COMP1511': 'Programming Fundamentals', 'COMP1521': 'Operating System Fundamentals'}

# we can directly give a value to a key that is not created before
dic["COMP1531"] = "Software Fundamentals"
print(dic)                      # {'COMP1511': 'Programming Fundamentals', 'COMP1521': 'Operating System Fundamentals', 'COMP1531': 'Software Fundamentals'}

# The setdefault() method returns the value of a key (if the key is in dictionary). If not, it inserts key with a value to the dictionary.
print(dic.setdefault("COMP1511", 21))       # Programming Fundamentals
print(dic.setdefault("COMP2511", 22))       # 22
# {'COMP1511': 'Programming Fundamentals', 'COMP1521': 'Operating System Fundamentals', 'COMP1531': 'Software Fundamentals', 'COMP2511': 22}
print(dic)

# clear the dictionary
dic.clear()
print(dic)                                  # {}

# example: grap information from a long list and increment this value by 1
# if the key exists and set value to 1 if the key shows up for the first time
my_list = ["a", "b", "a", "c", "m", "a", "c"]
my_dict = {}
for i in my_list:
    my_dict[i] = my_dict.setdefault(i, 0) + 1

# {'a': 3, 'b': 1, 'c': 2, 'm': 1}
print(my_dict)

# Convert two lists into a dictionary with zip function
# The zip() function returns a zip object
# which is an iterator of tuples where the first item in each passed iterator
# is paired together, and then the second item in each passed iterator
# are paired together etc.
keys = ['Ten', 'Twenty', 'Thirty']
values = [10, 20, 30]
print(zip(keys, values))            # <zip object at 0x7f81be4ba280>
res_dict = dict(zip(keys, values))
print(res_dict)                     # {'Ten': 10, 'Twenty': 20, 'Thirty': 30}
```

## Python Tuples
- tuples are similar to lists except they are read-only once created and we should create them with ()
- Tuple items are ordered, unchangeable, and allow duplicate values.
- To create a tuple with only one item, you have to add a comma after the item, otherwise Python will not recognize it as a tuple.
- Tuple items can be of any data types.

``` python
# tuple
# tuple is immutable
t = (1, "this", 3.6, True)

# count how many elements inside the tuple
print(len(t))                   # 4

# count the number of matching item
num = t.count(1)
print(num)                      # 2

# search the index for matching item
match = t.index("this")
print(match)                    # 1
```

**unpacking tuples**

Unpacking tuples means assigning individual elements of a tuple to multiple variables.
The first variable will match the first element of the tuple and so on.
``` python
items = [(1, 'a'), (2, 'b'), (3, 'c')]

# 1, a
# 2, b
# 3, c
for number, char in items:
    print(f"{number}, {char}")
```

## Python Sets
- Set items are unordered, unchangeable, and do not allow duplicate values.
- Set items can be of any data type.

More methods and functions on Python sets
``` python
# set
# we can also create a set by set()
se1 = {1, 3.0, "this"}
se2 = set([True, "this", "is", 6.2])

# add an element to the set
se1.add("hi")
print(se1)                      # {1, 'this', 3.0, 'hi'}

# difference() returns the difference between two sets which is also a set. It doesn't modify the original sets.
print(se1.difference(se2))      # {'hi', 3.0}

# remove an element. If the element is not a member, raises a KeyError
se1.remove('hi')
print(se1)                      # {1, 'this', 3.0}

# the pop() method randomly removes an item from a set and returns the removed item
print(se1.pop())                # this
print(se1)                      # {1, 3.0}

# if the two sets are disjoint
print(se1.isdisjoint(se2))      # False

# if is subset
print(se1.issubset(se2))        # False

# if is superset
print(se1.issuperset(se2))      # False

# intersection
print(se1.intersection(se2))    # {1}

# The intersection_update() updates the set calling intersection_update() method with the intersection of sets.
se1.intersection_update(se2)
print(se1)                      # {1}

# union
print(se1.union(se2))           # {1, 'is', 6.2, 'this'}

# join two sets
se1.update(se2)
print(se1)                      # {1, 'is', 6.2, 'this'}

# discard() Removes an element from the set if it is a member. (Do nothing if the element is not in set)
se1.discard("this")             # {1, 'is', 6.2}
print(se1)

# The Python symmetric_difference() method returns the symmetric difference of two sets.
print(se1.symmetric_difference(se2))    # {'this'}
```

## Python Functions
- A function is a block of code which only runs when it is called
- we can pass data as paramenters into a function
- in Python, a function is declared by the ```def``` keyword
``` python
def my_function():
    print("Hello World")
    
# to call a function, use the function name followed by parenthesis
my_function()
```

**arguments**
- data can be passed into functions as arguments
- data we sent can be any type including list, dictionary ...
- arguments are specified after the function name, inside the parentheses
- we can add as many arguments as we want as long as they are corresponding to the function defination

``` python
def my_function(name):
  print("Hello " + name)

my_function("Justin")               # Hello Justin
my_function("John")                 # Hello John
my_function("Tony")                 # Hello Tony
```

**parameters or arguments?**

From the function's perspective:
- a parameter is the variable listed inside the parentheses in the function definition
- an argument is the value that is sent to the function when it is called

**keyword arguments**

We can send arguments with the key = value syntax where the order of the arguments does not matter.
``` python
def my_function(child3, child2, child1):
  print("The youngest child is " + child3)

# The youngest child is Linus
my_function(child1 = "Emil", child2 = "Tobias", child3 = "Linus")

# another very good example is to print a line without a newline at the end
print("Hello World", end="")            # this prints Hello World without a newline
```

**default parameter value**

If we call the function without argument, it uses the default value
``` python
def my_function(country = "Norway"):
  print("I am from " + country)

my_function("Sweden")       # I am from Sweden
my_function("India")        # I am from India
my_function()               # I am from Norway
my_function("Brazil")       # I am from Brazil
```

**return values**

To let a function return a value, use the ```return``` statement.
``` python
def my_function(x):
  return 5 * x
    
print(my_function(3))       # 8
print(my_function(5))       # 10
print(my_function(9))       # 14
```
## Python Errors and Exceptions
There are two distinguishable kinds of errors: syntax errors and exceptions
### Syntax Errors
- syntax errors, also known as parsing errors, are perhaps the most common kind of complaint.
- syntax errors are produced by python when it is translating the source code into byte code.
- python syntax errors can cause the code failed to compile.
``` python
>>> while True print('Hello world')
  File "<stdin>", line 1
    while True print('Hello world')
                   ^
SyntaxError: invalid syntax
```

### Exceptions
- An exception is an action that disrupts the normal flow of a program.
- this action is often representative of an error being thrown
- exceptions are ways that we can elegantly recover from errors
- these exceptions can be handled using the ```try``` statement
- the ```try``` block lets you test a block of code for errors
- the ```except``` block lets you handle the error
- the ```else``` block lets you execute code when there is no error
- the ```finally``` block lets you execute code, regardsless of the result of the try and except blocks

``` python
try:
  print(x)
except:
  print("An exception occurred")        # this piece of code only runs when there's an exception
```

**many exceptions**

We can define as many exception blocks as we want and deal with it to a specific exception
``` python
try:
  print(x)
except NameError:
  print("Variable x is not defined")    # runs when there's a NameError
except:
  print("Something else went wrong")    # runs when any exception other than NameError
```

**else**

We can use the ```else``` keyword to define a block of code to be executed if no errors were raised
``` python
try:
  print("Hello")
except:
  print("Something went wrong")
else:
  print("Nothing went wrong")       # only runs when there's no exception
```

**finally**

The ```finally``` block, if specified, will be executed regardless if the try block raises an error or not.
``` python
try:
  print(x)
except:
  print("Something went wrong")
finally:
  print("The 'try except' is finished")     # this line will run anyway
```

### Raise an exception
As a Python developer, we can choose to throw an exception if a condition occurs.
To throw an exception, use the ```raise``` keyword.
``` python
x = -1

if x < 0:
  raise Exception("Sorry, no numbers below zero")
```
We can define what kind of error to raise, and the text to print to the user.
``` python
x = "hello"

if not type(x) is int:
  raise TypeError("Only integers are allowed")
```

# Python advanced syntax
## Python Recursion
Recursion means defining a problem in terms of itself.
We alreaady known that a function can call other functions.
It is also possible that the function calls itself and this type of construct is termed as recursive function.

``` python
def factorial(x):
    """This is a recursive function
    to find the factorial of an integer"""

    if x == 1:
        return 1
    else:
        return (x * factorial(x-1))


num = 3
# The factorial of 3 is 6
print("The factorial of", num, "is", factorial(num))

# in details
factorial(3)          # 1st call with 3
3 * factorial(2)      # 2nd call with 2
3 * 2 * factorial(1)  # 3rd call with 1
# our recursion ends when the number reduces to 1.
# this is called the base condition.
3 * 2 * 1             # return from 3rd call as number=1
3 * 2                 # return from 2nd call
6                     # return from 1st call
```
By default, the maximum depth of recursion is 1000.
If the limit is crossed, it results in RecursionError.

**Advantages of recursion**
1. Recursive functions make the code look clean and elegant.
2. A complex task can be broken down into simpler sub-problems using recursion.
3. Sequence generation is easier with recursion than using some nested iteration.

**Disadvantages of recursion**
1. Sometimes the logic behind recursion is hard to follow through.
2. Recursive calls are expensive (inefficient) as they take up a lot of memory and time.
3. Recursive functions are hard to debug.

**Recursion or Iteration**
- Recursion is when a function calls itself within its code, thus repeatedly executing the instructions present inside it. 
- Iteration is when a loop repeatedly executes the set of instructions like "for" loops and "while" loops.
- Recursion is made for solving problems that can be broken down into smaller, repetitive problems. It is especially good for working on things that have many possible branches and are too complex for an iterative approach.
- Recursion is particularly useful when dealing with tree structures.
- Recursion is a useful tool, but it can increase memory usage.

## Python Anonymous Function
- In Python, an anonymous function is a function that is defined without a name.
- while normal functions are defined using the ```def``` keyword in Python, anonymous functions are defined using the ```lambda``` keyword.
- Hence, anonymous functions are also called lambda functions.
- Lambda functions can have any number of arguments but only one expression.
- Lambda functions can be used wherever function objects are required.

**Syntax of lambda function in Python**
``` python
lambda arguments: expression
```
Example:
``` python
# Program to show the use of lambda functions
double = lambda x: x * 2

print(double(5))                # 10
'''
The lambda function is exactly the same as:
def double(x):
   return x * 2
'''
```

## Python map(), filter() and reduce()
### Python map()
The ```map()``` function applies a given function to each item of an iterable(list, tuple etc.) and returns an iterator.

**Syntax for map()**
``` python
map(function, iterable, ...)
```
- The ```map()``` takes two parameters
- function - a function that perform some action to each element of an iterable
- iterable - an iterable like sets, lists, tuples etc
- we can pass more than one iterable to the ```map()``` function
- The ```map()``` function returns an object of map class.
- The returned value can be passed to functions like list() which ocnverts to a list and set() whcih converts to a set
``` python
def calculateSquare(n):
    return n*n

numbers = (1, 2, 3, 4)
result = map(calculateSquare, numbers)
print(result)                           # <map object at 0x7f722da129e8>

# converting map object to set
numbersSquare = set(result)
print(numbersSquare)                    # {16, 1, 4, 9}
```
It would be easier to achieve the same result with lambda functions
``` python
numbers = (1, 2, 3, 4)
result = map(lambda x: x*x, numbers)
print(result)                           # <map 0x7fafc21ccb00>

# converting map object to set
numbersSquare = set(result)
print(numbersSquare)                    # {16, 1, 4, 9}
```
We can pass multiple iterators to map() using lambda
``` python
num1 = [4, 5, 6]
num2 = [5, 6, 7]

result = map(lambda n1, n2: n1+n2, num1, num2)
# this added the matching values from the first list and second list and append them to a map class
print(list(result))             # [9, 11, 13]
```
## Python Extended Keyword Arguments
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

### Regular Expression special characters
- ```.```: In the default mode, this matches any character except a newline. If the DOTALL flag has been specified, this matches any character including a newline.
- ```^```: Matches the start of the string.
- ```$```: Matches the end of the string or just before the newline at the end of the string.
- ```*```: Causes the resulting RE to match 0 or more repetitions of the preceding RE, as many repetitions as are possible.
- ```+```: Causes the resulting RE to match 1 or more repetitions of the preceding RE.
- ```?```: Causes the resulting RE to match 0 or 1 repetitions of the preceding RE.
- ```{m}```: Specifies that exactly m copies of the previous RE should be matched; fewer matches cause the entire RE not to match.
- ```{m ,n}```: Causes the resulting RE to match from m to n repetitions of the preceding RE, attempting to match as many repetitions as possible.
- ```{m, n}?```: Causes the resulting RE to match from m to n repetitions of the preceding RE, attempting to match as few repetitions as possible.
- ```\```: Either escapes special characters (permitting you to match characters like ```*```, ```?```, and so forth inside a string if we have ```\*```, ```\?``` and so fourth), or signals a special sequence.
- ```[]```: Used to indicate a set of characters.
    - Characters can be listed individually, e.g. [amk] will match 'a', 'm', or 'k'.
    - Ranges of characters can be indicated by giving two characters and separating them by a '-', for example [a-z] will match any lowercase ASCII letter, [0-5][0-9] will match all the two-digits numbers from 00 to 59.
    - Special characters lose their special meaning inside sets. For example, [(+*)] will match any of the literal characters '(', '+', '*', or ')'.
- ```|```: A|B, where A and B can be arbitrary REs, creates a regular expression that will match either A or B.
- ```(...)```: Matches whatever regular expression is inside the parentheses, and indicates the start and end of a group; the contents of a group can be retrieved after a match has been performed. In other words, ```()``` can extract a specific part from a string.

### Python re package - useful functions
```re.search(regex, string, flags)```
- search for a regex match within string
- return object with information about match or None if match fails
- optional parameter modifies matching, e.g. make matching case-insensitive with: flags=re.I
``` python

```

```re.match(regex, string, flags)```
- only match at start of string
- same as re.search stating with ^
``` python
```

```re.fullmatch(regex, string, flags)```
- only match the full string
- same as re.search starting with ^ and ending with $
``` python
```

```re.sub(regex, replacement, string, count, flags)```
- return string with anywhere regex matches, substituted by replacement
- optional parameter count, if non-zero, sets maximum number of substitutions
``` python

```

```re.findall(regex, string, flags)```
- return all non-overlapping matches of pattern in string
- if pattern contains () return part matched by ()
- if pattern contains multiple () return tuple
``` python

```

```re.split(regex, string, maxsplit, flags)```
- Split string everywhere regex matches
- optional parameter maxsplit, if non-zero, set maximum number of splits
``` python

```

```re.finditer(pattern, string, flags)```
- return an iterator yielding match objects over all non-overlapping matches for the RE pattern in string.
- the string is scanned left-to-right, and matches are returned in the order found.
``` python

```

### Character classes
Python regular expression adds character classes
- \d - matches any digit, for ASCII: [0-9]
- \D - matches any non-digit, for ASCII: [^0-9]
- \w - matches any word char, for ASCII: [a-zA-Z_0-9]
- \W - matches any non-word char, for ASCII: [^a-zA-Z_0-9]
- \s - matches any whitespace, for ASCII: [ \t\n\r\f]
- \S - matches any non-whitespace, for ASCII: [^ \t\n\r\f]
- \b - matches at a word boundary
- \B - matches except at a word boundary
- \A - matches at the start of the string, same as ^
- \Z - matches at the end of the string, same as $

### raw strings
- python raw-string is prefixed with an r (for raw)
- backslashes have no special meaning in raw-string except before quotes
- regexes often contain backslashes - using raw-strings makes them more readable

``` python
# Hello
# Andrew
print('Hello\nAndrew')

# Hello\nAndrew
print(r'Hello\nAndrew')

print( r'Hello\nAndrew' == 'Hello\\nAndrew')                 # True

len('\n')               # 1
len(r'\n')              # 2
```

### Match objects
- re.search, re.match, re.fullmatch return a match object if a match suceeds, None if it fails
- Match objects always have a boolean value of True.
- Match objects support some methods and attributes

``` python

```

### Back-referencing
- \number can be used further on in a regex - often called a back-reference
- back-references allow matching impossible with classical regular expressions
- python supports up to 99 back-references, \1, \2 ... \99
- \01 or \100 is interpreted as an octal number

``` python
>>> re.search(r'^(\d+) (\d+)$', '42 43')
<re.Match object; span=(0, 5), match='42 43'>
# the following returns None cause 43 does not equal to 42, the back-referencing \1 ensures the two numbers must be the same
>>> re.search(r'^(\d+) (\1)$', '42 43')
>>> re.search(r'^(\d+) (\1)$', '42 42')
<re.Match object; span=(0, 5), match='42 42'>
```

### Non-Capturing Group
- ```()``` is a non-capturing group
- it has the same grouping behaviour as (...)
- it doesn't capture the part of the string matched by the group

``` python
m = re.search(r'.*(?:[aeiou]).*([aeiou]).*', 'abcde')
print(m)                # <re.Match object; span=(0, 5), match='abcde'>

print(m.groups())       # ('e',)

print(m.group(1))       # e
```

### Greedy vs non-Greedy pattern matching
- the default semantics for pattern matching is greedy
- starts match the first place it can succeed
- make the match as long as possible
- the ```?``` operator changes pattern matching to non-greedy
- also starts match the first place it can succeed
- make the match as short as possible

``` python
s = 'abbbc'
print(re.sub(r'ab+', 'X', s))     # Xc

print( re.sub(r'ab+?', 'X', s))   # Xbbc
```

## Python with Database
## Python with Statistics
``` python
import statistics
```

Averages and measures of central location
- mean() - arithmetic mean (average) of data
- fmean() - fast, floating point arithmetic mean
- geometric_mean() - geometric mean of data
- harmonic_mean() - harmonic mean of data
- median() - median (middle value) of data
- median_low() - low median of data
- median_high() - high median of data
- mode() - single mode (most common value) of discrete or nominal data
- multimode() - list of modes of discrete or nominal data
- quantiles() - divide data into intervals with equal probability


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
swap values of two variables
``` python
first = 1
last = 5
first, last = last, first           # swap the values of first and last
print(first)                        # 5
print(last)                         # 1
```

unpacking tuples
``` python
tup = (1, 5)
first, last = tup
print(first)                        # 1
print(last)                         # 5
```
## Python pip
## Python virtural environment
## [Python Memory management](https://docs.python.org/3/c-api/memory.html#:~:text=Memory%20management%20in%20Python%20involves,by%20the%20Python%20memory%20manager.)
## Python virtural machine
## Python interpreter

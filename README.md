# Table of Contents
1. [Why Python](#why-python)
    1. [Python history](#python-history)
    2. [Python 2 and Python 3](#python-2-and-python-3)
    3. [Why Python is popular](#why-python-is-popular)
    4. [Why Python is slow](#why-python-is-slow)
2. [Python Basics](#python-basics)
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
    14. [Python User-Defined Modules](#python-user-defined-modules)
    15. [Python File Handling and with Statement](#python-file-handling-and-with-statement)
    16. [Python Properties to Note](#python-properties-to-note)
3. [Advanced Python](#advanced-python)
	1. [pip and Virtual Environment](#pip-and-virtual-environment)
    2. [Python Recursion](#python-recursion)
    3. [Python Anonymous Function](#python-anonymous-function)
    4. [Python map(), filter() and reduce()](#python-map-filter-and-reduce)
    5. [Python Extended Keyword Arguments](#python-extended-keyword-arguments)
    6. [Python Generators](#python-generators)
    7. [Python Iterators](#python-iterators)
    8. [Python Decorators](#python-decorators)
4. [Python Object Oriented Programming](#python-object-oriented-programming)
	1. [Basic OOP concepts](#basic-oop-concepts)
	2. [Python Classes and Objects](#python-classes-and-objects)
	3. [Python Property](#python-property)
	4. [Python Inheritance](#python-inheritance)
5. [Python with Data Structure and Algorithms](#python-with-data-structure-and-algorithms)
    1. [Python Linked Lists](#python-linked-lists)
    2. [Python Stack](#python-stack)
    3. [Python Queue](#python-queue)
    4. [Python Trees](#python-trees)
    5. [Python Graphs](#python-graphs)
    6. [Python Searching Algorithms](#python-searching-algorithms)
	    1. [Linear Search](#linear-search)
	    2. [Binary Search](#binary-search)
    7. [Python Sorting Algorithms](#python-sorting-algorithms)
		1. [Bubble Sort](#bubble-sort)
	    2. [Selection Sort](#selection-sort)
		3. [Insertion Sort](#insertion-sort)
		4. [Merge Sort](#merge-sort)
		5. [Quick Sort](#quick-sort)
		6. [Shell Sort](#shell-sort)
		7. [Heap Sort](#heap-sort)
		8. [Counting Sort](#counting-sort)
		9. [Bucket Sort](#bucket-sort)
		10. [Radix Sort](#radix-sort)
	8. [Greedy Algorithms](#greedy-algorithms)
6. [Python with other modules](#python-with-other-modules)
    1. [Python with Flask](#python-with-flask)
    2. [Python with Subprocess](#python-with-subprocess)
    3. [Python with Regular expression](#python-with-regular-expression)
    4. [Python with Database](#python-with-database)
    5. [Python with Statistics](#python-with-statistics)
    6. [Python with Math](#python-with-math)
    7. [Python with Sys](#python-with-sys)
    8. [Python with Collections](#python-with-collections)
    9. [Python with Random](#python-with-random)
    10. [Python with JSON](#python-with-json)
    11. [Python with CSV](#python-with-csv)
    12. [Python with Datetime](#python-with-datetime)
    13. [Python with Typing](#python-with-typing)
    14. [Python with Argparse](#python-with-argparse)
    15. [Python with OS](#python-with-os)
7. [Python Program Testing and Debugging](#python-program-testing-and-debugging)

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
7. Python works on different platforms (Windows, Mac, Linux ...)
8. Python has procedural, object-orientated and functional properties

## Why Python is slow
Unlike native languages like C/C++, Python code gets interpreted at runtime instead of being compiled to native code at compile time. Python is an interpreted language, which means that the Python code we write must go through many, many stages of abstraction before it can become executable machine code.

Python code is first compiled into python Byte Code. The Byte Code interpreter conversion happens internally and most of it is hidden from the developer.Byte code is platform-independent and lower-level programming. Compilation of byte code is to ramp up the execution of source code. The source code compiled to byte code is then executed in Python’s virtual machine one by one, to carry out the operations. The virtual machine is an internal component of Python. Internally Python code is interpreted during run time rather than being compiled to native code hence it is a bit slower. 

# Python Basics

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

### Scope of variables (Global vs Local)
Global variables are those which are not defined inside any function and have a global scope whereas local variables are those which are defined inside a function and its scope is limited to that function only.

``` python
def func():
    # the local variable just belongs to the local scope
    # the variable string does not exist outside of the function
    string = "local variable"
    print("This is a", string)

def change():
    # if we want to change the variable of global scope
    # we need to use the global variable first
    global string
    string = "now has changed"

string = "global scope"
print(string)       # global scope
# calling a func() would not change the variable in global scope
func()              # This is a local variable
# change() can change the variable in global scope
change()
print(string)       # now has changed
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

# '>>' is Zero fill left shift, it shifts left by pushing zeros 
# in from the right and let the leftmost bits fall off
print(5 >> 2 )         # 0101 >> 2 => 0001 => 1

# '<<' is Signed right shift, it shifts right by pushing copies 
# of the leftmost bit in from the left, and let the rightmost bits fall off
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
# 140378634129696 (but every time you run this command, we get a different result)
print(id(string))

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

# strip() method is to remove the leading and 
# the trailing characters based on the string argument passed
new_string = "    cool and i like it      \n"
print(new_string.strip())                   # cool and i like it

# rstrip() only removes the trailing characters
print(new_string.rstrip())                  #     cool and i like it

# lstrip() only removes the leading characters
# cool and i like it      \n (\n is interpreted as a newline)
print(new_string.lstrip())
# we can specify a character
new_string = "HHHHHcool and i like itHHHHH"
print(new_string.strip("H"))                # cool and i like it

# check if a string starts with another string
print(string.startswith("Hello"))           # True

# string format
# print specific number of digits
f = 3.1415926
print("{:.3f}".format(f))                   # 3.142

num = 1234546
print(f"{num:10}")                          # '   1234546'
print(f"{num:10,}")                         # ' 1,234,546'
print(f"{str(num):10}")                     # '1234546   '

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

#### if
- An if statement is written by using the ```if``` keyword.
- Python relies on indentation (whitespace at the beginning of a line) to define scope in the code.
- The code with indentation under if statement will run if the condition is True.

``` python
a = 5
b = 6
if a > b:
	# we will not see this line because the condition is False and the line will not be executed
    print("5 is greater than 6")    

if a < b:
	# we can see this line because the condition is True
    print("5 is less than 6")
```

#### elif

The ```elif``` keyword is pythons way of saying if the previous conditions were false, then try to check this condition.
``` python
a = 33
b = 33
if b > a:
  print("b is greater than a")      # failed this check
elif a == b:
  print("a and b are equal")        # passed this check and print the line
```

#### else

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

#### short hand if

if you have only one statement to execute, you can put it on the same line as the if statement
``` python
if a > b: print("a is greater than b")
# this is the same as:
# if a > b:
#     print("a is greater than b")
```

#### short hand if .. else
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

#### nested if

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

#### pass

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

#### break

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

#### continue

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

#### else

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

#### The range() Function

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

#### nested loops

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

Switch statment is simply another form of writing if .. else statements.

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
    return "zero"
elif argument == 1: 
    return "one"
elif argument == 2:
    return "two"
else:
    return "something"
```
## Python Lists
- lists are sequential containers of memory.
- Values are referenced by their integer index that represents their location in an order.
- List items are ordered, changeable, and allow duplicate values.
- List items can be of any data type.

Time complexity of list operations on Average and Worst cases:
| Operation | Average | Worst |
| --------- | ------- | ----- |
| Copy | O(n) | O(n) |
| Append | O(1) | O(1) |
| Pop last | O(1) | O(1) |
| Pop intermediate | O(n) | O(n) |
| Insert | O(n) | O(n) |
| Get item | O(1) | O(1) |
| Set item | O(1) | O(1) |
| Delete item | O(n) | O(n) |
| Iteration | O(n) | O(n) |
| Get slice | O(k) | O(k) |
| Set slice | O(k+n) | O(k+n) |
| Del slice | O(n) | O(n) |
| Extend | O(k) | O(k) |
| Sort | O(n log n) | O(n log n) |
| Multiply | O(nk) | O(nk) |
| x in s | O(n) | O(n) |
| min(s), max(x) |  O(n) | O(n) |
| Get length | O(1) | O(1) |

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

### enumerate()

Enumerate() method adds a counter to an iterable and returns it in a form of enumberating object. The syntax is enumberate(iterable, start=0) where iterable is any object that supports iteration, and start means the index value from which the counter is to be started, by default it is 0.
``` python
items = ['a', 'b', 'c', 'd']

# [(0, 'a'), (1, 'b'), (2, 'c'), (3, 'd')]
print(list(enumerate(items)))

# [(5, 'a'), (6, 'b'), (7, 'c'), (8, 'd')]
print(list(enumerate(items, start=5)))
```

### List comprehension
List comprehension offers a shorter syntax when you want to create a new list based on the values of an existing list.
The common Python code is:
``` python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = []

for x in fruits:
  if "a" in x:
    newlist.append(x)

print(newlist)
```
With list comprehension, we can rewrite as:
``` python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newlist = [x for x in fruits if "a" in x]

print(newlist)
```

## Python Dictionaries
- Dictionaries are associative containers of memory.
- Values are referenced by their string key that maps to a value.
- Dictionaries are used to store data values in key:value pairs.
- Dictionary items are ordered, changeable, and does not allow duplicates.
- The values in dictionary items can be of any data type.
- In Python, dictionary basically represents the implementation of hash table.

Time complexity of dict operations in average and worst cases
| Operation | Average | Worst |
| --------- | ------- | ----- |
| k in d | O(1) | O(n) |
| Copy | O(n) | O(n) |
| Get item | O(1) | O(n) |
| Set item | O(1) | O(n) |
| Delete item | O(1) | O(n) |
| iteration | O(n) | O(n) |

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

### unpacking tuples

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

### arguments
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

### parameters or arguments?

From the function's perspective:
- a parameter is the variable listed inside the parentheses in the function definition
- an argument is the value that is sent to the function when it is called

### keyword arguments

We can send arguments with the key = value syntax where the order of the arguments does not matter.
``` python
def my_function(child3, child2, child1):
  print("The youngest child is " + child3)

# The youngest child is Linus
my_function(child1 = "Emil", child2 = "Tobias", child3 = "Linus")

# another very good example is to print a line without a newline at the end
print("Hello World", end="")            # this prints Hello World without a newline
```

### default parameter value

If we call the function without argument, it uses the default value
``` python
def my_function(country = "Norway"):
  print("I am from " + country)

my_function("Sweden")       # I am from Sweden
my_function("India")        # I am from India
my_function()               # I am from Norway
my_function("Brazil")       # I am from Brazil
```

### return values

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

### many exceptions

We can define as many exception blocks as we want and deal with it to a specific exception
``` python
try:
  print(x)
except NameError:
  print("Variable x is not defined")    # runs when there's a NameError
except:
  print("Something else went wrong")    # runs when any exception other than NameError
```

### else

We can use the ```else``` keyword to define a block of code to be executed if no errors were raised
``` python
try:
  print("Hello")
except:
  print("Something went wrong")
else:
  print("Nothing went wrong")       # only runs when there's no exception
```

### finally

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

## Python User-Defined Modules

### What is a module
Modules refer to a file containing Python statements and definitions.

A file containing Python code, for example: example.py, is called a module, and its module name would be example.

We use modules to break down large programs into small manageable and organized files.
We can define our most used functions in a module and import it, instead of copying their definitions into different programs.

### How to import modules in Python
We can import the definitions inside a module to another module or the interactive interpreter in Python.

We use the import keyword to do this. To import our previously defined module example, we type the following in the Python prompt.

``` python
# if there is file called example.py
import example
```

### Import with renaming
We can import a module by renaming it as follows:
``` python
# import module by renaming it

import math as m
print("The value of pi is", m.pi)
```

### Python from...import statement
We can import specific names from a module without importing the module as a whole.
``` python
# import only pi from math module

from math import pi
print("The value of pi is", pi)
```

***Notice**: when importing a module, basically it imports every code in the file. So codes in the main function will also run after imported. To avoid the issue, we bound the main function by ```if __name__ == '__main__':```.

Example:
``` python
if __name__ == "__main__":
    print("Hello, World!")
    
# the code only runs when we execute the file
# the code will not run in the file which imports the module
```

## Python File Handling and with Statement
Files are named locations on disk to store related information.
They are used to permanently store data in a non-volatile memory (hard disk).
Since Random Access Memory (RAM) is volatile (which loses its data when the computer is turned off), we use files for future use of the data by permanently storing them.

In Python, a file operation takes place in the folllowing order:
1. Open a file
2. Read or write (perform operation)
3. Close the file

### Opening Files in Python
We can sepcify the mode while opening a file.

| Mode | Description |
| ---- | ----------- |
| r | Opens a file for reading. (default) |
| w | Opens a file for writing. Creates a new file if it does not exist or truncates the file if it exists. | 
| x | Opens a file for exclusive creation. If the file already exists, the operation fails. |
| a | Opens a file for appending at the end of the file without truncating it. Creates a new file if it does not exist. |
| t | Opens in text mode. (default) |
| b | Opens in binary mode. |
| + | Opens a file for updating (reading and writing) |

``` python
f = open("test.txt")      # equivalent to 'r' or 'rt'
f = open("test.txt",'w')  # write in text mode
f = open("img.bmp",'r+b') # read and write in binary mode
```

### Closing Files in Python
When we are done with performing operations on the file, we need to properly close the file.

Closing a file will free up the resources that were tied with the file. It is done using the close() method available in Python.

Python has a garbage collector to clean up unreferenced objects but we must not rely on it to close the file.

``` python
f = open("test.txt", encoding = 'utf-8')
# perform file operations
f.close()
```

A safer way is to use a try...finally block.
``` python
try:
   f = open("test.txt", encoding = 'utf-8')
   # perform file operations
finally:
   f.close()
```

### with Statement
However, the best way to close a file is by using the `with` statement. This ensures that the file is closed when the block inside the `with` statement is exited.

The with statement simplifies exception handling by encapsulating comon preparation and cleanup tasks.
In addition, it will automatically close the file.

``` python
with open("test.txt", encoding = 'utf-8') as f:
   # perform file operations
```

### Writing to Files in Python
In order to write into a file in Python, we need to open it in write `w`, append `a` or exclusive creation `x` mode.

We need to be careful with the `w` mode, as it will overwrite into the file if it already exists. Due to this, all the previous data are erased.

Writing a string or sequence of bytes (for binary files) is done using the `write()` method. This method returns the number of characters written to the file.

``` python
with open("test.txt",'w',encoding = 'utf-8') as f:
   f.write("my first file\n")
   f.write("This file\n\n")
   f.write("contains three lines\n")
```

This program will create a new file named `test.txt` in the current directory if it does not exist. If it does exist, it is overwritten.

### Reading Files in Python
We can use the `read(size)` method to read in the `size` number of data. If the `size` parameter is not specified, it reads and returns up to the end of the file.

``` python
>>> f = open("test.txt",'r',encoding = 'utf-8')
>>> f.read(4)    # read the first 4 data
'This'

>>> f.read(4)    # read the next 4 data
' is '

>>> f.read()     # read in the rest till end of file
'my first file\nThis file\ncontains three lines\n'

>>> f.read()  # further reading returns empty sting
''
```

We can change our current file cursor (position) using the `seek()` method. Similarly, the `tell()` method returns our current position (in number of bytes).
``` python
>>> f.tell()    # get the current file position
56

>>> f.seek(0)   # bring file cursor to initial position
0

>>> print(f.read())  # read the entire file
This is my first file
This file
contains three lines
```

We can also read a file line-by-line using a for loop.
``` python
with open('text.txt') as f:
	for line in f:
		print(line.strip())
```

Alternatiely, we can use the `readline()` method to read individual lines of a file.
This method reads a file till the newline, including the newline character.

``` python
>>> f.readline()
'This is my first file\n'

>>> f.readline()
'This file\n'

>>> f.readline()
'contains three lines\n'

>>> f.readline()
''
```

Moreover, the `readlines()` method returns a list of remaining lines of the entire file.
``` python
print(f.readlines())
# ['This is my first file\n', 'This file\n', 'contains three lines\n']
```

### More Python File Methods
| Method | Description |
| ------ | ----------- | 
| close() | Closes an opened file. It has no effect if the file is already closed.
| detach() | Separates the underlying binary buffer from the TextIOBase and returns it.
| fileno() | Returns an integer number (file descriptor) of the file.
| flush() | Flushes the write buffer of the file stream.
| isatty() | Returns True if the file stream is interactive.
| read(n) | Reads at most n characters from the file. Reads till end of file if it is negative or None.
| readable() | Returns True if the file stream can be read from.
| readline(n=-1) | Reads and returns one line from the file. Reads in at most n bytes if specified.
| readlines(n=-1) | Reads and returns a list of lines from the file. Reads in at most n bytes/characters if specified.
| seek(offset,from=SEEK_SET) | Changes the file position to offset bytes, in reference to from (start, current, end).
| seekable() | Returns True if the file stream supports random access.
| tell() | Returns an integer that represents the current position of the file's object.
| truncate(size=None) | Resizes the file stream to size bytes. If size is not specified, resizes to current location.
| writable() | Returns True if the file stream can be written to.
| write(s) | Writes the string s to the file and returns the number of characters written.
| writelines(lines) | Writes a list of lines to the file.

## Python Properties to Note
- Everything in Python is an object
- Every object in Python has a type
- type and class are synonymous

# Advanced Python

## pip and Virtual Environment

### Python pip
A package is a collection of files.

There are about 390000 packages available on PyPI which is a website that allows us to search for and register our own packages.

Any packages listed on the index can be installed via `pip`.

- `pip` is the standard package manager for Python
- `pip` can install any package on PyPI

To install a package, we can use the following command:
```
$ python3 -m pip install <package_name>
```

`pip` also updates and uninstalls package
```
$ python3 -m pip install --upgrade <package_name>
$ python3 -m pip uninstall <package_name>
```

`pip` can install package from a `requirements.txt` file directly
```
$ pip install -r requirements.txt
```

### Python virtural environment
By default, Python installs package in the global Python environment.
This is usually messy.

It is preferable to keep our package within the project that is using them.
This can be done by creating a virtual environment.

In Python, a virtual environment is a directory that contains a copy of the Python interpreter.
It can be used to isolate our project from the rest of the system.
It's common to simply name our virtual environment venv.

To create a virtual environment, use the following command:
```
$ python3 -m venv <venv_name>
```

Once we have a virtural environment, we can activate it by running the following command:
```
$ . <venv_name>/bin/activate
```
without activating a virtual environment, we are still in the global environment.

Once activated, the python, python3, pip etc commands will be run from within the virtual environment.

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

### Python filter()
Filter() is a built-in function in Python. The filter function can be applied to an iterable such as a list or a dictionary and create a new iterator.
This new iterator can filter out certain specific elements based on the condition that you provide very efficiently.

``` python
# with common functions
letters = ['a', 'b', 'd', 'e', 'i', 'j', 'o']

# a function that returns True if letter is vowel
def filter_vowels(letter):
    vowels = ['a', 'e', 'i', 'o', 'u']
    return True if letter in vowels else False

filtered_vowels = filter(filter_vowels, letters)

# converting to tuple
vowels = tuple(filtered_vowels)
# ('a', 'e', 'i', 'o')
print(vowels)

# with lambda functions inside filter()
numbers = [1, 2, 3, 4, 5, 6, 7]

# the lambda function returns True for even numbers 
even_numbers_iterator = filter(lambda x: (x%2 == 0), numbers)

# converting to list
even_numbers = list(even_numbers_iterator)

# [2, 4, 6]
print(even_numbers)
```

filter a dictionary by its values:
``` python
def findRepeatedDnaSequences(self, s: str) -> List[str]:
	ss = []
	for i in range(len(s)):
		if i + 10 <= len(s):
			ss.append(s[i:i+10])

	dicts = collections.Counter(ss)
	more_dicts = filter(lambda x: (dicts[x] > 1), dicts)
	return list(more_dicts)
```

### Python reduce()
The reduce() function facilitates a functional approach to Python programming.
It performs a rolling-computation as specified by the passed function to the neighboring elements, by taking a function and an iterable as arguments, and returns the final computed value.

``` python
from functools import reduce
result = reduce((lambda a, b: a + b), [1, 2, 3, 4])
# 10
print(result)
```

## Python Extended Keyword Arguments
*args and **kargs allows us to pass a varying number of positional arguments.

args is just a name, the important things here is the unpacking operator (*). It unpacks arguments as a tuple.

unpacking operator (**) unpacks keyword operators as a dictionary with keyword as keys.
``` python
def func(required, *args, **kwargs):
    # 1
    print(required)

    # (2, 3, 4)
    print(args)

    # {'good': 5, 'happy': 6}
    print(kwargs)

func(1, 2, 3, 4, good=5, happy=6)
```

## Python Generators

## Python Iterators

### Iterator vs Iterable
Lists, tuples, dictionaries and sets are all iterable objects are iterable containers which we can get an iterator from.

All these objects have a iter() method which is used to get an iterator.

Example: return an iterator from a tuple, and print each value:
``` python
mytuple = ("apple", "banana", "cherry")
myit = iter(mytuple)

print(next(myit))		# apple
print(next(myit))		# banana
print(next(myit))		# cherry
```

### Create an Iterator
To create an object/class as an iterator you have to implement the methods __iter__() and __next__() to your object.

The __iter__() method can do operations, but must always return the iterator object itself.

The __next__() method also allows us to do operations, and must return the next item in the sequence.

``` python
class MyNumbers:
  def __iter__(self):
    self.a = 1
    return self

  def __next__(self):
    x = self.a
    self.a += 1
    return x

myclass = MyNumbers()
myiter = iter(myclass)

print(next(myiter))		# 1
print(next(myiter))		# 2
print(next(myiter))		# 3
print(next(myiter))		# 4
print(next(myiter))		# 5
```

### StopIteration
THe example above would continue forever if we had enough next() statements, or it was used in a for loop.

To prevent the iteration to go on forever, we can use the StopIteration statement.

In the __next__() method, we can add a terminating condition to raise an error if the iteration is done a psecified number of times

``` python
class MyNumbers:
  def __iter__(self):
    self.a = 1
    return self

  def __next__(self):
    if self.a <= 20:
      x = self.a
      self.a += 1
      return x
    else:
      raise StopIteration

myclass = MyNumbers()
myiter = iter(myclass)

for x in myiter:
  # print from 1 to 20
  print(x)
```

## Python Decorators
A decorator is a design pattern in Python that allows a user to add new functionality to an existing object without modifying its structure.
Decorators are usually called before the definition of a function you want to decorate.

### Assigning Functions to Variables
We can assign the function to a variable and use this variable to call the function.
``` python
def plus_one(number):
    return number + 1

add_one = plus_one
add_one(5)		# 6
```

### Defining Functions Inside other Functions
``` python
def plus_one(number):
    def add_one(number):
        return number + 1


    result = add_one(number)
    return result
plus_one(4)		# 5
```

### Passing Functions as Arguments to other Functions
Functions can also be passed as parameters to other functions.
``` python
def plus_one(number):
    return number + 1

def function_call(function):
    number_to_add = 5
    return function(number_to_add)

function_call(plus_one)		# 6
```

### Functions Returning other Functions
A function can also generate another function.
``` python
def hello_function():
    def say_hi():
        return "Hi"
    return say_hi
hello = hello_function()
hello()			# 'Hi'
```

### Nested Functions have access to the Enclosing Functions' Variable Scope
Python allows a nested function to access the outer scope of the enclosing function.
``` python
def print_message(message):
    "Enclosong Function"
    def message_sender():
        "Nested Function"
        print(message)

    message_sender()

print_message("Some random message")	# Some random message
```

### Creating Decorators
``` python
def uppercase_decorator(function):
    def wrapper():
        func = function()
        make_uppercase = func.upper()
        return make_uppercase

    return wrapper

def say_hi():
    return 'hello there'

decorate = uppercase_decorator(say_hi)
decorate()		# 'HELLO THERE'
```

Python also provides a much easier way for us to apply decorators.
We simply use the @ symbol before the function we would like to decorate.
``` python
def uppercase_decorator(function):
    def wrapper():
        func = function()
        make_uppercase = func.upper()
        return make_uppercase

    return wrapper

@uppercase_decorator
def say_hi():
    return 'hello there'

say_hi()		# 'HELLO THERE'
```

### Applying Multiple Decorators to a Single Function
We can use multiple decorators to a single function.
However, the decorators will be applied in the order that we've called them.

``` python
def uppercase_decorator(function):
    def wrapper():
        func = function()
        make_uppercase = func.upper()
        return make_uppercase

    return wrapper
    
def split_string(function):
    def wrapper():
        func = function()
        splitted_string = func.split()
        return splitted_string

    return wrapper
    
@split_string
@uppercase_decorator
def say_hi():
    return 'hello there'
say_hi()		# ['HELLO', 'THERE']
```

### Accepting Arguments in Decorator Functions
Sometimes we might need to define a decorator that accepts arguments.
We achieve this by passing the arguments to the wrapper function.
``` python
def decorator_with_arguments(function):
    def wrapper_accepting_arguments(arg1, arg2):
        print("My arguments are: {0}, {1}".format(arg1,arg2))
        function(arg1, arg2)
    return wrapper_accepting_arguments


@decorator_with_arguments
def cities(city_one, city_two):
    print("Cities I love are {0} and {1}".format(city_one, city_two))

cities("Sydney", "New York")

# My arguments are: Sydney, New York
# Cities I love are Sydney and New York
```

### Defining General Purpose Decorators
To define a general purpose decorator that can be applied to any function, we use *args and **kwargs.
*args and **kwargs collect all positional and keyword arguments and stores them in the args and kwargs variables.
*args and **kwargs can deal with a varyig number of arguments.

``` python
def a_decorator_passing_arbitrary_arguments(function_to_decorate):
    def a_wrapper_accepting_arbitrary_arguments(*args,**kwargs):
        print('The positional arguments are', args)
        print('The keyword arguments are', kwargs)
        function_to_decorate(*args)
    return a_wrapper_accepting_arbitrary_arguments

@a_decorator_passing_arbitrary_arguments
def function_with_no_argument():
    print("No arguments here.")

function_with_no_argument()

# The positional arguments are ()
# The keyword arguments are {}
# No arguments here.
```

use the decorator with positional arguments
``` python
@a_decorator_passing_arbitrary_arguments
def function_with_arguments(a, b, c):
    print(a, b, c)

function_with_arguments(1,2,3)

# The positional arguments are (1, 2, 3)
# The keyword arguments are {}
# 1 2 3
```

use the decorator with keyword arguments
``` python
@a_decorator_passing_arbitrary_arguments
def function_with_keyword_arguments():
    print("This has shown keyword arguments")

function_with_keyword_arguments(first_name="Derrick", last_name="Mwiti")

# The positional arguments are ()
# The keyword arguments are {'first_name': 'Derrick', 'last_name': 'Mwiti'}
# This has shown keyword arguments
```

### Passing Arguments to the Decorator
``` python
def decorator_maker_with_arguments(decorator_arg1, decorator_arg2, decorator_arg3):
    def decorator(func):
        def wrapper(function_arg1, function_arg2, function_arg3) :
            "This is the wrapper function"
            print("The wrapper can access all the variables\n"
                  "\t- from the decorator maker: {0} {1} {2}\n"
                  "\t- from the function call: {3} {4} {5}\n"
                  "and pass them to the decorated function"
                  .format(decorator_arg1, decorator_arg2,decorator_arg3,
                          function_arg1, function_arg2,function_arg3))
            return func(function_arg1, function_arg2,function_arg3)

        return wrapper

    return decorator

pandas = "Pandas"
@decorator_maker_with_arguments(pandas, "Numpy","Scikit-learn")
def decorated_function_with_arguments(function_arg1, function_arg2,function_arg3):
    print("This is the decorated function and it only knows about its arguments: {0}"
           " {1}" " {2}".format(function_arg1, function_arg2,function_arg3))

decorated_function_with_arguments(pandas, "Science", "Tools")

# The wrapper can access all the variables
#     - from the decorator maker: Pandas Numpy Scikit-learn
#     - from the function call: Pandas Science Tools
# and pass them to the decorated function
# This is the decorated function, and it only knows about its arguments: Pandas Science Tools
```

# Python Object Oriented Programming

## Basic OOP concepts
There are four fundamental concepts in object-oriented programming:
- Abstraction
- Encapsulation
- Inheritance
- Polymorphism

## Python Classes and Objects
Everything in Python is an object.
An object has states and behaviours.
To create an object, we have to define a class first.
Then, from the class, we can create one or more objects.
The objects are instances of a class.

### Define a class
To define a class, we use the `class` keyword followed by the class name.
``` python
class Person:
    pass
```

### Create an object
To create an object from the `Person` class, we use the class name followed by `()`.
``` python
person = Person()
```
In this example, the `person` is an instance of the `Person` class.

### Define instance attributes
Python is dynamic. It means that you can add an attribute to an instance of a class dynamically at runtime.
``` python
person.name = 'John'
```

To define and initialize an attribute for all instances of a class, we use the __init__ method.
``` python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```
The `person` object now has the `name` and `age` attributes.

To access an instance attribute, we use the dot(`.`) notation.
``` python
person.name
```

### \_\_init\_\_ method
Unlike regular method, the `__init()__` method has two underscores on each side.
Therefore, the method is often called dunder init.

The double underscores at both sides of the method indicate that Python will use the method internally.
In other words, we should not explicitly call this method.

When we create a `Person` object, Python automatically calls the `__init__` method to initialize the instance attributes.

In the `__init__` method, the `self` is the instance of the `Person` class.

``` python
person = Person('John', 25)
```

### Define instance methods
We can adds more methods in the class.
``` python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        return f"Hi, it's {self.name}."
```

To call an instance method, we use the dot(`.`) notation.
``` python
person = Person('John', 25)
print(person.greet())

# Hi, it's John
```

### Define class attributes
Unlike instance attributes, class attributes are shared by all instances of the class.
``` python
class Person:
    counter = 0

    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        return f"Hi, it's {self.name}."
```

We can access the `counter` attribute from the `Person` class:
``` python
Person.counter
```
or 
``` python
person = Person('John',25)
person.counter
```

We can also use the class attribute in class methods.
``` python
class Person:
    counter = 0

    def __init__(self, name, age):
        self.name = name
        self.age = age
        Person.counter += 1

    def greet(self):
        return f"Hi, it's {self.name}."
```

### Define class method
Like a class attribute, a class method is shared by all instances of the class.

The first argument of a class method is the clas itself.
By convention, its name is `cls`.

Use the `@classmethod` decorator to decorate a class method.
``` python
class Person:
    counter = 0

    def __init__(self, name, age):
        self.name = name
        self.age = age
        Person.counter += 1

    def greet(self):
        return f"Hi, it's {self.name}."

    @classmethod
    def create_anonymous(cls):
        return Person('Anonymous', 22)
```

Then call the `create_anonymous()` class method
``` python
anonymous = Person.create_anonymous()
print(anonymous.name)  # Anonymous
```

### Define a static method
A static method is not bound to a class or any instances of the class.

To define a static method, we use the `@staticmethod` decorator.
``` python
class TemperatureConverter:
    @staticmethod
    def celsius_to_fahrenheit(c):
        return 9 * c / 5 + 32

    @staticmethod
    def fahrenheit_to_celsius(f):
        return 5 * (f - 32) / 9
```

To call a static method, you use the ClassName.static_method_name() syntax.
``` python
f = TemperatureConverter.celsius_to_fahrenheit(30)
print(f)  # 86
```

### Private attributes
Private attributes can be only accessible from the methods of the class.
In other words, they cannot be accessible from outside of the class.

However, Python doesn't really have a concept of private attributes.
That is, all attributes are still accessible from the outside of a class.

By convension, we define a private attribute by prefixing a single underscore(`_`):
``` python
class Counter:
    def __init__(self):
        self._current = 0

    def increment(self):
        self._current += 1

    def value(self):
        return self._current

    def reset(self):
        self._current = 0
```

### Name magling with double underscores
Python will automatically change the name of the `__attribute` to `_class__attribute` which is called the name mangling in Python.

By doing this, we can't call __attribute outside of a class.
However, we still can call it with `_class__attribute`

### Magic methods
Called magic mehtods or dunder methods because they have double underscores on both sides of the method name.

#### `__str__()`
To make an object printable.
When we use the `print()` function to print out an instance of the `Person` class, Python calls the `__str__` method automatically.
``` python
class Person:
    def __init__(self, first_name, last_name, age):
        self.first_name = first_name
        self.last_name = last_name
        self.age = age

    def __str__(self):
        return f'Person({self.first_name},{self.last_name},{self.age})'
```
calls the mthod
``` python
person = Person('John', 'Doe', 25)
print(person)

# Person(John,Doe,25)
```

#### `__repr__()`
The `__repr__` dunder method defines behaviour when you pass an instance of a class to the `repr()`

The `__repr__` method returns the string representation of an object.
Typically, the `__repr__()` returns a string that can be executed and yield the same value as the object.

``` python
class Person:
    def __init__(self, first_name, last_name, age):
        self.first_name = first_name
        self.last_name = last_name
        self.age = age

    def __repr__(self):
        return f'Person("{self.first_name}","{self.last_name}",{self.age})'
```
calls the method
``` python
person = Person("John", "Doe", 25)
print(repr(person))

# Person("John","Doe",25)
```

#### `__bool__()`
The `__bool` method will return a boolean vlaue by the condition we have defined.

``` python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __bool__(self):
        if self.age < 18 or self.age > 65:
            return False
        return True

if __name__ == '__main__':
    person = Person('Jane', 16)
    print(bool(person))  # False
```

#### `__hash__`
The `hash()` function accepts an object and returns the hash value as an integer.

If a class overrides the `__eq__` method, the objects of the class become unhashable. This means that you won’t able to use the objects in a mapping type. For example, you will not able to use them as keys in a dictionary or elements in a set.

To make the `Person` class hashable, we needto implement the `__hash__` method
``` python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __eq__(self, other):
        return isinstance(other, Person) and self.age == other.age

    def __hash__(self):
        return hash(self.age)
```
Now, we have the `Person` class that supports equality based on `age` and is hashable.

## Python Property
### Getters and Setters
The getter and setter methods provide an interface for accessing an instance attribute:
- The getter returns the value of an attribute
- The setter sets a new value for an attribute

Getters and setters are used to protect your data, particularly when creating classes.

In the `set_age()` method
``` python
def set_age(self, age):
    if age <= 0:
        raise ValueError('The age must be positive')
    self._age = age
```

In the `get_age()` method
``` python
def get_age(self):
    return self._age
```
Then in `__init__()` method, we call the `set_age()` setter to initialize the `_age` attribute
``` python
def __init__(self, name, age):
    self.set_name(name)
    self.set_age(age)
```

### The Python propery class
The property class returns a `property` object.

The `property()` class has the following syntax:
``` python
property(fget=None, fset=None, fdel=None, doc=None)
```

The `property()` has the following parameters:
- `fget` - is a function to get the value of the attribute, or the getter method.
- `fset` - is a function to set the value of the attribute, or the setter method.
- 'fdel` - is a function to delete the attribute.
- 'doc` - is a docstring i.e., a comment.

The following uses the `property()` function to define the `age` property for the `Person` class.
``` python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def set_age(self, age):
        if age <= 0:
            raise ValueError('The age must be positive')
        self._age = age

    def get_age(self):
        return self._age

    # the age now is a class attribute, not an instance attribute
    age = property(fget=get_age, fset=set_age)
```

### Python Property Decorator
We can use decorators to create a property
``` python
class MyClass:
    def __init__(self, attr):
        self.prop = attr

    @property
    def prop(self):
        return self.__attr

    @prop.setter
    def prop(self, value):
        self.__attr = value
```

### Python read-only property
To define a readonly property, you need to create a property with only the getter. However, it is not truly read-only because you can always access the underlying attribute and change it.

The read-only properties are useful in some cases such as for computed properties.

``` python
import math

class Circle:
    def __init__(self, radius):
        self.radius = radius

    @property
    def area(self):
        return math.pi * self.radius ** 2

c = Circle(10)
print(c.area)
```

## Python inheritance
Inheritance allows a class to reuse the logic of an existing class.
The following is a single inheritance because the `Student` inherits from a single class `Person`.
``` python
# create a parent class
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)

#Use the Person class to create an object, and then execute the printname method:

x = Person("John", "Doe")
x.printname()               # John Doe

# create a child class
class Student(Person):
    def __init__(self, fname, lname, grade):
       super().__init__(fname, lname)
       self.grade = grade
       self.year = 2022

    def welcom(self):
        print("Welcome", self.firstname, self.lastname)

x = Student("Mike", "Jan", 95)
print(x.grade)              # 95
x.welcom()                  # Welcom Mike Jan
```

### Inheritance Terminology
The `Person` class is the parent class, the base class, or the super class of the `Student` class. And the `Student` class is a child class, a derived class, or a subclass of the `Person` class.

The `Student` class derives from, extends, or subclasses the `Person` class.

The relationship between the `Student` class and `Person` class is IS-A relationship. In other words, an employee is a person.

### isinstance
To check if an object is an instance of a class, we use the `isinstance()` method.
``` python
person = Person('Jane')
print(isinstance(person, Person))  # True

employee = Employee('John', 'Python Developer')
print(isinstance(employee, Person))  # True
print(isinstance(employee, Employee))  # True
print(isinstance(person, Employee))  # False
```

### issubclass
To check if a class is a subclass of another class, we use the `issubclass()` function.
``` python
print(issubclass(Student, Person)) # True
```

## Python Operator overloading
To overload the + operator, we will need to implement __add__() function in the class.
We can define our own operations, just like '+' can mean different operations for lists, numbers and strings.

``` python
class Point:
    def __init__(self, x=0, y=0):
        self.x = x
        self.y = y

    def __str__(self):
        return "({0},{1})".format(self.x, self.y)

    def __add__(self, other):
        x = self.x + other.x
        y = self.y + other.y
        return Point(x, y)

p1 = Point(1, 2)
p2 = Point(2, 3)

print(p1+p2)		# (3,5)
```

More operations that we can overload:
| Operator | Expression | Internally |
| ----------- | ----------- | ----------- |
| Addition | p1 + p2 | p1.__add__(p2)|
| Subtraction | p1 - p2 | p1.__sub__(p2) |
| Multiplication | p1 * p2 | p1.__mul__(p2) |
| Power | p1 ** p2 | p1.__pow__(p2) |
| Division | p1 / p2 | p1.__truediv__(p2) |
| Floor Division | p1 // p2 | p1.__floordiv__(p2) |
| Remainder (modulo) | p1 % p2 | p1.__mod__(p2) |
| Bitwise Left Shift | p1 << p2 | p1.__lshift__(p2) |
| Bitwise Right Shift | p1 >> p2 | p1.__rshift__(p2) |
| Bitwise AND | p1 & p2 | p1.__and__(p2) |
| Bitwise OR | p1 \| p2 | p1.__or__(p2) |
| Bitwise XOR | p1 ^ p2 | p1.__xor__(p2) |
| Bitwise NOT | ~p1 | p1.__invert__() |
| Less than | p1 < p2 | p1.__lt__(p2) |
| Less than or equal to | p1 <= p2 | p1.__le__(p2) |
| Equal to | p1 == p2 | p1.__eq__(p2) |
| Not equal to | p1 != p2 | p1.__ne__(p2) |
| Greater than | p1 > p2 | p1.__gt__(p2) |
| Greater than or equal to | p1 >= p2 | p1.__ge__(p2) |

# Python with Data Structure and Algorithms

## Python Linked lists
A linked list is a sequence of data elements, which are connected together via links. 
Each data element contains a connection to another data element in form of a pointer.

``` python
class Node:
    def __init__(self, dataval=None):
        self.dataval = dataval
        self.nextval = None

class SLinkedList:
    def __init__(self):
        self.headval = None
        self.size = 0

    def display(self):
        printval = self.headval
        while printval is not None:
            print (printval.dataval)
            printval = printval.nextval

    def prepend(self, val):
        newNode = Node(val)

        newNode.nextval = self.headval
        self.headval = newNode
        self.size += 1

    def append(self, val):
        newNode = Node(val)
        if self.headval == None:
            self.headval = newNode
        else:
            last = self.headval
            while last.nextval:
                last = last.nextval

            last.nextval = newNode

        self.size += 1

    def insert(self, val, idx):
        if idx >= self.size:
            print("Out of bound")
        
        newNode = Node(val)

        if idx == 0:
            self.prepend(val)
        else:
            p = self.headval
            i = 1
            while i < idx:
                p = p.nextval
                i += 1

            newNode.nextval = p.nextval
            p.nextval = newNode

    def search(self, val):
        p = self.headval
        while p:
            if p.dataval == val:
                return True
            
            p = p.nextval
        
        return False

    def delete(self, idx):
        if self.headval == None:
            print("No elements")

        temp = self.headval

        if idx == 0:
            self.headval = temp.nextval
            temp = None
            return

        for i in range(idx - 1):
            temp = temp.nextval
            if temp == None:
                break

        if temp == None:
            return

        if temp.nextval == None:
            return

        next = temp.nextval.nextval

        temp.nextval = None

        temp.nextval = next

    

list = SLinkedList()
list.prepend("Mon")
list.prepend("Tue")
list.prepend("Fri")
list.append("Sun")
list.append("Thu")
list.insert("Wed", 2)

list.display()                  # Fri Tue Wed Mon Sun Thu
print(list.search("Sun"))       # True
print(list.search("sun"))       # False

list.delete(2)
list.display()                  # Fri Tue Mon Sun Thu
```

## Python Stack
Stack stores the data elements in a similar fashion as a bunch of plates are stored one above another in the kitchen. 
So stack data strcuture allows operations at one end wich can be called top of the stack.
We can add elements or remove elements only form this end of the stack.
Stack is Last in First out.

For the array-based implementation of a stack, the push and pop operations take constant time O(1).

``` python
class Stack:
    def __init__(self) -> None:
        self.stack = []

    def push(self, val) -> None:
        self.stack.append(val)

    def pop(self):
        if len(self.stack) <= 0:
            return "No element in the Stack"
        else:
            return self.stack.pop()

    def isEmpty(self):
        if self.stack == []:
            return True
        else:
            return False
    
    def peek(self):
        if len(self.stack) <= 0:
            return "No element in the Stack"
        else:
            return self.stack[-1] 

s = Stack()
s.push(5)
s.push(3)
print(s.pop())          # 3
print(s.peek())         # 5
print(s.pop())          # 5
print(s.isEmpty())      # True
```

## Python Queue

### Simple Queue
The uniqueness of queue lies in the way items are added and removed. 
The items are allowed at on end but removed form the other end. 
So it is a First-in-First out method.

The complexity of enqueue and dequeue operations in a queue using an array is O(1).
In Python, pop(N) might have complexity of O(n) depending on the position of the item to be popped.

``` python
class Queue:
    def __init__(self) -> None:
        self.queue = []

    def enqueue(self, val):
        self.queue.insert(0, val)

    def dequeue(self):
        if len(self.queue) <= 0:
            return "No element in the Queue"
        else:
            return self.queue.pop()

    def display(self):
        print(self.queue)
    
    def size(self):
        return len(self.queue)

q = Queue()
q.enqueue(1)
q.enqueue(2)
q.enqueue(3)
q.enqueue(4)
q.enqueue(5)
q.display()         # [5, 4, 3, 2, 1]

q.dequeue()
print("After removing an element")
q.display()         # [5, 4, 3, 2]
```

### Circular Queue
A circular queue is the extended version of a regular queue where the last element is connected to the first element.
Circular Queue works by the process of circular increment i.e. when we try to increment the pointer and we reach the end of the queue, we start from the beginning of the queue.

The complexity of the enqueue and dequeue operations of a circular queue is O(1) for (array implementations).

``` python
class MyCircularQueue:
    def __init__(self, length) -> None:
        self.length = length
        self.queue = [None] * length
        self.head = self.tail = -1

    def enqueue(self, val):
        if ((self.tail + 1) % self.length == self.head):
            print("The circular queue is full")
        elif (self.head == -1):
            self.head = 0
            self.tail = 0
            self.queue[self.tail] = val
        else:
            self.tail = (self.tail + 1) % self.length
            self.queue[self.tail] = val

    def dequeue(self):
        if (self.head == -1):
            print("The circular queue is empty")
        elif (self.head == self.tail):
            temp = self.queue[self.head]
            self.head = -1
            self.tail = -1
            return temp
        else:
            temp = self.queue[self.head]
            self.head = (self.head + 1) % self.length
            return temp

    def printQueue(self):
        if (self.head == -1):
            print("No element in the circular queue")
        elif (self.tail >= self.head):
            for i in range(self.head, self.tail + 1):
                print(self.queue[i], end=" ")
            print()
        else:
            for i in range(self.head, self.length):
                print(self.queue[i], end=" ")
            for i in range(0, self.tail + 1):
                print(self.queue[i], end=" ")
            print()

obj = MyCircularQueue(5)
obj.enqueue(1)
obj.enqueue(2)
obj.enqueue(3)
obj.enqueue(4)
obj.enqueue(5)
print("Initial queue")
obj.printQueue()            # 1 2 3 4 5 

obj.dequeue()
print("After removing an element from the queue")
obj.printQueue()            # 2 3 4 5
```

### Priority Queue
A priority queue is a type of queue in which each element is associated with a priority value.
Higher priority elements are served first.

By using the heap, the time complexity of inserting and deleting are O(log n)

``` python
# Priority Queue implementation in Python
class MyPriorityQueue:
    def __init__(self) -> None:
        self.arr = []

    def heapify(self, n, i):
        # find the largest among root, left child and right child
        largest = i
        l = 2 * i + 1
        r = 2 * i + 2

        if l < n and self.arr[i] < self.arr[l]:
            largest = 1

        if r < n and self.arr[largest] < self.arr[r]:
            largest = r

        # Swap and continue heapifying if root is not largest
        if largest != i:
            self.arr[i], self.arr[largest] = self.arr[largest], self.arr[i]
            self.heapify(n, largest)

    # Function to insert an element into the tree
    def insert(self, newNum):
        size = len(self.arr)
        if size == 0:
            self.arr.append(newNum)
        else:
            self.arr.append(newNum)
            for i in range((size // 2) - 1, -1, -1):
                self.heapify(size, i)

    # Function to delete an element from the tree
    def deleteNode(self, num):
        size = len(self.arr)
        i = 0
        for i in range(0, size):
            if num == self.arr[i]:
                break

        self.arr[i], self.arr[size - 1] = self.arr[size - 1], self.arr[i]

        self.arr.remove(size - 1)

        for i in range((len(self.arr) // 2) - 1, -1, -1):
            self.heapify(len(self.arr), i)

myPriorityQueue = MyPriorityQueue()
myPriorityQueue.insert(3)
myPriorityQueue.insert(4)
myPriorityQueue.insert(9)
myPriorityQueue.insert(5)
myPriorityQueue.insert(2)

# [9, 3, 4, 5, 2]
print("Max-Heap array: " + str(myPriorityQueue.arr))
myPriorityQueue.deleteNode(4)
# [9, 3, 2, 5]
print("After deleting an element: ", str(myPriorityQueue.arr))
```

### Double Ended Queue (Dequeue)
Deque or Double Ended Queue is a type of queue in which insertion and removal of elements can either be performed from the front or the rear. 
Thus, it does not follow FIFO rule (First In First Out).

``` python
# Deque implementaion in python

class Deque:
    def __init__(self):
        self.items = []

    def isEmpty(self):
        return self.items == []

    def addRear(self, item):
        self.items.append(item)

    def addFront(self, item):
        self.items.insert(0, item)

    def removeFront(self):
        return self.items.pop(0)

    def removeRear(self):
        return self.items.pop()

    def size(self):
        return len(self.items)

d = Deque()
print(d.isEmpty())          # True
d.addRear(8)
d.addRear(5)
d.addFront(7)
d.addFront(10)
print(d.size())             # 4
print(d.isEmpty())          # False
d.addRear(11)
print(d.removeRear())       # 11
print(d.removeFront())      # 10
d.addFront(55)
d.addRear(45)
print(d.items)              # [55, 7, 8, 5, 45]
```

## Python Trees

### Tree Terminologies

#### Node
A node is an entity that contains a key or value and pointers to its child nodes.

The last nodes of each path are called lead nodes or external nodes that do not contain a link to child nodes.

The node having at least a child node is called an internal node.

#### Edge
It is the link between any two nodes.

#### Root
It is the topmost node of a tree.

#### Height of a Node
The height of a node is the number of edges from the node to the deepest leaf.

#### Depth of a Node
The depth of a node is the number of edges from the root to the node.

#### Height of a Tree
The max path length form root to leaf.

#### Degree of a Node
The degree of a node is the total number of branches of that node.

#### Forest
A collection of disjoint trees is called a forest.

### Binary Tree

#### Full Binary Tree
A full Binary tree is a special type of binary tree in which every parent node/internal node has either two or no children.

Let, i = the number of internal nodes (nodes that are not leaves), n = the total number of nodes, l = the number of leaves and lambda = the number of levels.
1. The number of leaves is i + 1
2. The total number of nodes is 2*i + 1
3. The number of internal nodes is (n – 1) / 2
4. The number of leaves is (n + 1) / 2
5. The total number of nodes is 2l – 1
6. The number of internal nodes is l – 1
7. The number of leaves is at most 2 ^ (lambda - 1)

``` python
# Checking if a binary tree is a full binary tree in Python

# Creating a node
class Node:

    def __init__(self, item):
        self.item = item
        self.leftChild = None
        self.rightChild = None


# Checking full binary tree
def isFullTree(root):

    # Tree empty case
    if root is None:
        return True

    # Checking whether child is present
    if root.leftChild is None and root.rightChild is None:
        return True

    if root.leftChild is not None and root.rightChild is not None:
        return (isFullTree(root.leftChild) and isFullTree(root.rightChild))

    return False

root = Node(1)
root.rightChild = Node(3)
root.leftChild = Node(2)

root.leftChild.leftChild = Node(4)
root.leftChild.rightChild = Node(5)
root.leftChild.rightChild.leftChild = Node(6)
root.leftChild.rightChild.rightChild = Node(7)

if isFullTree(root):
    print("The tree is a full binary tree")
else:
    print("The tree is not a full binary tree")
```

#### Perfect Binary Tree
A perfect binary tree is a type of binary tree in which every internal node has exactly two child nodes and all the leaf nodes are at the same level.

``` python
# Checking if a binary tree is a perfect binary tree in Python

class newNode:
    def __init__(self, k):
        self.key = k
        self.right = self.left = None

# Calculate the depth
def calculateDepth(node):
    d = 0
    while (node is not None):
        d += 1
        node = node.left
    return d

# Check if the tree is perfect binary tree
def is_perfect(root, d, level=0):

    # Check if the tree is empty
    if (root is None):
        return True

    # Check the presence of trees
    if (root.left is None and root.right is None):
        return (d == level + 1)

    if (root.left is None or root.right is None):
        return False

    return (is_perfect(root.left, d, level + 1) and
            is_perfect(root.right, d, level + 1))

root = None
root = newNode(1)
root.left = newNode(2)
root.right = newNode(3)
root.left.left = newNode(4)
root.left.right = newNode(5)

if (is_perfect(root, calculateDepth(root))):
    print("The tree is a perfect binary tree")
else:
    print("The tree is not a perfect binary tree")
```

#### Complete Binary Tree
A complete binary tree is just like a full binary tree, but with two major differences
1. Every level must be completely filled
2. All the leaf elements must lean towards the left.
3. The last leaf element might not have a right sibling i.e. a complete binary tree doesn't have to be a full binary tree.

``` python
# Checking if a binary tree is a complete binary tree in C

class Node:

    def __init__(self, item):
        self.item = item
        self.left = None
        self.right = None

# Count the number of nodes
def count_nodes(root):
    if root is None:
        return 0
    return (1 + count_nodes(root.left) + count_nodes(root.right))

# Check if the tree is complete binary tree
def is_complete(root, index, numberNodes):

    # Check if the tree is empty
    if root is None:
        return True

    if index >= numberNodes:
        return False

    return (is_complete(root.left, 2 * index + 1, numberNodes)
            and is_complete(root.right, 2 * index + 2, numberNodes))

root = Node(1)
root.left = Node(2)
root.right = Node(3)
root.left.left = Node(4)
root.left.right = Node(5)
root.right.left = Node(6)

node_count = count_nodes(root)
index = 0

if is_complete(root, index, node_count):
    print("The tree is a complete binary tree")
else:
    print("The tree is not a complete binary tree")
```

#### Degenerate or Pathological Tree
A degenerate or pathological tree is the tree having a single child either left or right.

#### Skewed Binary Tree
A skewed binary tree is a pathological tree in which the tree is either dominated by the left nodes or the right nodes.
Thus, there are two types of skewed binary tree: left-skewed binary tree and right-skewed binary tree.

#### Balanced Binary Tree
The balanced binary tree, also known as the height-balanced binary tree, is defined as the binary tree in which the height of the left and right subtree of any node differ by not more than 1.

Three conditions for a height-balanced binary tree:
- difference between the left and the right subtree for any node is not more than one
- the left subtree is balanced
- the right subtree is balanced

``` python
# Checking if a binary tree is height balanced in Python

class Node:

    def __init__(self, data):
        self.data = data
        self.left = self.right = None

class Height:
    def __init__(self):
        self.height = 0

def isHeightBalanced(root, height):

    left_height = Height()
    right_height = Height()

    if root is None:
        return True

    l = isHeightBalanced(root.left, left_height)
    r = isHeightBalanced(root.right, right_height)

    height.height = max(left_height.height, right_height.height) + 1

    if abs(left_height.height - right_height.height) <= 1:
        return l and r

    return False

height = Height()

root = Node(1)
root.left = Node(2)
root.right = Node(3)
root.left.left = Node(4)
root.left.right = Node(5)

# the tree is balanced
if isHeightBalanced(root, height):
    print('The tree is balanced')
else:
    print('The tree is not balanced')
```

### Binary Search Tree
The properties that separate a binary search tree from a regular binary tree is:
1. All nodes of left subtree are less than the root node
2. All nodes of right subtree are more than the root node
3. Both subtrees of each node are also BSTs, that is, they have the above two properties

Time complexity in worst case
- Search - O(n)
- Insertion - O(n)
- Deletion - O(n)

Space Complexity:
- The space complexity for all the operations is O(n)

``` python
# Binary Search Tree operations in Python

# Create a node
class Node:
    def __init__(self, key):
        self.key = key
        self.left = None
        self.right = None

# Inorder traversal
def inorder(root):
    if root is not None:
        # Traverse left
        inorder(root.left)

        # Traverse root
        print(str(root.key) + "->", end=' ')

        # Traverse right
        inorder(root.right)

# Insert a node
def insert(node, key):

    # Return a new node if the tree is empty
    if node is None:
        return Node(key)

    # Traverse to the right place and insert the node
    if key < node.key:
        node.left = insert(node.left, key)
    else:
        node.right = insert(node.right, key)

    return node

# Find the inorder successor
def minValueNode(node):
    current = node

    # Find the leftmost leaf
    while(current.left is not None):
        current = current.left

    return current

# Deleting a node
def deleteNode(root, key):
    # four cases to consider
    # empty tree - new tree is also empty
    # zero subtrees - unlink node from parent
    # one subtree - replace by child
    # two subtrees - replace by successor, join two subtrees

    # Return if the tree is empty
    if root is None:
        return root

    # Find the node to be deleted
    if key < root.key:
        root.left = deleteNode(root.left, key)
    elif(key > root.key):
        root.right = deleteNode(root.right, key)
    else:
        # If the node is with only one child or no child
        if root.left is None:
            temp = root.right
            root = None
            return temp

        elif root.right is None:
            temp = root.left
            root = None
            return temp

        # If the node has two children,
        # place the inorder successor in position of the node to be deleted
        # this is also known as joining two trees
        temp = minValueNode(root.right)

        root.key = temp.key

        # Delete the inorder successor
        root.right = deleteNode(root.right, temp.key)

    return root

root = None
root = insert(root, 8)
root = insert(root, 3)
root = insert(root, 1)
root = insert(root, 6)
root = insert(root, 7)
root = insert(root, 10)
root = insert(root, 14)
root = insert(root, 4)

print("Inorder traversal: ", end=' ')
inorder(root)

print("\nDelete 10")
root = deleteNode(root, 10)
print("Inorder traversal: ", end=' ')
inorder(root)
```

### AVL Tree
AVL tree is a self-balancing binary search tree in which each node maintins extra information called a balance factor whose value is either -1, 0 or 1. AVL always remains balanced even after inserting, deleting and searching. AVL tree got its name after its inventor Georgy Adelson-Velsky and Landis.

Balance factor of a node in an AVL tree is the difference between the height of the left subtree and that of the right subtree of that node. 

Balance Factor = (Height of Left Subtree - Height of Right Subtree) or (Height of Right Subtree - Height of Left Subtree)

The time complexities of insertion, delettion and search in an AVL tree are O(log n).

When ensuring the tree remain balanced while inserting a node, we introduced right rotation and left rotation. (due to the limitaion of markdown file and my drawing, please search online)

``` python
# AVL tree implementation in Python

import sys

# Create a tree node
class TreeNode(object):
    def __init__(self, key):
        self.key = key
        self.left = None
        self.right = None
        self.height = 1

class AVLTree(object):

    # Function to insert a node
    def insert_node(self, root, key):

        # Find the correct location and insert the node
        if not root:
            return TreeNode(key)
        elif key < root.key:
            root.left = self.insert_node(root.left, key)
        else:
            root.right = self.insert_node(root.right, key)

        root.height = 1 + max(self.getHeight(root.left),
                              self.getHeight(root.right))

        # Update the balance factor and balance the tree
        balanceFactor = self.getBalance(root)
        if balanceFactor > 1:
            if key < root.left.key:
                return self.rightRotate(root)
            else:
                root.left = self.leftRotate(root.left)
                return self.rightRotate(root)

        if balanceFactor < -1:
            if key > root.right.key:
                return self.leftRotate(root)
            else:
                root.right = self.rightRotate(root.right)
                return self.leftRotate(root)

        return root

    # Function to delete a node
    def delete_node(self, root, key):

        # Find the node to be deleted and remove it
        if not root:
            return root
        elif key < root.key:
            root.left = self.delete_node(root.left, key)
        elif key > root.key:
            root.right = self.delete_node(root.right, key)
        else:
            if root.left is None:
                temp = root.right
                root = None
                return temp
            elif root.right is None:
                temp = root.left
                root = None
                return temp
            temp = self.getMinValueNode(root.right)
            root.key = temp.key
            root.right = self.delete_node(root.right,
                                          temp.key)
        if root is None:
            return root

        # Update the balance factor of nodes
        root.height = 1 + max(self.getHeight(root.left),
                              self.getHeight(root.right))

        balanceFactor = self.getBalance(root)

        # Balance the tree
        if balanceFactor > 1:
            if self.getBalance(root.left) >= 0:
                return self.rightRotate(root)
            else:
                root.left = self.leftRotate(root.left)
                return self.rightRotate(root)
        if balanceFactor < -1:
            if self.getBalance(root.right) <= 0:
                return self.leftRotate(root)
            else:
                root.right = self.rightRotate(root.right)
                return self.leftRotate(root)
        return root

    # Function to perform left rotation
    def leftRotate(self, z):
        y = z.right
        T2 = y.left
        y.left = z
        z.right = T2
        z.height = 1 + max(self.getHeight(z.left),
                           self.getHeight(z.right))
        y.height = 1 + max(self.getHeight(y.left),
                           self.getHeight(y.right))
        return y

    # Function to perform right rotation
    def rightRotate(self, z):
        y = z.left
        T3 = y.right
        y.right = z
        z.left = T3
        z.height = 1 + max(self.getHeight(z.left),
                           self.getHeight(z.right))
        y.height = 1 + max(self.getHeight(y.left),
                           self.getHeight(y.right))
        return y

    # Get the height of the node
    def getHeight(self, root):
        if not root:
            return 0
        return root.height

    # Get balance factore of the node
    def getBalance(self, root):
        if not root:
            return 0
        return self.getHeight(root.left) - self.getHeight(root.right)

    def getMinValueNode(self, root):
        if root is None or root.left is None:
            return root
        return self.getMinValueNode(root.left)

    def preOrder(self, root):
        if not root:
            return
        print("{0} ".format(root.key), end="")
        self.preOrder(root.left)
        self.preOrder(root.right)

myTree = AVLTree()
root = None
nums = [33, 13, 52, 9, 21, 61, 8, 11]
for num in nums:
    root = myTree.insert_node(root, num)
key = 13
myTree.preOrder(root)       # 33 13 9 8 11 21 52 61
print()
root = myTree.delete_node(root, key)
print("After Deletion: ")
myTree.preOrder(root)       # 33 9 8 21 11 52 61 
print()
```

### B-Tree
B-Tree is a special type of self-balancing search tree in which each node can contain more than one key and cna have more than two children.
It is a generalized form of the binary search tree.
It is also known as a height-balanced m-way tree.

#### Why do we need a B-tree data strcuture
The need for B-tree arose with the rise in the need for lesser time in accessing the physical storage media like a hard disk.
The secondary storage devices are slower with a larger capacity.
There was a need for such types of data structures that minimize the disk accesses.

Other data structures such as a binary search tree, AVL tree, red-black tree, etc can store only one key in one node.
If we have to store a large number of keys, then the height of such trees becomes very large and the access tie increases.

However, B-tree can store many keys in a single node and can have multiple child nodes.
This decreases the height significantly allowing faster disk accesses.

The specific form of B-tree is 2-3-4 Tree.

#### B-tree properties
1. For each noe x, the keys are stored in increasing order.
2. In each node, there is a boolean value x.leaf which is true if x is a leaf.
3. If n is the order of the tree, each internal node can contain at most n - 1 keys along wich a pointer to each child.
4. Each node except root can have at most n children and at least n/2 children.
5. All leaves have the same depth
6. THe root has at least 2 children and contains a minimum of 1 key.
7. If n >= 1, then for any n-key B-tree of height h and mimimum degree t >= 2, h >= log t (n+1)/2

#### B-tree operations time complexity
- Time complexity for searching is O(log n) in best, average and worst cases
- Space complexity for searching is O(n) in average and worst cases
- Time complexity for deleting is O(log n) in best case
- Space complexity for deleting is O(n)

#### Code Example
``` python

```

## Python Heaps
Heap is a special tree structure in which each parent node is less than or equal to its child node. Then it is called a Min Heap. If each parent node is greater than or equal to its child node then it is called a max heap.

``` python
# Max-Heap data strucute in Python

def heapify(arr, size, i):
    largest = i
    
    # l is the left child
    l = 2 * i + 1
    # r is the right child
    r = 2 * i + 2

    if l < size and arr[i] < arr[l]:
        largest = l
    
    if r < size and arr[largest] < arr[r]:
        largest = r

    if largest != i:
        arr[i], arr[largest] = arr[largest], arr[i]
        heapify(arr, size, largest)

def insert(arr, num):
    size = len(arr)
    if size == 0:
        arr.append(num)
    else:
        arr.append(num)
        for i in range((size//2)-1, -1, -1):
            heapify(arr, size, i)

def delete(arr, num):
    size = len(arr)
    i = 0
    for i in range(size):
        if num == arr[i]:
            break
    
    arr[i], arr[size-1] = arr[size-1], arr[i]

    arr.remove(num)

    for i in range((len(arr)//2)-1, -1, -1):
        heapify(arr, len(arr), i)

arr = []

insert(arr, 3)
insert(arr, 4)
insert(arr, 9)
insert(arr, 5)
insert(arr, 2)

print(arr)      # [9, 5, 4, 3, 2]

delete(arr, 4)

print(arr)      # [9, 5, 2, 3]
```

## Python Tries
Trie is a tree-like data structure made up of nodes.
Nodes can be used to store data.
Each node may have none, one or more children.

A trie is a data strucute for representing a set of strings.
It supports string matching queries in O(L) time where L is the length of the string being searched for

Each node in a trie:
- contains one part of a key (typically one character)
- may have up to 26 children
- may be tagged as a finishing node
- but even finishing nodes may have children
- may contain other data for application

``` python
from typing import Tuple

class TrieNode(object):
    """
    Our trie node implementation. Very basic. but does the job
    """
    
    def __init__(self, char: str):
        self.char = char
        self.children = []
        # Is it the last character of the word.`
        self.word_finished = False
        # How many times this character appeared in the addition process
        self.counter = 1
    

def add(root, word: str):
    """
    Adding a word in the trie structure
    """
    node = root
    for char in word:
        found_in_child = False
        # Search for the character in the children of the present `node`
        for child in node.children:
            if child.char == char:
                # We found it, increase the counter by 1 to keep track that another
                # word has it as well
                child.counter += 1
                # And point the node to the child that contains this char
                node = child
                found_in_child = True
                break
        # We did not find it so add a new chlid
        if not found_in_child:
            new_node = TrieNode(char)
            node.children.append(new_node)
            # And then point node to the new child
            node = new_node
    # Everything finished. Mark it as the end of a word.
    node.word_finished = True


def find_prefix(root, prefix: str) -> Tuple[bool, int]:
    """
    Check and return 
      1. If the prefix exsists in any of the words we added so far
      2. If yes then how may words actually have the prefix
    """
    node = root
    # If the root node has no children, then return False.
    # Because it means we are trying to search in an empty trie
    if not root.children:
        return False, 0
    for char in prefix:
        char_not_found = True
        # Search through all the children of the present `node`
        for child in node.children:
            if child.char == char:
                # We found the char existing in the child.
                char_not_found = False
                # Assign node as the child containing the char and break
                node = child
                break
        # Return False anyway when we did not find a char.
        if char_not_found:
            return False, 0
    # Well, we are here means we have found the prefix. Return true to indicate that
    # And also the counter of the last node. This indicates how many words have this
    # prefix
    return True, node.counter

if __name__ == "__main__":
    root = TrieNode('*')
    add(root, "hackathon")
    add(root, 'hack')

    print(find_prefix(root, 'hac'))         # (True, 2)
    print(find_prefix(root, 'hack'))        # (True, 2)
    print(find_prefix(root, 'hackathon'))   # (True, 1)
    print(find_prefix(root, 'ha'))          # (True, 2)
    print(find_prefix(root, 'hammer'))      # (False, 0)
```

## Python Graphs
A graph data structure is a collection of nodes that have data and are connected to other nodes.

More precisely, a graph is a data structure (V, E) that consists of
- a collection of vertices V
- a collection of edges E, represented as ordered pairs of vertices (u, v)

### Graph Terminology
- Adjacency: A vertex is said to be adjacent to another vertex if there is an edge connecting them. Vertices 2 and 3 are not adjacent because there is no edge between them.
- Path: A sequence of edges that allows you to go from vertex A to vertex B is called a path. 0-1, 1-2 and 0-2 are paths from vertex 0 to vertex 2.
- Directed Graph: A graph in which an edge (u,v) doesn't necessarily mean that there is an edge (v, u) as well. The edges in such a graph are represented by arrows to show the direction of the edge.

### Graph representation
There are several ways that we could represent graph:
1. Adjacency Matrix
An adjacency matrix is a 2D array of V x V vertices. Each row and column represent a vertex.
If the value of any element a[i][j] is 1, it represents that there is an edge connecting vertex i and vertex j.
2. Adjacency List
An adjacency list represents a graph as an array of linked lists.
The index of the array represents a vertex and each element in its linked list represents the other vertices that form an edge with the vertex.
An adjacency list is efficient in terms of storage because we only need to store the values for the edges. For a graph with millions of vertices, this can mean a lot of saved space.

### Spanning Tree and Minimum Spanning Tree

#### Undirected graph
An undirected graph is a graph in which the edges do not point in any direction (ie. the edges are bidirectional).

#### Connected graph
A connected graph is a graph in which there is always a path from a vertex to any other vertex.

#### Spanning tree
A spanning tree is a sub-graph of an undirected connected graph, which includes all the vertices of the graph with a minimum possible number of edges. 
If a vertex is missed, then it is not a spanning tree.

#### Minimum Spanning Tree
A minimum spanning tree is a spanning tree in which the sum of the weight of the edges is as minimum as possible.

### Minimum Spanning Tree Algorithms

#### Prim's Algorithm
Prim's algorithm is a minimum spanning tree algorithm that takes a graph as input and finds the subset of the edges of that graph which
- form a tree that includes every vertex
- has the minimum sum of weights among all the trees that can be formed from the graph

#### How Prim's algorithm works
It falls under a class of algorithms called greedy algorithms that find the local optimum in the hopes of finding a global optimum.

We start from one vertex and keep adding edges with the lowest weight until we reach our goal.

The steps for implementing Prim's algorithm are as follows:
1. Initialize the minimum spanning tree with a vertex chosen at random.
2. Find all the edges that connect the tree to new vertices, find the minimum and add it to the tree
3. Keep repeating step 2 until we get a minimum spanning tree

The time complexity of Prim's Algorithm is O(E log V).

``` python
# Prim's Algorithm in Python

INF = 9999999
# number of vertices in graph
V = 5
# create a 2d array of size 5x5
# for adjacency matrix to represent graph
G = [[0, 9, 75, 0, 0],
     [9, 0, 95, 19, 42],
     [75, 95, 0, 51, 66],
     [0, 19, 51, 0, 31],
     [0, 42, 66, 31, 0]]
# create a array to track selected vertex
# selected will become true otherwise false
selected = [0, 0, 0, 0, 0]
# set number of edge to 0
no_edge = 0
# the number of egde in minimum spanning tree will be
# always less than(V - 1), where V is number of vertices in
# graph
# choose 0th vertex and make it true
selected[0] = True
# print for edge and weight
print("Edge : Weight\n")
while (no_edge < V - 1):
    # For every vertex in the set S, find the all adjacent vertices
    #, calculate the distance from the vertex selected at step 1.
    # if the vertex is already in the set S, discard it otherwise
    # choose another vertex nearest to selected vertex  at step 1.
    minimum = INF
    x = 0
    y = 0
    for i in range(V):
        if selected[i]:
            for j in range(V):
                if ((not selected[j]) and G[i][j]):  
                    # not in selected and there is an edge
                    if minimum > G[i][j]:
                        minimum = G[i][j]
                        x = i
                        y = j
    print(str(x) + "-" + str(y) + ":" + str(G[x][y]))
    selected[y] = True
    no_edge += 1
```

#### Kruskal's Algorithm
Kruskal's algorithm is a minimum spanning tree algorithm that takes a graph as input and finds the subset of the edges of that graph which
- form a tree that includes every vertex
- has the minimum sum of weights among all the trees that can be formed from the graph

#### How Kruskal's algorithm works
It falls under a class of algorithms called greedy algorithms that find the local optimum in the hopes of finding a global optimum.

We start from the edges with the lowest weight and keep adding edges until we reach our goal.

The steps for implementing Kruskal's algorithm are as follows:
1. Sort all the edges from low weight to high
2. Take the edge with the lowest weight and add it to the spanning tree. If adding the edge created a cycle, then reject this edge.
3. Keep adding edges until we reach all vertices.

The time complexity of Kruskal's Algorithm is O(E log E).

``` python
# Kruskal's algorithm in Python

class Graph:
    def __init__(self, vertices):
        self.V = vertices
        self.graph = []

    def add_edge(self, u, v, w):
        self.graph.append([u, v, w])

    # Search function

    def find(self, parent, i):
        if parent[i] == i:
            return i
        return self.find(parent, parent[i])

    def apply_union(self, parent, rank, x, y):
        xroot = self.find(parent, x)
        yroot = self.find(parent, y)
        if rank[xroot] < rank[yroot]:
            parent[xroot] = yroot
        elif rank[xroot] > rank[yroot]:
            parent[yroot] = xroot
        else:
            parent[yroot] = xroot
            rank[xroot] += 1

    #  Applying Kruskal algorithm
    def kruskal_algo(self):
        result = []
        i, e = 0, 0
        self.graph = sorted(self.graph, key=lambda item: item[2])
        parent = []
        rank = []
        for node in range(self.V):
            parent.append(node)
            rank.append(0)
        while e < self.V - 1:
            u, v, w = self.graph[i]
            i = i + 1
            x = self.find(parent, u)
            y = self.find(parent, v)
            if x != y:
                e = e + 1
                result.append([u, v, w])
                self.apply_union(parent, rank, x, y)
        for u, v, weight in result:
            print("%d - %d: %d" % (u, v, weight))


g = Graph(6)
g.add_edge(0, 1, 4)
g.add_edge(0, 2, 4)
g.add_edge(1, 2, 2)
g.add_edge(1, 0, 4)
g.add_edge(2, 0, 4)
g.add_edge(2, 1, 2)
g.add_edge(2, 3, 3)
g.add_edge(2, 5, 2)
g.add_edge(2, 4, 4)
g.add_edge(3, 2, 3)
g.add_edge(3, 4, 3)
g.add_edge(4, 2, 4)
g.add_edge(4, 3, 3)
g.add_edge(5, 2, 2)
g.add_edge(5, 4, 3)
g.kruskal_algo()
```

## Time complexities of different data structures in worst case
| Data structure | Access | Search | Insertion | Deletion
| -------------- | ------ | ------ | --------- | --------
| Array | O(1) | O(N) | O(N) | O(N)
| Stack | O(N) | O(N) | O(1) | O(1)
| Queue | O(N)| O(N) | O(1) | O(1)
| Singly Linked list | O(N) | O(N) | O(1) | O(1)
| Doubly Linked List | O(N) | O(N) | O(1) | O(1)
| Hash Table | O(N) | O(N) | O(N) | O(N)
| Binary Search Tree | O(N) | O(N) | O(N) | O(N)
| AVL Tree | O(log N) | O(log N) | O(log N) | O(log N)
| Binary Tree | O(N) | O(N) | O(N) | O(N)
| Red Black Tree | O(log N) | O(log N) | O(log N) | O(log N)

## Python Searching Algorithms

### Linear Search
Linear search is a sequential searching algorithm where we start from one end and every element of the list until the desired element is found.

The time complexity of linear search is O(n).

``` python
# Linear Search in Python

def linearSearch(array, n, x):

    # Going through array sequencially
    for i in range(n):
        if (array[i] == x):
            return i
    return -1


array = [2, 4, 0, 1, 9]
x = 1
n = len(array)
result = linearSearch(array, n, x)
if(result == -1):
    print("Element not found")
else:
    print("Element found at index: ", result)
```

### Binary Search
Binary Search is a searching algorithm for finding an element's position in a sorted array.

In this approach, the element is always searched in the middle of a portion of an array.

The time complexity of binary search in worst case is O(log n).
The space complexity of binary search is always O(1).

Do binary search iteratively:
``` python
# Binary Search in python

def binarySearch(array, x, low, high):

    # Repeat until the pointers low and high meet each other
    while low <= high:

        mid = low + (high - low)//2

        if array[mid] == x:
            return mid

        elif array[mid] < x:
            low = mid + 1

        else:
            high = mid - 1

    return -1

array = [3, 4, 5, 6, 7, 8, 9]
x = 4

result = binarySearch(array, x, 0, len(array)-1)

if result != -1:
    print("Element is present at index " + str(result))
else:
    print("Not found")
```

Do binary search recursively:
``` python
# Binary Search in python

def binarySearch(array, x, low, high):

    if high >= low:

        mid = low + (high - low)//2

        # If found at mid, then return it
        if array[mid] == x:
            return mid

        # Search the left half
        elif array[mid] > x:
            return binarySearch(array, x, low, mid-1)

        # Search the right half
        else:
            return binarySearch(array, x, mid + 1, high)

    else:
        return -1

array = [3, 4, 5, 6, 7, 8, 9]
x = 4

result = binarySearch(array, x, 0, len(array)-1)

if result != -1:
    print("Element is present at index " + str(result))
else:
    print("Not found")
```

## Python Sorting algorithms

### Bubble sort
Bubble sort is a sorting algorithm that compares two adjacent elements and swaps them until they are in the intended order.

- The time complexity in worse case is O(n^2).
- The space complexity is O(1) because an extra variable is used for swapping.

``` python
def bubbleSort(arr):
    for i in range(len(arr)):
        for j in range(len(arr) - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
```

### Selection sort
Selection sort is a sorting algorithm that selects the smallest element from an unsorted list in each iteration and places that element at the beginning of the unsorted list.

- The time complexity of selection sort is O(n^2).
- The space complexity of selection sort is O(1).

``` python
def selectionSort(arr):
    size = len(arr)

    for step in range(size):
        min_idx = step

        for i in range(step + 1, size):
            if arr[i] < arr[min_idx]:
                min_idx = i
        
        arr[step], arr[min_idx] = arr[min_idx], arr[step]
```

### Insertion sort
Insertion sort is a sorting algorithm that places an unsorted element at its suitable place in each iteration.

Insertion sort works similarly as we sort cards in our hand in a card game.

- The time complexity of insertion sort is O(n^2).
- The space complexity of insertion sort is O(1).

``` python
def insertionSort(arr):
    for step in range(1, len(arr)):
        key = arr[step]
        j = step - 1

        while j >= 0 and key < arr[j]:
            arr[j + 1] = arr[j]
            j = j - 1

        arr[j + 1] = key
```

### Merge sort
Merge Sort is one of the most popular sorting algorithms that is based on the principle of Divide and Conquer Algorithm.
It repeatedly divides the array into two halves until we reach a stage where we try to perform MergeSort on a subarray of size 1.
After that, the merge function comes into play and combines the sorted arrays into larger arrays until the whole array is merged.

- The time complexity of merge sort is O(n * log n).
- The space complexity of merge sort is O(n).
- Merge sort is stable.

``` python
def mergeSort(arr):
    if len(arr) > 1:
        r = len(arr) // 2
        l = arr[:r]
        m = arr[r:]

        mergeSort(l)
        mergeSort(m)

        i = j = k = 0

        while (i < len(l) and j < len(m)):
            if l[i] < m[j]:
                arr[k] = l[i]
                i += 1
            else:
                arr[k] = m[j]
                j += 1
            k += 1

        while i < len(l):
            arr[k] = l[i]
            i += 1
            k += 1

        while j < len(m):
            arr[k] = m[j]
            j += 1
            k += 1
```

### Quick sort
Quicksort is a sorting algorithm based on the divide and conquer approach where
1. An array is divided into subarrays by selecting a pivot element (element selected from the array). While dividing the array, the pivot element should be positioned in such a way that elements less than pivot are kept on the left side and elements greater than pivot are on the right side of the pivot.
2. The left and right subarrays are also divided using the same approach. This process continues until each subarray contains a single element.
3. At this point, elements are already sorted. Finally, elements are combined to form a sorted array.

- The time complexity in worst case is O(n^2) while in best and average are O(n * log n).
- The space complexity of quick sort is O(log n).
- Quick sort is not stable.

``` python
def partition(arr, low, high):
    pivot = arr[high]

    i = low - 1

    for j in range(low, high):
        if arr[j] <= pivot:
            i = i + 1
            arr[i], arr[j] = arr[j], arr[i]

    arr[i + 1], arr[high] = arr[high], arr[i + 1]

    return i + 1

def quickSort(arr, low, high):
    if low < high:
        pi = partition(arr, low, high)

        quickSort(arr, low, pi - 1)

        quickSort(arr, pi + 1, high)
```

### Shell sort
Shell sort is a generalized version of the insertion sort algorithm. It first sorts elements that are far apart from each other and successively reduces the interval between the elements to be sorted.

- The time complexities in best and average case are O(n * log n).
- The time complexity in worst case is O(n^2).
- The space complexity of shell sort is O(1).
- Shell sort is not stable.

``` python
def shellSort(arr):
    size = len(arr)

    interval = size // 2
    while interval > 0:
        for i in range(interval, size):
            temp = arr[i]
            j = i
            while j >= interval and arr[j - interval] > temp:
                arr[j] = arr[j - interval]
                j -= interval

            arr[j] = temp
        interval //= 2
```

### Heap sort
Heap Sort is a popular and efficient sorting algorithm in computer programming.
It uses arrays and heap data structure.

Working of heap sort:
1. Since the tree satisfies Max-Heap property, then the largest item is stored at the root node.
2. Swap: Remove the root element and put at the end of the array (nth position) Put the last item of the tree (heap) at the vacant place.
3. Remove: Reduce the size of the heap by 1.
4. Heapify: Heapify the root element again so that we have the highest element at root.
5. The process is repeated until all the items of the list are sorted.

``` python
def heapify(arr, size, i):
    largest = i
    l = 2 * i + 1
    r = 2 * i + 2

    if l < size and arr[i] < arr[l]:
        largest = l

    if r < size and arr[largest] < arr[r]:
        largest = r

    if largest != i:
        arr[i], arr[largest] = arr[largest], arr[i]
        heapify(arr, size, largest)

def heapSort(arr):
    size = len(arr)

    for i in range(size//2, -1, -1):
        heapify(arr, size, i)

    for i in range(size - 1, 0, -1):
        arr[i], arr[0] = arr[0], arr[i]

        heapify(arr, i, 0)
```

### Counting sort
Counting sort is a sorting algorithm that sorts the elements of an array by counting the number of occurrences of each unique element in the array. The count is stored in an auxiliary array and the sorting is done by mapping the count as an index of the auxiliary array.

Generally speaking, counting sort is incapable of sorting negative numbers.

- The time complexity of counting sort is O(n+k).
- The space complexity is O(max).
- Counting sort is stable.

``` python
def countingSort(arr):
    size = len(arr)
    output = [0] * size

    count = [0] * (max(arr) + 1)

    for i in range(size):
        count[arr[i]] += 1
    
    for i in range(1, max(arr)+1):
        count[i] += count[i - 1]
        
    i = size - 1
    while i >= 0:
        output[count[arr[i]] - 1] = arr[i]
        count[arr[i]] -= 1
        i -= 1

    for i in range(size):
        arr[i] = output[i] 
```

### Bucket sort
Bucket Sort is a sorting algorithm that divides the unsorted array elements into several groups called buckets. 
Each bucket is then sorted by using any of the suitable sorting algorithms or recursively applying the same bucket algorithm.
Finally, the sorted buckets are combined to form a final sorted array.

Can be used to sort decimals.

- The time complexity in average case is O(n) and O(n^2) in worst case.
- The space complexity is O(n+k)
- Bucket sort is stable

``` python
def bucketSort(array):
    bucket = []

    # Create empty buckets
    for i in range(len(array)):
        bucket.append([])

    # Insert elements into their respective buckets
    for j in array:
        index_b = int(10 * j)
        bucket[index_b].append(j)

    # Sort the elements of each bucket
    for i in range(len(array)):
        bucket[i] = sorted(bucket[i])

    # Get the sorted elements
    k = 0
    for i in range(len(array)):
        for j in range(len(bucket[i])):
            array[k] = bucket[i][j]
            k += 1
    return array
```

### Radix sort
Radix sort is a sorting algorithm that sorts the lements by first grouping the individual digits of the same place value.
Then sort the elements according to their increasing/decreasing order.

- The time complexity of radix sort in best, average and worst cases are O(n+k).
- The space complexity is O(max).
- Radix sort is stable.

``` python
def countingSortforRadix(arr, place):
    size = len(arr)
    output = [0] * size
    max_len = max(arr) + 1
    count = [0] * max_len

    for i in range(size):
        index = arr[i] // place
        count[index % 10] += 1

    for i in range(1, max_len):
        count[i] += count[i - 1]

    i = size - 1
    while i >= 0:
        index = arr[i] // place
        output[count[index % 10] - 1] = arr[i]
        count[index % 10] -= 1
        i -= 1

    for i in range(size):
        arr[i] = output[i]

def radixSort(arr):
    max_element = max(arr)

    place = 1
    while max_element // place > 0:
        countingSortforRadix(arr, place)
        place *= 10
```

## Greedy Algorithms

## Dynamic Programming

# Python with other modules

## Python with Flask
``` python
import flask
```

## Python with Subprocess
The subprocess module allows you to spawn new processes, connect to their input/output/error pipes and obtain their codes.
We can run shell commands on Python scripts via the subprocess module.

```subprocess.run(args, *, stdin=None, input=None, stdout=None, stderr=None, capture_output=False, shell=False, cwd=None, timeout=None, check=False, encoding=None, errors=None, text=None, env=None, universal_newlines=None, **other_popen_kwargs)```

The subprocess module can make Python interact with shell.
``` python
# Strings of the form <pathname> should be replaced with the contents of the file named pathname.
# Strings of the form <!command> should be replaced by the output of running command as a shell command.
# other words remains the same
for line in sys.stdin:
    for command in re.finditer(r"<(!?)(.*?)>", line):
        if command.group(1) == "!":
            line = line.replace(command.group(0), subprocess.run(command.group(2), shell=True, capture_output=True, text=True).stdout)
        else:
            line = line.replace(command.group(0), subprocess.run(f"cat {command.group(2)}", shell=True, capture_output=True, text=True).stdout)
    print(line, end="")
```

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
string = "Hello World, I am good. My number is z1234567."

# extract the part that contains Hello
m = re.search("Hello", string)
print(m)                    # <re.Match object; span=(0, 5), match='Hello'>
print(m.group(0))           # Hello

# extract the first word separated by whitespace that contains l
m = re.search('\s*\S+l\s*\S+', string)
print(m)                    # <re.Match object; span=(0, 5), match='Hello'>
print(m.group(0))           # Hello

m = re.search(r'[aiou].*[aeiou]', 'pillow')
print(m)                    # <re.Match object; span=(1, 5), match='illo'>
print(m.group(0))           # illo
print(m.span())             # (1, 5)

m = re.search("hello\D+\d+", string)
print(m)                    # None

m = re.search("hello\D+\d+", string, re.I)
# <re.Match object; span=(0, 45), match='Hello World, I am good. My number is z1234567'>
print(m)
```

```re.match(regex, string, flags)```
- only match at start of string
- same as re.search stating with ^
``` python
string = "Hello World, I am good. My number is z1234567."

# extract the part that contains Hello
m = re.match("World", string)
print(m)                    # None because the string does not start with World

# search() vs match()
# re.match() checks for a match only at the beginning of the string
# re.search() checks for a match anywhere in the string
print(re.match("c", "abcdef"))      # No match
print(re.search("c", "abcdef"))     # <re.Match object; span=(2, 3), match='c'>
```

```re.fullmatch(regex, string, flags)```
- only match the full string
- same as re.search starting with ^ and ending with $
``` python
string = "Hello World, I am good. My number is z1234567"

m = re.search("World\D+\d+", string)
# <re.Match object; span=(6, 45), match='World, I am good. My number is z1234567'>
print(m)

m = re.match("World\D+\d+", string)
# None
print(m)

m = re.match("Hello\D+\d+", string)
# <re.Match object; span=(0, 45), match='Hello World, I am good. My number is z1234567'>
# re.match() checks from the beginning, so Hello can pass while World doesn't
print(m)

m = re.match("Hello\D+", string)
# <re.Match object; span=(0, 38), match='Hello World, I am good. My number is z'>
print(m)

m = re.fullmatch("Hello\D+", string)
# None because the end of the string is not non-digit
print(m)

m = re.fullmatch("Hello\D+\d+", string)
# <re.Match object; span=(0, 45), match='Hello World, I am good. My number is z1234567'>
print(m)
```

```re.sub(regex, replacement, string, count, flags)```
- return string with anywhere regex matches, substituted by replacement
- optional parameter count, if non-zero, sets maximum number of substitutions
``` python
# \number can be used to refer to group number in an re.sub replacement string
m = re.sub(r'(\d+) and (\d+)', r'\2 or \1', "The answer is 42 and 43?")
print(m)            # The answer is 43 or 42?

m = re.sub(r'ab+c', 'X', "abbabbbbbbbabbbc")
print(m)            # abbabbbbbbbX

m = re.sub(r'a.*bc', 'X', "abbabbbbbbbcabbb")
print(m)            # Xabbb
```

```re.findall(regex, string, flags)```
- return all non-overlapping matches of pattern in string
- if pattern contains () return part matched by ()
- if pattern contains multiple () return tuple
``` python
# regex findall returns a list of items
# the example below extracts a list of numbers from the string
m = re.findall(r'\d+', "hello 42 I'm a 32 string 30")
print(m)                    # ['42', '32', '30']
```

```re.split(regex, string, maxsplit, flags)```
- Split string everywhere regex matches
- optional parameter maxsplit, if non-zero, set maximum number of splits
``` python
m = re.split(r'\W+', 'Words, words, words.')
print(m)        # ['Words', 'words', 'words', '']

# by using capturing parentheses, we are not just capturing the strings between the split patterns but also the split patterns themselves
m = re.split(r'(\W+)', 'Words, words, words.')
print(m)        # ['Words', ', ', 'words', ', ', 'words', '.', '']

m = re.split(r'\W+', 'Words, words, words.', 1)
print(m)        # ['Words', 'words, words.']

m = re.split('[a-f]+', '0a3B9', flags=re.I)
print(m)        # ['0', '3', '9']

# If there are capturing groups in the separator and it
# matches at the start of the string,
# the result will start with an empty string
m = re.split(r'(\W+)', '...words, words...')
print(m)        # ['', '...', 'words', ', ', 'words', '...', '']
```

```re.finditer(pattern, string, flags)```
- return an iterator yielding match objects over all non-overlapping matches for the RE pattern in string.
- the string is scanned left-to-right, and matches are returned in the order found.
``` python
# a complex example
first = "Here is <!echo practice_q9.txt>"
second = "Next is <practice_q9.txt>"

match_one = re.finditer(r"<(!?)(.*?)>", first)
print(match_one)        # <callable_iterator object at 0x7fe76131cee0>
for i in match_one:
    print(i)            # <re.Match object; span=(8, 31), match='<!echo practice_q9.txt>'>
    print(i.group(0))   # <!echo practice_q9.txt>
    print(i.group(1))   # !
    print(i.group(2))   # echo practice_q9.txt

match_two = re.finditer(r"<(!?)(.*?)>", second)
print(match_two)        # <callable_iterator object at 0x7f4c0d41e280>
for i in match_two:
    print(i)            # <re.Match object; span=(8, 25), match='<practice_q9.txt>'>
    print(i.group(0))   # <practice_q9.txt>
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
# extract two words that separated by a whitespace
m = re.match(r"(\w+) (\w+)", "Isaac Newton, physicist")
print(m)                    # <re.Match object; span=(0, 12), match='Isaac Newton'>
print(m.groups())           # Return a tuple containing all the subgroups of the match ('Isaac', 'Newton')
print(m.group(0))           # The entire match                      Isaac Newton
print(m.group(1))           # The first parenthesized subgroup.     Isaac
print(m.group(2))           # The second parenthesized subgroup.    Newton
print(m.group(1, 2))        # Multiple arguments give us a tuple.   ('Isaac', 'Newton')

# Match object with default values
m = re.match(r"(\d+)\.?(\d+)?", "24")
m.groups()      # Second group defaults to None. -> ('24', None)
m.groups('0')   # Now, the second group defaults to '0'. -> ('24', '0')

# Match.groupdict(default=None)
m = re.match(r"(?P<first_name>\w+) (?P<last_name>\w+)", "Malcolm Reynolds")
print(m)                # <re.Match object; span=(0, 16), match='Malcolm Reynolds'>
print(m.groupdict())    # {'first_name': 'Malcolm', 'last_name': 'Reynolds'}
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
Psycopg is the most popular PostgreSQL database adapter for the Python programming language.
Psycopg2 is mostly implemented in C as a libpq wrapper, resulting in being both efficient and secure.

Installation:
```$ pip install psycopg2```

``` python
import psycopg2
```

``` python
# connect to our desired database which is call mydb
conn = psycopg2.connect(f"dbname='mydb'")
# get the cursor
# cursors are bound to the connection for the entire lifetime and 
# all the commands are executed in the context of the database session wrapped by the connection.
cur = conn.cursor()
# execute the sql query
# query is the sql query and [] are the arguments
cur.execute(query, [subject,term])
# get the results
students = cur.fetchall()
students = cur.fetchone()
students = cur.fetchmany(3)
```

``` python
# print a specified player's career performance
import sys
import psycopg2

db = None
cur = None

if len(sys.argv) < 2:
   print(f"Usage: {sys.argv[0]} PlayerName")
   exit(1)
player = sys.argv[1]

qPlayer = "select id,name from Players where name = %s";
qGames  = """
select m.id, m.city, m.playedOn
from   Teams t join Involves i on (i.team=t.id)
       join Matches m on (m.id=i.match)
       join Players p on (t.id=p.memberof)
where  p.id = %s
order  by m.playedOn
"""
qGoals = "select count(*) from Goals where scoredIn = %s and scoredBy = %s"
qTeam  = """
select t.country
from   Teams t join Players p on (t.id = p.memberof)
where  p.id = %s
"""

totMatches = 0
totGoals = 0
     
try:
   db = psycopg2.connect("dbname=footy")
   cur = db.cursor();
   cur.execute(qPlayer,[player])
   res = cur.fetchone()
   if not res:
      print("No such player")
      exit(1)
   pid,name = res
   cur.execute(qGames, [pid])
   for g in cur.fetchall():
      totMatches = totMatches + 1
      mid,city,date = g
      cur.execute(qGoals, [mid,pid])
      ngoals = cur.fetchone()[0];
      totGoals = totGoals + ngoals
      if ngoals == 0:
         continue
      elif ngoals == 1:
         goals = " and scored 1 goal"
      else:
         goals = f" and scored {ngoals} goals"
      print(f"played in {city} on {date}{goals}")
   cur.execute(qTeam, [pid])
   team = cur.fetchone()[0]
   print(f"Summary: played for {team}, {totMatches} matches, {totGoals} goals")
except psycopg2.Error as err:
	print("DB error: ", err)
finally:
   if cur:
       cur.close()
   if db:
      db.close()
```

## Python with Statistics
``` python
import statistics
```

Averages and measures of central location
- ```mean()``` - arithmetic mean (average) of data
- ```fmean()``` - fast, floating point arithmetic mean
- ```geometric_mean()``` - geometric mean of data
- ```harmonic_mean()``` - harmonic mean of data
- ```median()``` - median (middle value) of data
- ```median_low()``` - low median of data
- ```median_high()``` - high median of data
- ```mode()``` - single mode (most common value) of discrete or nominal data
- ```multimode()``` - list of modes of discrete or nominal data
- ```quantiles()``` - divide data into intervals with equal probability

Measures of spread
- ```pstdev()``` - population standard deviation of data
- ```pvariance()``` - population variance of data
- ```stdev()``` - sample standard deviation of data
- ```variance()``` - sample variance of data

Statistics for relations between two inputs
- ```covariance()``` - sample covariance for two variables
- ```correlation()``` - person's correlation coeeficient for two variables
- ```linear_regression()``` - slope and intercept for simple linear regression

``` python
import statistics

first_nums = [1 , 2, 3]
second_nums = [-1.0, 2.5, 3.25, 5.75]
third_nums = ["red", "blue", "blue", "red", "green", "red", "red"]

# average of data
print(statistics.mean(first_nums))              # 2
print(statistics.mean(second_nums))             # 2.625

# fast, floating point average
print(statistics.fmean(first_nums))             # 2.0
print(statistics.fmean(second_nums))            # 2.625

# geometric mean of data
print(statistics.geometric_mean(first_nums))    # 1.8171205928321397

# harmonic mean of data
print(statistics.harmonic_mean(first_nums))     # 1.6363636363636365

# middle value of data
print(statistics.median(first_nums))            # 2
print(statistics.median(second_nums))           # 2.875

# low median of data
print(statistics.median_low(second_nums))       # 2.5

# high median of data
print(statistics.median_high(second_nums))      # 3.25

# most common value of data
print(statistics.mode(third_nums))              # red

# standard deviation
print(statistics.stdev(second_nums))            # 2.787621447279622

# variance
print(statistics.variance(second_nums))         # 7.770833333333333
```

## Python with Math
``` python
import math
```

- ```math.ceil(x)``` - the ceiling of x
- ```math.comb(n, k)``` - the combination of n and k which is ```n! / (k! * (n - k)!)```
- ```math.fabs(x)``` - the absolute value of x
- ```math.factorial(x)``` - x factorial as an integer
- ```math.floor(x)``` - the floor of x which is the integer less than or equal to x
- ```math.gcd(*integers)``` - the greatest common divisor of the integer arguments
- ```math.lcm(*integers)``` - the least common divisor of the integer arguments
- ```math.perm(n, k=None)``` - the permutation of n and k which is ```n! / (n - k)!```
- ```math.prod(iterable, *, start=1)``` - calculate the product of all the elements in the input iterable
- ```math.exp(x)``` - return e raised to the power x.
- ```math.log(x[, base])``` - return the logarithm and we can specify the base
- ```math.pow(x, y)``` - return x raised to the power y
- ```math.sqrt(x)``` - return the square root of x
- ```math.cos(x)``` - cosine of x radians
- ```math.sin(x)``` - return the sine of x radians
- ```math.tan(x)``` - return the tangent of x radians
- ```math.degrees(x)``` - convert angle x from radians to degrees
- ```math.radians(x)``` - convert angle x from degrees to radians
- ```math.pi``` - the constant π = 3.141592…
- ```math.e``` - the constant e = 2.718281…

## Python with Sys
``` python
import sys
```

- ```sys.argv``` - the list of command line arguments passed to a Python script.
- ```sys.exit([arg])``` - raise a SystemExit exception, signalling an intention to exit the interpreter.
- ```sys.path``` - a list of strings that specifies the search path for modules.
- ```sys.stdin``` - standard input, used for all interactive input.
- ```sys.stdout``` - standard output, used for the output of print() and expression statements and for the prompts of input().
- ```sys.stderr``` - the interpreter's own prompts and its error messages go to this way.
- ```sys.version``` - a string containing the version number of the Python interpreter plus additional information on the build number and compiler used.

## Python with Collections
The collection Module in Python provides different types of containers.
A container is an object that is used to store different objects and provide a way to access the contained objects and iterate over them.

``` python
import collections
```

### Counters
A counter is a sub-class of the dictionary. It is used to keep the count of the elements in an iterable in the form of an unordered dictionary where the key represents the element in the iterable and value represents the count of that element in the iterable

Syntax: ```class collections.Counter([iterable-or-mapping])```

``` python
# with sequence of items
# Counter({'B': 5, 'A': 3, 'C': 2})
print(collections.Counter(['B','B','A','B','C','A','B',
               'B','A','C']))

# with dictionary
# Counter({'B': 5, 'A': 3, 'C': 2})
print(collections.Counter({'A':3, 'B':5, 'C':2}))

# with keyword arguments
# Counter({'B': 5, 'A': 3, 'C': 2})
print(collections.Counter(A=3, B=5, C=2))

data = collections.Counter(A=3, B=5, C=2)
# A - 3
# B - 5
# C - 2
for i in data:
    print(f"{i} - {data[i]}")
```

### OrderedDict
An OrderedDict is also a sub-class of dictionary but unlike dictionary, it remembers the order in which the keys were inserted.

Syntax: ```class collections.OrderDict()```

``` python
od = collections.OrderedDict() 
od['a'] = 4
od['b'] = 2
od['c'] = 1
od['d'] = 3
    
# a 4
# b 2
# c 1
# d 3
for key, value in od.items(): 
    print(key, value)
    
# deleting element
od.pop('a')
  
# Re-inserting the same
od['a'] = 1

# b 2
# c 1
# d 3
# a 1
for key, value in od.items(): 
    print(key, value)
```

### DefaultDict
A DefaultDict is also a sub-class to dictionary.
It is used to provide some default values for the key that does not exist and never raises a KeyError.

Syntax: ```class collections.defaultdict(default_factory)```

``` python
# Defining the dict 
# DefaultDict objects can be initialized using DefaultDict() method 
# by passing the data type as an argument.
d = collections.defaultdict(int) 
     
L = [1, 2, 3, 4, 2, 4, 1, 2] 
     
# Iterate through the list 
# for keeping the count 
for i in L: 
         
    # The default value is 0 
    # so there is no need to  
    # enter the key first 
    d[i] += 1

# defaultdict(<class 'int'>, {1: 2, 2: 3, 3: 1, 4: 2})       
print(d)
```

### Deque
A deque is similar to all of the other sequential data structures but
has some implemenation details that are different from other sequences like a list.
This module highlights those differences and shows how a deque can be used as a LIFO stack and a FIFO queue.

Deque objects support the following methods:
- ```append(x)``` - add x to the right side of the deque.
- ```appendleft(x)``` - add x to the left side of the deque.
- ```clear()``` - remove all elements from the deque leaving it with length 0.
- ```copy()``` - create a shallow copy of the deque.
- ```count(x)``` - count the number of deque elements equal to x.
- ```extend(iterable)``` - extend the right side of the deque by appending elements from the iterable argument.
- ```extendleft(iterable)``` - extend the left side of the deque by appending elements from iterable.
- ```index(x[, start[, stop]])``` - Return the position of x in the deque (at or after index start and before index stop). Returns the first match or raises ValueError if not found.
- ```insert(i, x)``` - insert x into the deque at position i.
- ```pop()``` - remove and return an element from the right side of the deque.
- ```popleft()``` - remove and return an element from the left side of the deque.
- ```remove(value)``` - remove the first occurence of value. If not found, raises a ValueError.
- ```reverse()``` - reverse the elements of the deque in-place and then return None.
- ```rotate(n=1)``` - rotate the deque n steps to the right. If n is negative, rotate to the left.
- ```maxlen``` - maximum size of a deque or None if unbounded.

``` python
import collections

d = collections.deque('good')   # create a new deque with four items
for element in d:
    print(element)              # iterate over and print deque's elements

d.append('h')
print(d)                        # deque(['g', 'o', 'o', 'd', 'h'])

d.appendleft('f')
print(d)                        # deque(['f', 'g', 'o', 'o', 'd', 'h'])

d.pop()
print(d)                        # deque(['f', 'g', 'o', 'o', 'd'])

d.popleft()
print(d)                        # deque(['f', 'g', 'o', 'o', 'd'])

print(list(d))                  # ['g', 'o', 'o', 'd']

d.rotate(1)
print(d)                        # deque(['d', 'g', 'o', 'o'])

d.rotate(-1)
print(d)                        # deque(['g', 'o', 'o', 'd'])

new_d = d.copy()
print(new_d)                    # deque(['g', 'o', 'o', 'd'])

print(d.count('o'))             # 2

d.extend("hello")
print(d)                        # deque(['g', 'o', 'o', 'd', 'h', 'e', 'l', 'l', 'o'])

new_d.extendleft("hey")
print(new_d)                    # deque(['y', 'e', 'h', 'g', 'o', 'o', 'd'])

d = collections.deque('good')
print(d.index('o'))             # 1

d.insert(2, 'h')
print(d)                        # deque(['g', 'o', 'h', 'o', 'd'])

d.remove('o')
print(d)                        # deque(['g', 'h', 'o', 'd'])

d.reverse()
print(d)                        # deque(['d', 'o', 'h', 'g'])

print(d.maxlen)                 # None (means unbounded)
```

## Python with Random
The random module implements pseudo-random number generators for various distributions.
``` python
import ranodm
```
- ```random.seed(a=None, version=2)``` - initialize the random number generator.
- ```random.random()``` - return the next random floating point number in the range [0.0, 1.0).
- ```random.uniform()``` - return a random floating point number N such that a <= N <= b for a <= b and b <= N <= a for b < a.
- ```random.randrange(start, stop[, step])``` - generate a random integer
- ```random.randint(a, b)``` - Return a random integer N such that a <= N <= b. Alias for randrange(a, b+1).
- ```random.choice(seq)``` - Return a random element from the non-empty sequence seq. If seq is empty, raises IndexError.
- ```random.choices(population, weights=None, *, cum_weights=None, k=1)``` - Return a k sized list of elements chosen from the population with replacement. If the population is empty, raises IndexError.
- ```random.shuffle(x[, random])``` - shuffle the sequence x in place.
- ```random.sample(population, k, *, counts=None)``` - Return a k length list of unique elements chosen from the population sequence or set. Used for random sampling without replacement.

``` python
print(random.random())              # Random float:  0.0 <= x < 1.0
print(random.uniform(2.5, 10.0))    # Random float:  2.5 <= x <= 10.0
print(random.randrange(10))         # Integer from 0 to 9 inclusive
print(random.randrange(0, 101, 2))  # Even integer from 0 to 100 inclusive
print(random.choice(['win', 'lose', 'draw']))   # Single random element from a sequence, might generate 'draw'

deck = 'ace two three four'.split()
print(deck)             # ['ace', 'two', 'three', 'four']
random.shuffle(deck)
print(deck)             # ['four', 'three', 'two', 'ace']

# [50, 40, 30, 20]
print(random.sample([10, 20, 30, 40, 50], k=4))

# Six roulette wheel spins (weighted sampling with replacement)
# ['red', 'green', 'black', 'black', 'red', 'black']
print(random.choices(['red', 'black', 'green'], [18, 18, 2], k=6))
```

## Python with JSON
JSON standards for JavaScript Object Notation, is a lightweight data-interchange format.
It is easy for humans to read and write.
It is easy for machines to parse and generate.

JSON is built on two structures:
- a collection of name/value pairs. In various languages, this is realized as an object, record, struct, dictionary, hash table, keyed list or associative array.
- an ordered list of values. In most languages, this is realized as an array, vector, list or sequence.
``` python
import json
```

- ```json.dumps(obj, *, skipkeys=False, ensure_ascii=True, check_circular=True, allow_nan=True, cls=None, indent=None, separators=None, default=None, sort_keys=False, **kw)``` - serialize obj to a JSON formatted str.
- ```json.loads(s, *, cls=None, object_hook=None, parse_float=None, parse_int=None, parse_constant=None, object_pairs_hook=None, **kw)``` - deserialize s (a str, bytes or bytearray instance containing a JSON document) to a Python object. For example, converting from string to dictionary.

Note:
- keys in key/value pairs of JSON are always of the type str.
- when a dictionary is converted into JSON, all the keys of the dictionary are coerced to strings.
- as a result of this, if a dictionary is converted into JSON and then back into a dictioanry, the dictionary may not equal to the original one.

``` python
import json

# converting from string to object
# some JSON:
x =  '{ "name":"John", "age":30, "city":"New York"}'

# parse x:
y = json.loads(x)

# the result is a Python dictionary:
print(y["age"])         # 30

# Converting from object to string
# a Python object (dict):
x = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

# convert into JSON:
y = json.dumps(x)

# the result is a JSON string:
print(y)                # {"name": "John", "age": 30, "city": "New York"}

x = {
  "name": "John",
  "age": 30,
  "married": True,
  "divorced": False,
  "children": ("Ann","Billy"),
  "pets": None,
  "cars": [
    {"model": "BMW 230", "mpg": 27.5},
    {"model": "Ford Edge", "mpg": 24.1}
  ]
}

# {"name": "John", "age": 30, "married": true, "divorced": false, "children": ["Ann", "Billy"], "pets": null, "cars": [{"model": "BMW 230", "mpg": 27.5}, {"model": "Ford Edge", "mpg": 24.1}]}
print(json.dumps(x))
```

## Python with CSV
The so-called CSV(Comma Separated Values) format is the most common import and export format for spreadsheets and databases.
CSV format was used for many years prior to attempts to describe the format in a standardized way.
The csv module implements classes to read and write tabular data in CSV format.
``` python
import csv
```

- ```csv.reader(csvfile, dialect='excel', **fmtparams)``` - return a reader object which will iterate over lines in the given csvfile.
- ```csv.writer(csvfile, dialect='excel', **fmtparams)``` - return a writer object responsible for converting the user's data into delimited strings on the given file-like object.

### Parameters
* `'dialect'` - Master parameter that sets the default values. String or a Dialect object.
* `'delimiter'` - A one-character string used to separate fields.
* `'quotechar'` - Character for quoting fields that contain special characters.
* `'doublequote'` - Whether quotechars inside fields are/get doubled or escaped.
* `'skipinitialspace'` - Is space character at the start of the field stripped by the reader.
* `'lineterminator'` - How writer terminates rows. Reader is hardcoded to '\n', '\r', '\r\n'.
* `'quoting'` - 0: As necessary, 1: All, 2: All but numbers which are read as floats, 3: None.
* `'escapechar'` - Character for escaping quotechars if doublequote is False.

### Read Rows from CSV File
```python
def read_csv_file(filename, dialect='excel'):
    with open(filename, encoding='utf-8', newline='') as file:
        return list(csv.reader(file, dialect))
```

### Write Rows to CSV File
```python
def write_to_csv_file(filename, rows, dialect='excel'):
    with open(filename, 'w', encoding='utf-8', newline='') as file:
        writer = csv.writer(file, dialect)
        writer.writerows(rows)
```

Coding Example:
``` python
import sys
import csv
# read from standard input
data = csv.reader(sys.stdin, delimiter='|')
# ['COMP1511', '3360379', 'Costner, Kevin Augustus          ', '3978/1', 'M']
# ...
for line in data:
    print(line)
    course, stuid, name, progam, gender = line
    # COMP1511/3360379/Costner, Kevin Augustus          /3978/1/M
    print("/".join([course, stuid, name, progam, gender]))
```
We can also open a file
``` python
with open('enrollments.txt') as enrollments:
    data = csv.reader(enrollments, delimiter="|")
    # ['COMP1511', '3360379', 'Costner, Kevin Augustus          ', '3978/1', 'M']
    # ...
    for line in data:
        print(line)
```

## Python with Datetime
A date in Python is not a data type of its own, but we can import a module named datetime to work with dates as date objects.
``` python
import datetime
```

The reference of all the legal format codes (used in strftime()):
- ```%a``` - Weekday, short version -- Wed
- ```%A``` - Weekday, full version -- Wednesday
- ```%w``` - Weekday as a number 0-6, 0 is Sunday -- 3
- ```%d``` - Day of month 01-31	-- 31
- ```%b``` - Month name, short version -- Dec
- ```%B``` - Month name, full version -- December	
- ```%m``` - Month as a number 01-12 -- 12	
- ```%y``` - Year, short version, without century -- 18	
- ```%Y``` - Year, full version -- 2018	
- ```%H``` - Hour 00-23 -- 17	
- ```%I``` - Hour 00-12 -- 05	
- ```%p``` - AM/PM -- PM	
- ```%M``` - Minute 00-59 -- 41	
- ```%S``` - Second 00-59 -- 08	
- ```%f``` - Microsecond 000000-999999 -- 548513	
- ```%z``` - UTC offset -- +0100	
- ```%Z``` - Timezone -- CST	
- ```%j``` - Day number of year 001-366 -- 365	
- ```%U``` - Week number of year, Sunday as the first day of week, 00-53 -- 52	
- ```%W``` - Week number of year, Monday as the first day of week, 00-53 -- 52	
- ```%c``` - Local version of date and time -- Mon Dec 31 17:41:00 2018	
- ```%C``` - Century -- 20	
- ```%x``` - Local version of date -- 12/31/18	
- ```%X``` - Local version of time -- 17:41:00	
- ```%%``` - A % character -- %	
- ```%G``` - ISO 8601 year -- 2018	
- ```%u``` - ISO 8601 weekday (1-7) -- 1	
- ```%V``` - ISO 8601 weeknumber (01-53) -- 01


``` python
import datetime

x = datetime.datetime.now()
print(x)                    # 2022-08-30 08:51:14.821024

print(type(x))              # <class 'datetime.datetime'>
print(x.year)               # 2022
print(x.month)              # 8
print(x.day)                # 30
print(x.hour)               # 8
print(x.minute)             # 53
print(x.second)             # 1

# creating date objects
y = datetime.datetime(2020, 5, 17)

print(y)                    # 2020-05-17 00:00:00

# the strftime() method
# it takes one parameter which is the format to specify the format of the returned string
print(x.strftime("%A"))     # Tuesday
print(x.strftime("%B"))     # August
```

## Python with Typing
``` python
import typing
```
This module provides runtime support for type hints.

The function below takes and returns a string and is annotated as follows:
``` python
def greeting(name: str) -> str:
    return 'Hello ' + name
```

### Any
Basically Any means any type.

### Type aliases
A type alias is defined by assigning the type to the alias. In this example, Vector and list[float] will be treated as interchangeable synonyms, we can also interchange Vector with list[int] or other types.
``` python
Vector = list[float]

def scale(scalar: float, vector: Vector) -> Vector:
    return [scalar * num for num in vector]

# typechecks; a list of floats qualifies as a Vector.
new_vector = scale(2.0, [1.0, -4.2, 5.4])
```

### NewType
Use the NewType helper to create distinct types:
``` python
from typing import NewType

UserId = NewType('UserId', int)
some_id = UserId(524313)
```

The static type checker will treat the new type as if it were a subclass of the original type. This is useful in helping catch logical errors:
``` python
def get_user_name(user_id: UserId) -> str:
    ...

# typechecks
user_a = get_user_name(UserId(42351))

# does not typecheck; an int is not a UserId
user_b = get_user_name(-1)
```

### Generics
Since type information about objects kept in containers cannot be statically inferred in a generic way, abstract base classes have been extended to support subscription to denote expected types for container elements.
``` python
from collections.abc import Mapping, Sequence

def notify_by_email(employees: Sequence[Employee],
                    overrides: Mapping[str, str]) -> None: ...
```

Generics can be parameterized by using a factory available in typing called TypeVar.
``` python
from collections.abc import Sequence
from typing import TypeVar

T = TypeVar('T')      # Declare type variable

def first(l: Sequence[T]) -> T:   # Generic function
    return l[0]
```

User-defined generic types
``` python
from typing import TypeVar, Generic
from logging import Logger

T = TypeVar('T')

class LoggedVar(Generic[T]):
    def __init__(self, value: T, name: str, logger: Logger) -> None:
        self.name = name
        self.logger = logger
        self.value = value

    def set(self, new: T) -> None:
        self.log('Set ' + repr(self.value))
        self.value = new

    def get(self) -> T:
        self.log('Get ' + repr(self.value))
        return self.value

    def log(self, message: str) -> None:
        self.logger.info('%s: %s', self.name, message)
```

## Python with Argparse
``` python
import argparse
```
The argparse module makes it easy to write user-friendly command-line interfaces.
The program defines what arguments it requires, and argparse will figure out how to parse those out of sys.argv.

### Getting started
``` python
# Import the library
import argparse

# Create the parser
parser = argparse.ArgumentParser()

# Add an argument
# --name specifies that the name of the varaible
# type=str specifies that the type of the argument is string
# required=True means we must give an argument to the variable

# python3 prac.py (doesn't work)
# python3 prac.py myName (doesn't work)
# python3 prac.py --name myName (works)
parser.add_argument('--name', type=str, required=True)

# Parse the argument
args = parser.parse_args()

# Print "Hello" + the user input argument
# In this case, we have Hello, myName
print('Hello,', args.name)
```

### Positional Arguments
Sometimes we don't want to use the flag's name in the argument.
We can use a positional argument to eliminate the needto specify the --name flag before inputting the actural value.

required is invalid for positional arguments

``` python
import argparse

parser = argparse.ArgumentParser()
# just x without --x
parser.add_argument('x', type=int)
parser.add_argument('y', type=int)
args = parser.parse_args()

product = args.x * args.y
print('Product:', product)

>> python3 prac.py 4 5
Product: 20
```

We can use the help parameter in add_argument() to specify more details about the argument.
``` python
parser.add_argument('x', type=int, help='The first value to multiply')
parser.add_argument('y', type=int, help='The second value to multiply')

>> python3 prac.py -h
usage: prac.py [-h] x y
positional argumetns:
x	The first value to multiply
y       The second value to multiply
```

### Optional Arguments
Optional arguments are useful if we want to give the user a choice to enable certain features.

``` python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument('--name', type=str, required=True)
parser.add_argument('--age', type=int)
args = parser.parse_args()

if args.age:
  print(args.name, 'is', args.age, 'years old.')
else:
  print('Hello,', args.name + '!')

# >> python3 prac.py --name myName --age 16
# myName is 16 years old.

# >> python3 prac.py --name myName
# Hello, myName!
```

### Multiple Input Arguments
Using the nargs parameter in add_argument(), we can sepecify the number of inputs the argument should expect.

``` python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument('--values', type=int, nargs=3)
args = parser.parse_args()

sum = sum(args.values)
print('Sum:', sum)

>> python3 prac.py --values 1 2 3
Sum: 6
```

We can also set nargs='+', whcih will allow the argument to take in any number of values.
``` python
>> python3 prac.py --values 1 2 3 4 5 6 7 8 9 10
Sum: 55
```

### Mutually Exclusive Arguments
There are times that, depending on one argument, you want to restrict the use of another. 
This could be because the user should only need to use one of the arguments, or that the arguments conflict with each other. 
The method add_mutually_exclusive_group() let’s us do exactly that — add a group of arguments that are mutually exclusive.

``` python
import argparse

parser = argparse.ArgumentParser()
group = parser.add_mutually_exclusive_group()
# argument if mentioned stores true value
group.add_argument('--add', action='store_true')
group.add_argument('--subtract', action='store_true')
parser.add_argument('x', type=int)
parser.add_argument('y', type=int)
args = parser.parse_args()

if args.add:
    sum = args.x + args.y
    print('Sum:', sum)
elif args.subtract:
    difference = args.x - args.y
    print('Difference:', difference)

# >> python3 prac.py --add 1 2
# Sum: 3

# >> python3 prac.py --add 4 3
# Difference: 1
```

### A more structured example
``` python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument('-i', action='store_true')
parser.add_argument('-n', action='store_true')
parser.add_argument('-f', nargs=1)
parser.add_argument('files', type=str, nargs='+')
args = parser.parse_args()

if args.i:
    print('have more operations')

if args.n:
    print('don\'t print any line')

file = args.f[0]
with open(file) as f:
    for line in f:
        print(line.strip('\n'))

files = args.files
for i in files:
    print(i)
```

## Python with OS
``` python
import os
```

Frequently used methods in os module:
- `getcwd()` - get current working directory
- `chdir(x)` - change current working directory to x
- `mkdir(x)` - create a new direcrory x
- `makedirs(x)` - create directory x recursively (can make leaf directory if any intermediate directory is missing)
- `listdir(x)` - list all files and directories in path x
- `remove()` - used to delete a file by a file path
- `rmdir()` - used to delete a directory by a directory path
- `rename(old, new)` - used to rename a file
- `path.exists(x)` - check if file x exists
- `path.getsize(x)` - get the size of the file x in bytes
- `name` - gives the name of the operating system dependent module imported

``` python
import os

# get current working directory
cwd = os.getcwd()
print(cwd)

# delete a directory
os.rmdir('newPython')

# create a directory
os.mkdir('newPython')

# create a directory recursively
os.makedirs('hey/new')

# changing the current working directory
os.chdir('../')
print(os.getcwd())

# get the list of all files and directories
print(os.listdir())

file = 'file.txt'
path = os.path.join(cwd, file)

# get size of a file
print(os.path.getsize(path))

# delete a file by the file path
os.remove(path)

print(os.name)      # posix
```

## Python with Socket
A network socket is a software structure within a network node of a computer network that serves as an endpoint for sending and receiving data across the network.

Socket programming is a way of connecting two nodes on a network to communicate with each other. 
One socket(node) listens on a particular port at an IP, while the other socket reaches out to the other to form a connection. The server forms the listener socket while the client reaches out to the server. 

``` python
import socket
```

Initialise a socket
``` python
# in this case, s is a socket object
# socket is a method to create a socket
# AF_INET refers to the address-family ipv4.
# Alternatively AF_INET6 to the address-family ipv6
# The SOCK_STREAM means connection-oriented TCP protocol. 
s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
```

Find the IP of the server
``` python
try:
    host_ip = socket.gethostbyname('www.google.com')
except socket.gaierror:
 
    # this means could not resolve the host
    print ("there was an error resolving the host")
    sys.exit()
```

Socket for server:
A server has a bind() method which binds it to a specific IP and port so that it can listen to incoming requests on that IP and port.
A server has a listen() method which puts the server into listening mode. This allows the server to listen to incoming connections.
A server has an accept() and close() method. The accept method initiates a connection with the client and the close method closes the connection with the client. 
``` python
import socket

s = socket.socket()

# port number can be any, 8080 in this case
port = 8080

# Next bind to the port
# we have not typed any ip in the ip field
# instead we have inputted an empty string
# this makes the server listen to requests
# coming from other computers on the network
# if we passed a specific address, then it would have listened 
# to only those calls made within the local computer
# the address is basically a tuple
s.bind(('', port))

# put the socket into listening mode
# 5 means that 5 connections are kept waiting if the server is busy
# and if a 6th socket tries to connect then the connection is refused
s.listen(5)

# a forever loop until we interrupt it or
# an error occurs
while True:
 
# Establish connection with client.
  c, addr = s.accept()    
  print ('Got connection from', addr )
 
  # send a thank you message to the client. encoding to send byte type.
  c.send('Thank you for connecting'.encode())
 
  # Close the connection with the client
  c.close()
   
  # Breaking once connection closed
  break
```

# Python Program Testing and Debugging

## Linting and pylint
Linting is the automated checking of your source code for programmatic and stylistic errors.
This is done by using a lint tool (known as linter).

Pylint is a static code analyser for Python.

Pylint analyses your code without actually running it.
It checks for errors, enforces a coding standard, looks for code smells and can make suggestions about how the code could be refactored.

Install
`pip install pylint`

Run Pylint and check files
```$ pylint file.py```

## Verification and Validation

### Verification
Verification in a system life cycle context is a set of activities that compares a product of the system life cycle against the required characteristics for that product. This may include, but is not limited to, specified requirements, design description and the system itself.

System has been built right.

#### Verification Types
Static verification (known as linting)

Dynamic verification (known as testing)

Static verification is usually considered a more robust and reliable form of teseting.
However, in many cases we need to dynamically verify code too.

#### Static Verification
- (Linting) Style checking
- (Linting) Type checking
- (Linting) Logic checking. Includes anti-pattern detection and potential warnings
- key metric checking. Includes coupling and cyclomatic complexity
- formal verification
- informal reasoning

#### Dynamic Verification
- Verification performed during the execution of software
- Often known as the "test" phase
- Typically falls into one of three categories:
	- Testing in the small
	- Testing in the large
	- Acceptance tests

### Validation
Validation in a system life cycle context is a set of activities ensuring and gaining confidence that a system is able to accomplish its intended use, goals and objectives.

The right system has been built

## Unit Test
A unit test is a way of testing a unit - the smallest piece of code that can be logically isolated in a system.

``` python

```

## Property Based Test
- A method of testing where tests are defined as general properties (i.e. parameterised predicates)
- Test input is generated automatically by supplying a strategy for generating that input
- The testing framework runs the test many times to ensure the properties are true for each input
- In the event of a test failure, the framework will shrink the generated input to find the smallest value that still fails the test
- Property based testing was first introduced by QuickCheck framework in Haskell
- Hypothesis is the name of the property-based testing framework for Python

``` python

```

## System Test
System testing, also referred to as system-level tests or system-integration testing, is the process in which a quality assurance (QA) team evaluates how the various components of an application interact together in the full, integrated system or application.

System testing falls under Black box testing as it includes testing of the external working of the software.

System Testing includes the following steps:
1. Verification of input functions of the application to test whether it is producing the expected output or not.
2. Testing of integrated software by including external peripherals to check the interaction of various components with each other.
3. Testing of the whole system for End to End testing.
4. Behavior testing of the application via auser's experience

## Black box testing and White box testing

## Code Coverage
Test Coverage: a measure of how much of the feature set is covered with test (this is often left to human judgement)

Code Coverage: a measure of how much code is executed during testing (this can be computed and quantified)

### Checking code coverage
Run Coverage.py for your pytests:
```
coverage run --source=. -m pytest
```
View the coverage report:
```
coverage report
```
Generate HTML to see a breakdown (puts report in htmlcov/)
```
coverage html
```

### Branch Coverage Checking
- For lines that can potentially jump to more than one other line (e.g. if statements), check how many of the possible branches were taken during execution
- Can be done with the --branch option in Coverage.py
- Sometimes referred to as edge coverage

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

``` python
(a, b, c) = (1, 2, 3)
(a, b, c) = 1, 2, 3
a, b, c = (1, 2, 3)
a, b, c = 1, 2, 3
```

unpacking iterables
``` python
a, b, c = '123'
a, b, c = [1, 2, 3]
a, b, c = {'one': 1, 'two':2, 'three': 3}
a, b, c = (i ** 2 for i in range(3))
x, y, z = range(3)
a, b, c = {'a', 'b', 'c'}
first, *body, last = [1, 2, 3, 4]
```

unpacking with the * operator
``` python
*a, = 1, 2          # where a = [1, 2]
a, *b = 1, 2, 3     # where a = 1 and b = [2, 3]
*a, b = 1, 2, 3     # where a = [1, 2] and b = 3d
```

list comprehension
``` python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x for x in fruits if "a" in x]
print(newlist)

newlist = [x for x in range(10) if x < 5]
print(newlist)
```

# TODO
- code example for b tree
- hashTable
- breadth first search
- depth first search
- flask module
- pytest

# What I will update in the future
- mainly focus on algorithms including greedy algorithms and dynamic programming
- Python socket module for networking
- More on python testing and debugging
- Leetcode examples done by Python

# Acknowledgement
Some of the sources are from UNSW lecture notes.

Some are from online resources.
- [File Handling](https://www.programiz.com/python-programming/file-operation)
- [Object-Oriented Programming](https://www.pythontutorial.net/python-oop/)
- [Python Modules](https://docs.python.org/3/py-modindex.html)
- [Trie Strcture code example](https://towardsdatascience.com/implementing-a-trie-data-structure-in-python-in-less-than-100-lines-of-code-a877ea23c1a1)

# Disclaimer
The purpose of this notebook is to help people have some Python background knowledge, some of the contents are from lecture notes and some are from the Internect. If you don't want your work showing up in the notebook please contact me and I will delete them.

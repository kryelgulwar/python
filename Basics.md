# Basics of Python

## What is Python?

-   Python is a dynamically typed, general purpose programming language that supports an object-oriented programming approach as well as a functional programming approach.
-   Python is an interpreted and a high-level programming language.
-   It was created by Guido Van Rossum in 1989. 

## Features of Python

-   Python is simple and easy to understand.
-   It is Interpreted and platform-independent which makes debugging very easy.
-   Python is an open-source programming language.
-   Python provides very big library support. Some of the popular libraries include NumPy, Tensorflow, Selenium, OpenCV, etc.
-   It is possible to integrate other programming languages within python.

## Application of Python
Here are some key applications of Python:

-   Web Development: Frameworks like Django and Flask enable the building of dynamic websites.
-   Data Science: Used for data analysis, visualization, and machine learning with libraries like Pandas, NumPy, and TensorFlow.
-   Automation/Scripting: Python scripts can automate repetitive tasks and system operations.
-   Artificial Intelligence (AI) and Machine Learning (ML): Popular for developing AI/ML models due to its simplicity and rich libraries.
-   Game Development: Used for creating 2D/3D games (e.g., using Pygame).
-   Scientific Computing: Widely used in scientific research, simulations, and computations.
-   Cybersecurity: Employed for network scanning, automation of security tasks, and vulnerability testing.
-   Finance and Fintech: Used for stock market analysis, quantitative trading, and risk management.
-   Desktop Applications: GUI-based applications can be built using libraries like Tkinter and PyQt.
-   IoT: Python is used in IoT development for controlling devices and data processing.

Its versatility, extensive libraries, and ease of use make Python suitable for many industries.

# Modules and pip in Python!

Module is like a code library which can be used to borrow code written by somebody else in our python program. There are two types of modules in python:
1. Built in Modules - These modules are ready to import and use and ships with the python interpreter. there is no need to install such modules explicitly.
2. External Modules - These modules are imported from a third party file or can be installed using a package manager like pip or conda. Since this code is written by someone else, we can install different versions of a same module with time.

## The pip command

It can be used as a package manager [pip](https://pip.pypa.io/en/stable/) to install a python module.
Lets install a module called pandas using the following command

```bash
pip install pandas
```

## Using a module in Python (Usage)
We use the import syntax to import a module in Python. Here is an example code:

```python
import pandas

# Read and work with a file named 'words.csv'
df = pandas.read_csv('words.csv')
print(df) # This will display first few rows from the words.csv file
 
```

Similarly we can install other modules and look into their documentations for usage instructions.\
We will find ourselved doing this often in the later part of this course

# First Program

Today we will write our first ever python program from scratch. It will consist of a bunch of print statements.
print can be used to print something on the console in python

## Quick Quiz

Write a program to print a poem in Python. Choose the poem of your choice and publish your repl


```python
print("---Your poem here---")

```

Please make sure you attempt this. Might be easy for some of you but please finish each and every task

# Comments, Escape sequence & Print in Python

Welcome to Day 5 of 100DaysOfCode. Today we will talk about Comments, Escape Sequences and little bit more about print statement in Python.
We will also throw some light on Escape Sequences

# Python Comments
A comment is a part of the coding file that the programmer does not want to execute, rather the programmer uses it to either explain a block of code or to avoid the execution of a specific part of code while testing.

## Single-Line Comments:

To write a comment just add a ‘#’ at the start of the line.

### Example 1

```python
#This is a 'Single-Line Comment'
print("This is a print statement.")
``` 

Output:

```markup
This is a print statement. 
``` 

### Example 2

```python
print("Hello World !!!") #Printing Hello World
```

Output:

```markup
Hello World !!!
``` 

### Example 3:

```python
print("Python Program")
#print("Python Program")
``` 

### Output: 

```markup
Python Program
``` 
## Multi-Line Comments:

To write multi-line comments you can use ‘#’ at each line or you can use the multiline string.

**Example 1:** The use of ‘#’.

```python
#It will execute a block of code if a specified condition is true.
#If the condition is false then it will execute another block of code.
p = 7
if (p > 5):
    print("p is greater than 5.")
else:
    print("p is not greater than 5.")
```


Output:

```markup
p is greater than 5.
```


**Example 2:** The use of multiline string.

```python
"""This is an if-else statement.
It will execute a block of code if a specified condition is true.
If the condition is false then it will execute another block of code."""
p = 7
if (p > 5):
    print("p is greater than 5.")
else:
    print("p is not greater than 5.")
```


### Output

```markup
p is greater than 5.
```

# Escape Sequence Characters

To insert characters that cannot be directly used in a string, we use an escape sequence character.

An escape sequence character is a backslash  `\`  followed by the character you want to insert.

An example of a character that cannot be directly used in a string is a double quote inside a string that is surrounded by double quotes:

```python
print("This doesnt "execute")
print("This will \" execute")
```

# More on Print statement
The syntax of a print statement looks something like this:

```python
print(object(s), sep=separator, end=end, file=file, flush=flush)
```

## Other Parameters of Print Statement 
1. object(s): Any object, and as many as you like. Will be converted to string before printed
2. sep='separator': Specify how to separate the objects, if there is more than one. Default is ' '
3. end='end': Specify what to print at the end. Default is '\n' (line feed)
4. file: An object with a write method. Default is sys.stdout

Parameters 2 to 4 are optional

# Variables and Data Types
## What is a variable?
Variable is like a container that holds data. Very similar to how our containers in kitchen holds sugar, salt etc
Creating a variable is like creating a placeholder in memory and assigning it some value. In Python its as easy as writing:
```python
a = 1
b = True
c = "Harry"
d = None
```

These are four variables of different data types.

## What is a Data Type?
Data type specifies the type of value a variable holds. This is required in programming to do various operations without causing an error. \
In python, we can print the type of any operator using type function:
```python
a = 1
print(type(a))
b = "1"
print(type(b))
```
By default, python provides the following built-in data types:

## 1. Numeric data: int, float, complex


 - int: 3, -8, 0
 -    float: 7.349, -9.0, 0.0000001
 -  complex: 6 + 2i 

 ## 2. Text data: str
    

str: "Hello World!!!", "Python Programming"

## 3. Boolean data:
    

Boolean data consists of values True or False.

## 4. Sequenced data: list, tuple
    

**list:**  A list is an ordered collection of data with elements separated by a comma and enclosed within square brackets. Lists are mutable and can be modified after creation.

**Example:**

```python
list1 = [8, 2.3, [-4, 5], ["apple", "banana"]]
print(list1)
```


Output:

```markup
[8, 2.3, [-4, 5], ['apple', 'banana']]
```


**Tuple:**  A tuple is an ordered collection of data with elements separated by a comma and enclosed within parentheses. Tuples are immutable and can not be modified after creation. 

**Example:**

```python
tuple1 = (("parrot", "sparrow"), ("Lion", "Tiger"))
print(tuple1)
```


Output:

```python
(('parrot', 'sparrow'), ('Lion', 'Tiger'))
```


## 5. Mapped data: dict
    

**dict:** A dictionary is an unordered collection of data containing a key:value pair. The key:value pairs are enclosed within curly brackets.

**Example:**

```python
dict1 = {"name":"Sakshi", "age":20, "canVote":True}
print(dict1)
```


Output:

```python
{'name': 'Sakshi', 'age': 20, 'canVote': True}
```

# Operators
Python has different types of operators for different operations. To create a calculator we require arithmetic operators.
# Arithmetic operators


|   Operator             |Operator Name                          |Example                         |
|----------------|-------------------------------|-----------------------------|
|+|`Addition`            |``` 15+7 ```            |
|-|`Subtraction`            |``` 15-7 ```            |
|*|`Multiplication`            |``` 5*7 ```            |
|**|`Exponential`            |``` 5**3 ```            |
|/|`Division`            |``` 5/3 ```            |
|%|`Modulus`            |``` 15%7 ```            |
|//|`Floor Division`            |``` 15//7 ```            |

# Exercise
```python
n = 15
m = 7
ans1 = n+m
print("Addition of",n,"and",m,"is", ans1)
ans2 = n-m
print("Subtraction of",n,"and",m,"is", ans2)
ans3 = n*m
print("Multiplication of",n,"and",m,"is", ans3)
ans4 = n/m
print("Division of",n,"and",m,"is", ans4)
ans5 = n%m
print("Modulus of",n,"and",m,"is", ans5)
ans6 = n//m
print("Floor Division of",n,"and",m,"is", ans6)
```
# Explaination
Here 'n' and 'm' are two variables in which the integer value is being stored. Variables 'ans1' , 'ans2' ,'ans3', 'ans4','ans5' and 'ans6' contains the outputs corresponding to addition, subtraction,multiplication, division, modulus and floor division respectively.

# Typecasting in python
The conversion of one data type into the other data type is known as type casting in python or type conversion in python.

Python supports a wide variety of functions or methods like: int(), float(), str(), ord(), hex(), oct(), tuple(), set(), list(), dict(), etc. for the type casting in python.


## Two Types of Typecasting:

1. Explicit Conversion (Explicit type casting in python)
2. Implicit Conversion (Implicit type casting in python).
### Explicit typecasting:
The conversion of one data type into another data type, done via developer or programmer's intervention or manually as per the requirement, is known as explicit type conversion. 

It can be achieved with the help of Python’s built-in type conversion functions such as int(), float(), hex(), oct(), str(), etc .
### Example of explicit typecasting:
```python
string = "15"
number = 7
string_number = int(string) #throws an error if the string is not a valid integer
sum= number + string_number
print("The Sum of both the numbers is: ", sum)
```
### Output:
```
The Sum of both the numbers is 22
```
### Implicit type casting:
Data types in Python do not have the same level i.e. ordering of data types is not the same in Python. Some of the data types have higher-order, and some have lower order. While performing any operations on variables with different data types in Python, one of the variable's data types will be changed to the higher data type. According to the level, one data type is converted into other by the Python interpreter itself (automatically). This is called, implicit typecasting in python.

Python converts a smaller data type to a higher data type to prevent data loss.
### Example of implicit type casting:
```python
# Python automatically converts
# a to int
a = 7
print(type(a))
 
# Python automatically converts b to float
b = 3.0
print(type(b))
 
# Python automatically converts c to float as it is a float addition
c = a + b
print(c)
print(type(c))
```
### Ouput:
```
<class 'int'>
<class 'float'>
10.0
<class 'float'>
```
# Taking User Input in python
In python, we can take user input directly by using input() function.This input function gives a return value as string/character hence we have to pass that into a variable
## Syntax:
```python
variable=input()
```
But input function returns the value as string. Hence we have to typecast them whenever required to another datatype.
## Example:
```python
variable=int(input())
variable=float(input())
```

We can also display a text using input function. This will make input() function take user input and display a message as well
## Example:
```python
a=input("Enter the name: ")
print(a)
```
## Output:
```
Enter the name: Harry
Harry
```
# Conditional (if-else) Statements
Sometimes the programmer needs to check the evaluation of certain expression(s), whether the expression(s) evaluate to True or False. If the expression evaluates to False, then the program execution follows a different path than it would have if the expression had evaluated to True.

Based on this, the conditional statements are further classified into following types:
- if
- if-else
- if-else-elif
- nested if-else-elif.
## An if……else statement evaluates like this:

### if the expression evaluates True:
Execute the block of code inside if statement. After execution return to the code out of the if……else block.\
### if the expression evaluates False:
Execute the block of code inside else statement. After execution return to the code out of the if……else block.
 ## Example:
```python
applePrice = 210
budget = 200
if (applePrice <= budget):
    print("Alexa, add 1 kg Apples to the cart.")
else:
    print("Alexa, do not add Apples to the cart.")
```
## Output:
```
Alexa, do not add Apples to the cart.
```
# elif Statements
Sometimes, the programmer may want to evaluate more than one condition, this can be done using an elif statement.
### Working of an elif statement
Execute the block of code inside if statement if the initial expression evaluates to True. After execution return to the code out of the if block.

Execute the block of code inside the first elif statement if the expression inside it evaluates True. After execution return to the code out of the if block.

Execute the block of code inside the second elif statement if the expression inside it evaluates True. After execution return to the code out of the if block.\
.\
.\
.\
Execute the block of code inside the nth elif statement if the expression inside it evaluates True. After execution return to the code out of the if block.

Execute the block of code inside else statement if none of the expression evaluates to True. After execution return to the code out of the if block.

## Example:
```python
num = 0
if (num < 0):
    print("Number is negative.")
elif (num == 0):
    print("Number is Zero.")
else:
    print("Number is positive.")
```
## Output:
```
Number is Zero.
```

# Nested if statements
We can use if, if-else, elif statements inside other if statements as well. \
Example:
```python
num = 18
if (num < 0):
    print("Number is negative.")
elif (num > 0):
    if (num <= 10):
        print("Number is between 1-10")
    elif (num > 10 and num <= 20):
        print("Number is between 11-20")
    else:
        print("Number is greater than 20")
else:
    print("Number is zero")
```
Output:
```
Number is between 11-20
```
# Match Case Statements
To implement switch-case like characteristics very similar to if-else functionality, we use a match case in python. If you are coming from a C, C++ or Java like language, you must have heard of switch-case statements. If this is your first language, dont worry as I will tell you everything you need to know about match case statements in this video!

A match statement will compare a given variable’s value to different shapes, also referred to as the pattern. The main idea is to keep on comparing the variable with all the present patterns until it fits into one.

The match case consists of three main entities :

1. The match keyword
2. One or more case clauses
3. Expression for each case

The case clause consists of a pattern to be matched to the variable, a condition to be evaluated if the pattern matches, and a set of statements to be executed if the pattern matches.
## Syntax:
```python
match variable_name:
            case ‘pattern1’ : //statement1
            case ‘pattern2’ : //statement2
            …            
            case ‘pattern n’ : //statement n
```
### Example:
```python
x = 4
# x is the variable to match
match x:
    # if x is 0
    case 0:
        print("x is zero")
    # case with if-condition
    case 4 if x % 2 == 0:
        print("x % 2 == 0 and case is 4")
    # Empty case with if-condition
    case _ if x < 10:
        print("x is < 10")
    # default case(will only be matched if the above cases were not matched)
    # so it is basically just an else:
    case _:
        print(x)
```
### Output:
```
x % 2 == 0 and case is 4
```

# Introduction to Loops
Sometimes a programmer wants to execute a group of statements a certain number of times. This can be done using loops. Based on this loops are further classified into following main types; 
- for loop
- while loop 
# The for Loop
for loops can iterate over a sequence of iterable objects in python. Iterating over a sequence is nothing but iterating over strings, lists, tuples, sets and dictionaries.

## Example: iterating over a string:

```python 
name = 'Abhishek'
for i in name:
    print(i, end=", ")
```
## Output:

A, b, h, i, s, h, e, k,
 

## Example: iterating over a list:

``` python 
colors = ["Red", "Green", "Blue", "Yellow"]
for x in colors:
    print(x)
```
## Output:

Red\
Green\
Blue\
Yellow

Similarly, we can use loops for lists, sets and dictionaries.
## range():
What if we do not want to iterate over a sequence? What if we want to use for loop for a specific number of times?

Here, we can use the range() function.

## Example:
```python
for k in range(5):
    print(k)
```
## Output:

0\
1\
2\
3\
4\
Here, we can see that the loop starts from 0 by default and increments at each iteration.

 

But we can also loop over a specific range.

## Example:
```python
for k in range(4,9):
    print(k)
```
## Output:

4\
5\
6\
7\
8

## Quick Quiz
Explore about third parameter of range (ie range(x, y, z))

# Python while Loop
As the name suggests, while loops execute statements while the condition is True. As soon as the condition becomes False, the interpreter comes out of the while loop. 
## Example:

```python 
count = 5
while (count > 0):
  print(count)
  count = count - 1
```
## Output:
```
5
4
3
2
1
```

Here, the count variable is set to 5 which decrements after each iteration. Depending upon the while loop condition, we need to either increment or decrement the counter variable (the variable count, in our case) or the loop will continue forever.

# Else with While Loop
We can even use the else statement with the while loop. Essentially what the else statement does is that as soon as the while loop condition becomes False, the interpreter comes out of the while loop and the else statement is executed. 

## Example:

```python 
x = 5
while (x > 0):
    print(x)
    x = x - 1
else:
    print('counter is 0')
```
## Output:
```
5
4
3
2
1
counter is 0
```

# Do-While loop in python
do..while is a loop in which a set of instructions will execute at least once (irrespective of the condition) and then the repetition of loop's body will depend on the condition passed at the end of the while loop. It is also known as an exit-controlled loop.
# How to emulate do while loop in python?
To create a do while loop in Python, you need to modify the while loop a bit in order to get similar behavior to a do while loop.

The most common technique to emulate a do-while loop in Python is to use an infinite while loop with a break statement wrapped in an if statement that checks a given condition and breaks the iteration if that condition becomes true:
## Example
```python 
while True:
  number = int(input("Enter a positive number: "))
  print(number)
  if not number > 0:
    break
```
## Output
```
Enter a positive number: 1
1
Enter a positive number: 4
4
Enter a positive number: -1
-1
```
## Explanation
This loop uses True as its formal condition. This trick turns the loop into an infinite loop. Before the conditional statement, the loop runs all the required processing and updates the breaking condition. If this condition evaluates to true, then the break statement breaks out of the loop, and the program execution continues its normal path.

# break statement
The break statement enables a program to skip over a part of the code. A break statement terminates the very loop it lies within.
## example

```python '
for i in range(1,101,1):
    print(i ,end=" ")
    if(i==50):
        break
    else:
        print("Mississippi")
print("Thank you")
```
### output
```
1 Mississippi
2 Mississippi
3 Mississippi
4 Mississippi
5 Mississippi
.
.
.
50 Mississippi
```

## Continue Statement
The continue statement skips the rest of the loop statements and causes the next iteration to occur.
## example
```python
for i in [2,3,4,6,8,0]:
    if (i%2!=0):
        continue
    print(i)
  ```
  ## output
  ```
2
4
6
8
0

```

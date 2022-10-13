# 1 Introduction

## Why Programming?

- Computers can help humans solve problems with some programming
- We can take advantage of computer elements such as processing unit, memory and others to help run our programs
- Computers take instructions literally and can get easily confused, so we need to precise and accurate with them
- Building programs/applications for solve problems for our selves or others.
- While take a lot of practice for building applications for others

## Hardware Architecture

- Major parts of computer:
- Central processing unit: 3 billon per sec request processing, does all thinking. Very dumb but super fast brain
- Main Memory (RAM): Really fast, memory feeds for instructions for CPU to process. Losses data after loss of power
- Secondary storage (HDD, SDD): To store program/data files. Permanent store
- Input Devices: Keyboard, Mouse, Touch screens to input data into computers
- Output Devices: Screen, Speakers, Printers that can share the result in required format to users
- Mother board: for older computers place to connect all relevant components
- Our python code lives in main memory while executing which processed by CPU
- Our code to translated into machine language, by python source code, which contains 1's and 0's

## Python as a Language

- Python, invited by Guido Van Rossum
- Python named after Monty Python's Flying Circus
- Syntax Errors: When python fails to interpret our code

### Interactive mode of python:

- Enter python3 into terminal
- Now python is ready to accept instructions after the chevron(>>>)

### Elements of Python

- Variables: characters or words we can assign values as part of our instructions.
- Reserved Words: Python source code has certain keywords that uses to process any instruction we give.
- Statements (Lines of Code): Sentences with collection of variable, operators and/or reserved words which makes a complete understandable instruction to python. Examples: assignment statement(x = 1), reserve word statement (print(x))
- Programs/Scripts: Enter a collection of statements into a file and asking python to execute them.
- Program Flows: Similar to assemble instructions, programs need to flow a sequence to solve problems. Understanding these flows and build better flows will resulting better solutions for the problems.
- Sequential Flow: Programs executes the statements in a certain given order

```
 x = 2
 print(x)
 x = x + 2
 print(x)
```

- Conditional Flow: Programs execute certain statements only when a specified condition is met. Like below code will print different text based on the condition if its less then 10 then 'small', if greater then 20 then 'large' and completes the program by printing finish

```
  x = 5
  if x < 10:
    print('small')
  if x > 20:
    print('large')
  print('finish')
```

- Repeated Flow: Program execute certain statements in a loop till the mentioned criteria is met. As mentioned in below code if `n` is greater than zero we keep on subtracting one till it becomes zero and completes the program by printing `Blast Off!!!`

```
  n = 5
  while n > 0:
    print(n)
    n = n - 1
  print('Blast Off!!!')
```

# 2 Variables, Expressions, and Statements

## Variables

### Constants

    - Fixed values which have their values remain the same through the program.
    - Constants can be numeric (1,2,3) and string with ' or " quotes('Hello World')
    - Reserved words are constants too!

- Named place in memory that programmers can use to store any data and get it back by calling the name
- Variables can only store 1 value and can altered at later stages
- Variable names must start with letter or _, although `_` is not recommended
- Variable names are case sensitive and can have letters, numbers and `_`
- Variable names should be meaning full as per the data getting stored in it.

## DataTypes

- Variables can store different types of data in them, data types help python differentiate between them for its operations. In the following example we can say that python can use `+` for both addition and string concatenation, but when used for operation with string and integer returns `TypeError`.

```
  x = 2 + 3
  print(x) // result 5
  t = 'hello ' + 'world'
  print(t) // result 'hello world'
  z = 2 + 'word'
  Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
  TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

- Python has the following data types built-in by default, in these categories:
  - Text Type: `str`
  - Numeric Types: `int`, `float`, `complex`
  - Sequence Types: `list`, `tuple`, `range`
  - Mapping Type: `dict`
  - Set Types: `set`, `frozenset`
  - Boolean Type: `bool`
  - Binary Types: `bytes`, `bytearray`, `memoryview`
  - None Type: `NoneType`

### Querying data types

- We can ask python for the data type using thee `type()` function

```
  print(type(5)) // result <class 'int'>
  print(type('hello')) // result <class 'str'>
  print(type(20.5)) // result <class 'float'>
```

### Setting data types

- We can also set a specific data type if required using the datatype reserved keyword as below:

```
  x = str('hello world')
  y = int(20)
```

### Converting data types

- We can convert one data type into another by using above setting logic, but not all can be converted into every other type for example python will through an error when converting string to an integer but we can convert an integer into float or string.

```
  z = int('hello world')
  Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
  ValueError: invalid literal for int() with base 10: 'hello world'

  w = str(10)
  print(w) // result '10'
  print(type(w)) // result <class 'str'>

  v = float(10)
  print(v) // result 10.0
  print(type(v)) // result <class 'float'>
```

- Integer division will return a float result which can be termed as conversion too

## Operators and Operands
- Operators are special symbols that represent computations like addition and multiplication. The values the operator is applied to are called operands
- Python divides the operators in the following groups:
  - Arithmetic operators
  - Assignment operators
  - Comparison operators
  - Logical operators
  - Identity operators
  - Membership operators
  - Bitwise operators
- _**Note:** Python Operators details can be found [here](https://www.w3schools.com/python/python_operators.asp)_
- Python has the following precedence order for arithmetic operators, **PEMDAS**:
  - Parenthesis
  - Exponentiation
  - Multiplication,
  - Division/Reminder
  - Addition
  - Subtraction

## Expressions

- An expression is a combination of values, variables, and operators. A value all by itself is considered an expression, and so is a variable

## Statements
- A statement is a unit of code that the Python interpreter can execute.

## Comments
- Due to nature of the problems we try to address the programs can get large and complex, so in order increase the readability of the code programmers introduced comments.
- Comments are notes of whats the code is doing or code that we are asking python to ignore.
- Single line comments state with `#` and multi line comments are surrounded with ` ``` `

# 3 Conditional Execution

## Indentation
- For any conditional execution we need to give an extra indent for blocks of code to indicate the scope. Its the way interprets the code to be executed for specified condition.
- If not indented properly python will raise `IndentationError`
- 4 spaces is marked as a intend
- No tabs != 4 spaces

## If Statement
- Python uses the comparison operators to verify if the given conditions is met which then prints the block of code in that section. Example:

```
  x = input('Enter the number: ')
  if x == 5:
    print('The number is 5')
  if x < 5:
    print('The number is less than 5')
  if x > 5:
    print('The number is greater than 5')
  print('Complete!')
```

- If statements also provide option of make two decisions using `if else` statements. Python can check for a condition and verify if its satisfied then execute one block of code else execute another.

```
  x = input('Enter the number: ')
  if x%2 == 0:
    print('The number is divisible by 2')
  else:
    print('The number is not divisible by 2')
  print('Complete!')
```

## Nested If Statement
- Programmers can check multiple conditions using nested if statement, if in another if. Example:

```
  x = input('Enter the number: ')
  if x%2 == 0:
    print('The number is divisible by 2)
    if x%5 == 0:
      print('The number is also divisible by 5)
  print('Complete!')
```

## Multi-way If Statement
- In the multiple conditions statements, unlike nested if, we may need to verify multiple conditions in such a way that we verify others only if earlier one is false.
- These Multi-way If statements use `if elif else` statements. Example:

```
  x = input('Enter the number: ')
  if x == 5:
    print('The number is 5')
  elif x < 5:
    print('The number is less than 5')
  elise:
    print('The number is greater than 5')
  print('Complete!')
```

## Try and Except Statement
- For any block of code that may raise errors based on user input's or other reasons, can be added under the `Try` block. So that python can try to execute that and if no errors happen we can move forward with our logic.
- `Except` block is used to handle the errors, like in above step we asked python to try and execute a block of code. If an error occurs then that can be handled in except block. Some ways to handle errors can be like give out a more understandable error message or execute a different block of code.
- Example:

```
  try:
    x = 'Hello World' + 1
    print('Text is: ', x)
  except:
    print('Try block failed!!!')
  try:
    x = 'Hello World' + 'John Doe'
    print('Text is: ', x)
  except:
    print('Try block failed!!!')
```

# 4 Functions
- Functions are blocks are of that are perform a task/block of code when invoked/called. This is improves the reusability of the code
## Built in functions
- Built in functions are the reserved keywords that are in python
## User defined functions
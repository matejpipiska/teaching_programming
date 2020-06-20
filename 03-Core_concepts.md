# Core concepts in programming

In this section, we will talk about some core concepts that are present in pretty much every programming language. These are generally covering inputs and outputs of data and various features for controlling the flow of the program.

## Inputs/outputs
Anything coming in our out of a program/computer :) Sometime abbreviated IO, I/O, io, etc.

There is something called standard input and standard output, which generally refers to what you see put in and read from your terminal window.

- **keyboard/screen**
    - `raw_input()`/`print()`
    - `name = raw_input("What is your name? ")`
    - `print("Hello " + name)`
    - NOTE - in python3 it is just `input()`
- **files**
    - we need to open a file to get a file handler. Then we can do `read()` and `write()`
    - `f = open('test_file')`
    - `data = f.read()`
    - ```python
      for line in f:
          print(line)
      f.close()
      ```
    - ```python
      f = open('test_file', 'w')
      f.write('35')
      f.close()
      ```
- drives
- network

## Variables (assignment, various types, None)
Variable is our 'temporary' storage within the program. In Python, we can assign values in variables as:
`<name of variable> = <value of variable>`

- Variables are used to store values, or send them to different parts of the program
- Each variable has some type, that we can find out through `type(variable)`. The type of variable specifies what we can do with it.
- Most used variable types:
    - boolean (true/false, 0/1)
    - int/float (numbers)
    - string
    - list
    - dictionary
    - tuple
    - `None`

Examples:
```python
a = true # boolean
a = false

x = 3 # integer
x = 4.5 # float

s = "Hello!" # string
s = 'Hello!' # also a string :)

l = [3, 5, 7] # a list! - of integers
l = ["John", "Mary", "Peter"] # also a list - of strings

d = {"John": 35, "Mary": 24, "Peter": 77} # dictionary
d_d = {"people": {
            "John": 35,
            "Mary": 24,
            "Peter": 77},
       "animals": {
            "cow": 4,
            "dog": 5,
            "duck": 3
       } # A dictionary of dictionaries :)

t = ('abc', 'def') # tuple

n = None
```

## Statements (conditionals) and branching
Since our program probably needs to decide on something, at some point of time, we need our means to give it some basic logic. Those are often so called `if` statements. They have a word `if` followed by some statement, which turns to be either `true` or `false`. If it is `true`, the part of the code in the following **code block** gets executed. Otherwise it is ignored. Additionally, we can add `else` or `else if` statements to better control the code.

Example:
```python
age = raw_input("How old are you? ")
age = int(text)

if age < 18:
    print("You are very young!")
else if age < 35:
    print("You're in your best age!")
else:
    print("It's only gonna get worse xD. Just kidding. Hang in there!")
```

## Loops
Loops allow us to 'loop' through a piece of code, as many times as necessary. We either have some condition that needs to be met, until we 'exit' the loop, or we have a list of values that we can iterate over.

We recognize `for` and `while` loops, mainly.

For loop allows us to loop over certain set of data. For instance over lists or dictionaries.

```python
ages = [13, 20, 27] # list of ages
total_age = 0 # we empty the variable

for age in ages: # here we iterate over every number in the ages list
    total_age = total_age + age # we add every age value to our total_age

print("The total age is: ", int(total_age)) # once finished, we print out the result :)
```

## Functions
Functions help us 'wrap' a piece of code and only provide those variables that change its behaviour. Additionally they can help us work with code as 'modules' or building blocks, without needing to worry how they operate.

For instance, we could create a function that adds 2 numbers for us, and then we do not need to worry about it again. We could call it e.g. `add(x, y)`.

Or for instance, it could be even simplier, like adding a function that executes `print("---")` as our 'line separator'. Then we use this function across the program. If we ever happen to need to change the separator to something else, we can simply modify this one function, instead of having to go through the whole code and change it everywhere.

The functions have generally the following format:
```
def <name of function>(<comma separated parameters>):
    command1
    command2
    command3
    ...
    commandX

```
The code in the function is a 'code block' and needs to be indented (shifted 4 characters to the right)

If the function is supposed to give something back for further processing, it does so using `return` statement.

Let's show an example of a function that adds 2 numbers.

```python
def add(x, y):
    return x + y
```

To call this function, we could use:
```python
print(add(3, 7))

# we can also store the result in a variable and use it further in the code
result = add(10, 15)
print(result)
```

## Error handling
Another aspect that allows us to control the flow of a program is related to handling errors. Normally, if an error happens, a program would 'crash' and stop. This would mean we'd need to re-start it and everything has to be re-loaded again.

This is why a concept of error handling and 'expecting' of errors was introduced. This comes with a whole ecosystem for 'raising' errors and handling errors that we 'expect'. Many default libraries come with various exceptions that we can handle out of the box. Of course, any unexpected exception will still halt the program execution, and should then be implemented in the program.

In Python, we designate a `try:` block of code, that could potentially raise eceptions. Then anything inside that block, if exception is encountered, will be handled by the following `except:` block.

```python
try:
    ...
except:
    ...
```

In practice, it looks something like this:


```python
try:
    a = 10 / 0
except ZeroDivisionError:
    print("Something went wrong, but the program continues!")
```

This way, instead of the ugly error from Python, we 'handle' the exception and continue in program execution.

This can for instance be useful when loading a big amount of data, where some of it could be malformed, or e.g. trying to open a file and the file does not exist, so we ask the user again.

And since this is a programming language, we can make our own exceptions, too.

To create (and raise) an exception, we use the `raise` command.

E.g.

```python
def division(x, y):
    if y == 0:
        raise ValueError("We do not support division by 0!")
    return x / y

try:
    division(3, 0)
except ValueError:
    print("Maybe we should try again with a non-zero value")
```

Of course, this example is silly, as we could just try to divide as is, and catch the ZeroDivisionError directly.

Some documentation and examples can be found [here](https://docs.python.org/3/tutorial/errors.html)

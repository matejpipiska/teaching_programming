# Core concepts in programming

In this section, we will talk about some core concepts that are present in pretty much every programming language. These are generally covering inputs and outputs of data and various features for controlling the flow of the program.

## Inputs/outputs
Anything coming in our out of a program/computer :) Sometime abbreviated IO, I/O, io, etc.

There is something called standard input and standard output, which generally refers to what you see put in and read from your terminal window.

- **keyboard/screen**
    - `input_raw()`/`print()`
    - `name = input_raw("What is your name? ")`
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
age = read("How old are you? ")
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

```
def <name of function>(<parameters>):
    ...
    commands
```

- Functions (grouping and reusing of code)
- Error handling

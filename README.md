# Learning to Program using Python

This lesson set is supposed to help an individual learn basic concepts of programming. There are no prerequisites or prior knowledge necessary. The inspiration for the topics and some ordering is taken from "Learning to program using Python" by Cody Jackson.

These documents are mostly supposed to serve as a guideline of topics to be covered, for now, although they might be expanded in the future to cover more detail.

## Agenda

### [What is programming?](./01-Programming.md)
- An intro to programming theory.
- What is programming and why?
- What kinds of languages and programs do we know?
- How do they differ?
- Why did we pick Python?

### [How do we use Python?](./02-Using_python.md)
- A bit more practical.
- Setting up development environment.
- Setting up IDE.
- Trying Python Command Line interpreter
- Trying to write and run a program

### [Core concepts in programming](./03-Core_concepts.md)
- Input/output
- Variables (assignment, various types, None)
- Statements (conditionals) and branching
- Loops
- Functions (grouping and reusing of code)
- Error handling

### Functions and making code
- def keyword
- Gives value back via return
- Do nothing placeholder - pass
- If no return, defaults to None
- Parameters = input variables
- Just the same code :)
- Some default functions! print(), len()...
- How to know what you can call? x.stuff(). Dir(x)

### Types - Numbers
- Recap about strict and dynamic typing
- Different number types are represented (integer, float, hex, complex, binary, etc)
- Functions and operators related to them and where to find them
- Converting between types

### Types - Strings
- empty string
- single and double quotes and combining them
- 'triple quoted block'
- concatenate 2 strings (a + b)
- repeat string (a * 3)
- index in string (a[3]) (also how indexes work, negatives, substrings, etc)
- length of string (len(a))
- string formatting (deprecated '%' % a; '{}'.format(a); f'{a}')
- iterate over characters in a string (for char in a)
- membership ('x' in a)


### Types - Lists
- What are they and why are they useful? An array of 'items'. Sorted. Indexed.
- Empty list (how to create a new list)
- Length of list
- Adding and removing from lists
- Index number in list (starts with 0)
- Iterating over lists
- Joining lists, append, sort, index, reverse
- String is a list of characters :)
- List inside list (a=[3, [1,2]]; a[1][0])
- Auto generating a list using range/xrange
- Set vs list

### Types - Dictionaries
- What are they and why are they useful? Mapping of something to something else. Key-value store. Not sorted.
- Empty dictionary
- Two item dict
- Nested dict
- Indexing by key (and nested indexing)
- '{}.has_key(x)', 'x' in {}, {}.get('x')
- {}.keys(), {}.values()
- {}[key] (adding), del {}[key]

### Tuples
- WTF are tuples
- Packing, unpacking

### Files
- Files! We need to read and write, sometime
- open(), open(file, access_mode)
- Reading from file - iterating over file
- Writing in file
- Creating a file
- 'with open() as f:'...
- Exceptions (try/except)

### Statements
- assignment
- print (python2)
- print()
- if/elif/else
- for
- while
- pass
- break/continue
- try/except/finally
- raise
- import
- def, return
- class

### Documenting code like a boss



### Exceptions

### Object Oriented Programming

### Testing your code

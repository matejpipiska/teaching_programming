# Functions and making code

## Intro
This chapter will talk a bit about why and how we group code into functions. Functions can be understood as groups of code that do not change and only require a few 'varible' parts to execute, while giving us back a desired result.

Functions are often used when we start duplicating same snippets of code, or when we want to group pieces of code that deliver some functionality or purpose.

Let's show an example...
Let's say we want to greet several people. We make a simple list of prints to do so:

```python
# we can greet everyone through writing down individual prints

print("Hi Alice!")
print("Hi Bob!")
print("Hi Charlie!")
```
This is cool. But what if we want to also print a polite "How are you" with it? We add the extra prints:

```python

# this will start getting a bit messy, when we start adding more code that uses the same names... e.g.

print("Hi Alice!")
print("How are you, Alice?")

print("Hi Bob!")
print("How are you, Bob?")

print("Hi Charlie!")
print("How are you, Charlie?")
```

We had to add 3 new lines of prints to ask everyone how they are doing. Outrageous.

But we realized that "Hi" is perhaps a bit too informal and we want to change the greeting to "Hello". We'll have to go to every print and modify it, to reflect the behaviour:

```python

# so if we want to say "Hello ..." instead of "Hi ..." we'd have to do something like..

print("Hello Alice!")
print("How are you, Alice?")

print("Hello Bob!")
print("How are you, Bob?")

print("Hello Charlie!")
print("How are you, Charlie?")
```

There surely must be a better way to do this! We are lazy programmers and do not want to do this al the time. Additionally, this makes it -so- easy to make a mistake. Mainly if we were modifying not 3, but a 100 names and greetings.

## Defining functions

We can **def**ine functions through the **def** keyword. The name of the function is lowercase and uses underscores if necessary. The code that belongs to the function is indented (it is shifted 2-4 blank characters to the right). A simple code with functions would look like something like this:

```python
def name_of_function():
    command1_in_function_1
    command2_in_function_1
    ...
    commandX_in_function_1

def name_of_function2():
    command1_in_function_2
    command2_in_function_2
    ...
    commandX_in_function_2

rest_of_code_that_is_not_a_part_of_the_function_anymore

# we can call the function
name_of_function()

name_of_function2()
```

### Code blocks

We mention indentation of code, or so called code blocks. Usually, in a flow of code, there are some logically separated sections of code. Imagine an *if* statement.

**TO BE CONTINUED**


- Gives value back via return
- Do nothing placeholder - pass
- If no return, defaults to None
- Parameters = input variables; namespaces
- Just the same code :)
- Some default functions! print(), len()...
- How to know what you can call? x.stuff(). Dir(x)
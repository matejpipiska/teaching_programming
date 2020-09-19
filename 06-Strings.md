# Types - Strings

Strings are the type of variables related to text. It is a 'string' of individual characters. In other languages, there is often a 'type' of variable related directly to a single character (char) and a separate one related to several characters (string or str). In python there is no char type and there is only string type. A single character is then a string of 1 character.

Strings, as any other types have a set of functions we can apply to them, but we will get to them later.

## Initiating a string

If we wish to create an empty string variable, we can do so in multiple ways. All of these produce an empty string.

```python
>>> a = ''
>>> b = ""
>>> c = str()
>>> a
''
>>> b
''
>>> c
''
```

Why would you want to create an empty string? Usually, you don't. But it is good to know, as there might be cases when it can be useful :)

## Single and double quotes and combining them

When assigning a string, you must have noticed it is ok to use single quotes and double quotes. It usually looks strange if you use both in the same code, so pick one and stick to it. Some style guides lead you to using one. For instance, [Google's Python Black tool uses double quotes everywhere](https://black.readthedocs.io/en/stable/the_black_code_style.html#strings).

Why do we have two ways, anyway? Sometime, you might want to create a string that contains quotes. And Python allows you to use 'outside' quotes to mark the string, and inside quotes can be then the other ones. So if you want to create a string that contains `"` or `'`, you can do so, and put the other type of string around it.

```python
>>> 'he said: "blah!"'
'he said: "blah!"'
>>> "she said: 'blah!'"
"she said: 'blah!'"
```

At this point, I am sure you're asking, but what happens if we want to use **both** quotes inside a string? A great question! Let's say we want a sentence: `They he said: "That's incredible!"`. Have a look at what happens:

```python
# we try to put the string in single or double quotes... But no success.
# Python is not happy with it. Note that we use both single and double
# quotes in the string (and that's what's breaking it. Python thinks 
# we're ending the string too soon)
>>> a = "They he said: "That's incredible!""
  File "<stdin>", line 1
    a = "They he said: "That's incredible!""
                           ^
SyntaxError: invalid syntax
>>> a = 'They he said: "That's incredible!"'
  File "<stdin>", line 1
    a = 'They he said: "That's incredible!"'
                             ^
SyntaxError: invalid syntax
```

So what can we do? This is a common problem in all of the computer science, not just in programming. Usually, there is a way to 'escape' the characters that would normally be considered 'control' characters. In our case, the control character is `"`. It 'controls' the program, telling it this is a beginning of the string, and also it controls at the end the end of the string. If we want to have it in the middle, we have to 'escape' it. We do so by adding a `\` in front of it. This can start looking quite funky for some complicated strings. But there's time for that later.

Let's see what would this look with escape characters!

```python
>>> a = "They he said: \"That's incredible!\""
>>> a
'They he said: "That\'s incredible!"'
# we can see internally python converts it into a string that is wrapped in single quotes

>>> b = 'They he said: "That\'s incredible!"'
>>> b
'They he said: "That\'s incredible!"'
# both ways work :)
```

## Triple quoted block

Sometime we want a way longer block of text to be stored or a part of string. For instance, we want a multi-line block of text, formatted, with new lines. In the previous section we mentioned so called 'escaped' characters. Escaping can be used to print characters that'd be difficult to do. Such as new lines (`\n`), or 'tab' (`\t`) keys. So let's say we want to create a block of text which looks like this.

```
Line1
Line2
Line3
```

One way, using the `\n` for new lines:
```python
>>> a = 'Line1\nLine2\nLine3'
>>> a
'Line1\nLine2\nLine3' # We can see the formatting characters are stored
>>> print(a) # when we print, they are represented properly on our screen
Line1
Line2
Line3
```

This could become somewhat clunky, if we had way more text and would need to remember where the `\n` is and such. This is where the concept of triple quotes (`"""` or `'''`) comes into play.

```python
>>> b = """
... Line 1
... Line 2
... Line 3
... """
>>> b
'\nLine 1\nLine 2\nLine 3\n' # Every new line after the """ becomes  represented by `\n`
>>> print(b)

Line 1
Line 2
Line 3

```

Triple quotes are sometime used also as so called docstrings which serve as strings at the beginning of e.g. functions to document the functionality of the function. It helps a lot when looking at a new code or returning to a code we have not seen for a while. Let's illustrate an example of a simple function and a function that takes 2 arguments and returns a result.

```python
def hello():
    """Print hello world."""
    print("Hello world!")

def sum(x, y):
    """Return a sum of two numbers.

    A helper function that takes 2 numbers and returns their sum.
    Can also be used with non-ints but internally we'll be
    only passing ints to it.

    Args:
        x(int): first number to sum
        y(int): second number to sum

    Returns:
        (int): sum of two numbers
    """
    return x + y

```

## Concatenate 2 strings (a + b)

The title says it. We can take 2 strings and connect them with a `+` symbol.

```python
>>> a = "abc" + "def" + "geh" + "ijk"
>>> a
'abcdefgehijk'

>>> b = "Hello "
>>> print(b + "world!")
Hello world!
```

## Repeat string (a * 3)

We can repeat same string several times. I have not seen this much in use, other than when doing some formatting or as status indicators.

```python
>>> print("!" * 10)
!!!!!!!!!!

# we can of course do multiple operations. As in math, multiplication
# takes precedence
>>> print("!" * 10 + " - watch out! - " + "!" * 10)
!!!!!!!!!! - watch out! - !!!!!!!!!!
```

## Indexes in strings (a[3])

This is something we did a bit already. Basically we can take out specific part of the string via an index. An index is defined by square brackets `[]` behind the string (or string variable). Indexes always start from 0.

Some examples:
```python
>>> a = 'abcdefghijklmnop'
>>> a[0]
'a'
>>> a[1]
'b'
>>> a[-1]
'p'
>>> a[0:1]
'a'
>>> a[0:5]
'abcde'
>>> a[1:2]
'b'
>>> a[1:3]
'bc'
>>> a[3:-1]
'defghijklmno'
```

## Length of string (len(a))

Sometime we just want to know the length of a string! We can use for that the built-in function `len(x)`. In the case of string it'd be like:

```python
>>> len('abc')
3
>>> x = '012345'
>>> len(x)
6
```

This can be used when verifying of inputs from users, or formatting, etc. Imagine a case, where a user is supposed to provide a user name, that can only be a certain length.

Note that the Python built-in len() function can be used to determine length of various types, not just strings! For instance, lists, dictionaries, sets, etc.

## string formatting (deprecated '%' % a; '{}'.format(a); f'{a}')
## iterate over characters in a string (for char in a)
## membership ('x' in a)
## default string functions
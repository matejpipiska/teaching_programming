

### keyboard/screen

We can read strings from keyboard/user and e.g. store them in a variable for further processing. For instance:

```python
name = input("Please enter your name: ")
print("Hello " + name)
```

Will look like this when run:
```
Please enter your name:
# here program waits for your input e.g. Matej
Please enter your name: Matej
Hello Matej
```

This would be our way of taking info in. Our input via keyboard. To output, we can do what we already know - print()

```python
print("Hello!")
age = 25
print("Mary is " + str(age) + " years old!")
```
There are various ways to format the text 'on the fly', but we will get to that later. One notable thing could be the parameter called `end`, which allows us to set a custom ending character when printing something on the screen. By default, the character inserted is `\n`, also known as the 'end of line' character. If we e.g. want to print multiple sentences in one line, we have to set it to something else, such as empty string, or `''`. In practice:
```python
print("hello!", end='')
print("my friend!")
# would produce
# hello!my friend!

print("hello!")
print("my friend!")
# would produce
# hello!
# my friend!

# note the separate lines! :)
```

#### files
We can also open a file in order to read from or write into.

Most commonly we either read the whole file, or a line by line. First we need to open a file, which will give us so called 'file handler', that then we can operate and read/write. Here we focus only on reading.

```python
with open('workfile', 'r') as f: # f is the file handler; 'r' means we open it for reading
     read_data = f.read() # this will read all the file
     print(read_data)
```

Alternatively, we can read line by line through:
```python
with open('another_workfile') as f: # we can also omit the 'r', as it is the default value
    for line in f: # this will iterate over file line by line
        print(line)
```

We can also use a file as an output! It is not that much different from reading, just that we write instead.

First we need to open the file we want to work with. We have to specify that we want to open a file for writing.

```python
with open('workfile', 'w') as f:
    f.write('Hello world!')
```
# Using Python
All we do going forward can be done or tested practically. For that, however, we need to know how to work with Python and what it can offer us. Here we describe different ways to run our code using python, try using CLI a tiny bit and show some useful tricks. We cover:

## Python interpreter (CLI = Command Line Interface)

  - Not all languages have this. You can open a window and run commands as if you were running a program. It is e.g. good for testing of 'what would happen if you do X'.
  - To open, just run `python`
  - To exit, do `exit()` or press `Ctrl+D`

## Versions of python - 2 vs 3

  - Just use 3. 2 is old, but exists (was stopped being used end of last year)
  - To find version, either `python --version` or `python -V` (the upper case is important) or just `python` and see what version it mentions.
  - By running `python` you start your 'default' version. If you want to pick a version, try `python <press TAB a few times>`. You should see something like, `python2`, `python3`, `python3.6`, etc.
- using CLI as a 'calculator' or to test what we intend to do! Woo! Practical work!
  - Maybe try:
    - `3+5`
    - `3*5`
    - `a=5`, `a`
    - `a+10`, `a`
    - `b=10`, `b`
    - `a-b`, `a`, `b`
    - `a=a+3`, `a`
    - `b=a+b`, `b`
    - `greeting="Hello "`
    - `greeting + "Pola!"`

## Comments '#' and why we use them

  - Use: clarifications, TODO, notes on branching of code, message for next adventurers :D
  - They are ignored when the program is ran (or if it is compiled), so are mostly for us and other people who might read the code
  - make a command with `#` after it. E.g. `3 + 5 # the sum of 3 and 5`

## Running programs outside of CLI

  - `python <name of script>` (or python3 or so)

## IDEs - Integrated Development Environments

  - Make development much easier
  - Help us autocomplete and keep track of variables, best practices and whatnot
  - We can use Visual Studio Code for Mac.
  - Run it using `code` or Launcher icon
  - We can also use it to e.g. edit MarkDown files (e.g. README.md in repositories) with easily seeing what we do (that's how I do this document, too)
  - This IDE has extensions, which can help with coding, commiting via Git and customizing the environment.
  - Recommended starting extensions:
    - `Anaconda Extension Pack` - General helping tools and context menus
    - `Better Comments` - Highlighting of comments in different ways
    - `GitLens - Git supercharged` - tools to help with working with Git directly from IDE, see who did last changes, etc.
    - `Python` - tools to help developing python
    - `Trailing Spaces` - hightlights spaces at the end of the line (usually not good)
    - `WhiteViz` - see whitespaces (spaces, tabs, 'invisible characters' better)
  - Show linting and explain what it is
  - Write commands that we did above in a file and run them using `python <name of file>`

## Mention dependencies and virtual environments

  - A lot of code was done and people publish them as libraries. That way we don't have to invent it ourselves.
  - However, these often come in different versions and with different requirements and our different scripts/projects might need different versions
  - This can create something called 'dependency hell' (illustrate)
  - Virtual environments help us separate our projects and allow each project have different dependencies installed. This is what we also do in the `gcal` project. More on this later.
# What is programming and why Python
We start with a bit of theory about programming, introduce Python and show why we pick this language. Here we cover:

## What is programming

  - Computers speak binary. We don't (and we don't want to)
  - Programming is writing instructions in human readable format, that can be translated to computer readable format and tell it what to do
  - It is like making a cooking recipe, kind of. A set of instructions to be executed (and computers are very good at executing them. To the very tiny detail. Including all the flaws we put in them)
  - Writing a recipe should be easy, so we can focus on creating new ones and not on struggling with the recipe book

## High vs low level languages

  - low = close to computer language; high = close to human language
  - Imagine like automatic vs manual gear on the car
  - Some things (like code interfacing with hardware or core of an operating system) need to be fast and simple.
  - High level languages are built on low level languages.
  - Low level languages are built on simple sets of commands that do 'binary' operations on microchips
  - 99% developers don't touch low level languages, there's no need to
  - High level languages often provide 'magical' features that simplify development, like easier memory management, variable type management, fail safe mechanisms, etc.

## Interpreted vs compiled languages

### Compiled

  - We check the recipe beforehand and make sure we have everything and everything makes sense.
  - We check we have enough big enough bowls and pans to cook the amounts we want to cook, that we understand all instructions, and perhaps re-write the recipe into a form where we can follow it easier (in our own words).
  - When done, we know all parts of this recipe will work and can be executed.
  - However, if something doesn't work as planned, it is harder to see exactly which part of the original recipe failed (as we have already rewritten it into our recipe).
  - If we make the tiniest change in the original recipe, we have to go through the whole process of rewriting it into our recipe again. This takes time (seconds to hours) and can be annoying to wait for hours to see if a tiny change will do something.

### Interpreted

  - We just take the recipe and wing it as we go.
  - We might find things we don't know what to do with.
  - Or we might find out we don't have the right tools or ingredients.
  - There might be faulty cases we never discover, because we never go in that option/branch of recipe(e.g. if you don't have cow milk you can use soy milk, but then you have to add X as well).
  - However, if something fails, we know exactly when and where we failed.
  - If we change something, we can just run it again without any delays.

### In summary

Action | Compiled | Interpreted |
 - | - | - |
 How can we run it? (e.g. after every change) | Always compile, then run. This can take minutes to hours. | Just run what you write as is right as you save the file.
 What is the format of what we run? | Binary, human unreadable. But tailored to given technology (e.g. windows, linux, mac, etc) | Human readable code just as we wrote it.
 Performance when running | Fast. Everything is in the computer understandable format since compiling. | Generally slower as it is 'compiled' (very loosely said) during the run-time.
 Code issue detection | Compiling reveals a lot of issues that could happen or mismatch. Guarantees the program can run (unless some logical errors are present) | We do not see problems before we run into them (this is not entirely true, but let's go with it for now)
 Troubleshooting if the program crashes | Harder to pintpoint exact problem. This happens more often during compiling, but is hard to map back once compiled (although there are ways, but generally more annoying) | You easily see which line the program broke on as it executes line by line.

## Dynamic/static variable types

  - Storing of any information is done in variables - cause they vary
  - Variables have types, so the computer knows what kind of data we store there and it should expect (otherwise it gets unhappy. "But you said we put only liquids in the blender! What the hell is this? It's a whole egg!")
  - Some languages require us to explicitly tell what type every variable is, before we store anything in them.
  - However! Some languages hide this from us and adjust the type for us. Magic! ("Oh, this looks like a liquid. Okay, I will categorize it as such, no worries")
  - Python is one of those. So we do not need to worry :)
  - It has (of course) pros and cons. For instance:
    - Performance (the processor needs to do a lot of handling and changes in the background)
    - More prone to errors if handled wrong
    - If the code gets big, having strict types can make it easier to work with it
    - However, it is such easy way to use these that the pros outweight the cons in most cases. Unless you're trying to do some crazy shit.

## Prototyping - ease of use and speed of development

  - Comparison to other languages [here](https://dev.to/saigowthamr/hello-world-examples-in-10-different-languages-4pf3)
  - Python code is short.
  - Python code is intuitive.
  - Python has a lot of libraries that do things for you.
  - This makes Python easy to learn.
  - Python has a lot of users.
  - Python is perfect for small automation projects
  - Having such a big community provides for a lot of support, questions and answers on internets, fast improvements, tons of libraries to do things for you, etc.

## Why would we even use other languages if Python is so awesome?

  - There is no 'best' language. There is always the 'best' language for the given task.
  - Each language has strong and not so strong areas
  - High performing services would not use Python. (this is why e.g. Spotify doesn't use it for user facing services)
  - Specialized tools that work directly with hardware wouldn't use Python, etc.
  - But a lot of work we do is focused around automating some other tools, or interfacing with some products (e.g. gmail, google calendar, spreadsheets, etc.). For these kinds of work, that also do not require crazy performance, Python is perfect.

## Briefly on procedural, object oriented and functional programming

  - Things can be done in many ways, there is no right way
  - Procedural - step by step recipe, going from top to bottom (with branches or conditions)
  - Object oriented - Creating object 'blueprints' that can perform certain tasks, or can be derived/inherited from other object blueprints. Then the program uses parametrized copies of those blueprints and works with them
  - Functional - everything is a function and feeds into another function. It can be powerful but I have no idea about it and never did it.
  - Python code can be written in any of those ways. It is often a mix of procedural and object oriented. We'll get to this later
  - For starters we'll go with the simple procedural one, which is the easiest to grasp

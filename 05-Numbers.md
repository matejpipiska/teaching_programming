# Types - Numbers

One of the most common types in programming are numbers. Numbers can come in various formats and are often used to do calculations or keep count of various things, events and so on. Usually we should use the number type that is relevant to our purpose. There is usually a limit on the highest (or lowest) number stored and this can vary based on the type.

To figure the type of a number (or any variable) we can simply use the `type` function.

```python
>>> type(3)
<type 'int'>
>>> type(3.5)
<type 'float'>
>>> a = 3/5.3
>>> a
0.5660377358490566
>>> type(a)
<type 'float'>
>>> a = 3
>>> type(a)
<type 'int'>
```

We recognize a multitude of types related to numbers. The most relevant are integers and floats.

## Integers
*E.g.: 0, 1, 2, -1, 1000*

*Conversion: int(3.5) -> 3*

Integers are our good old simple numbers. We recognize them because they have no special characters in them. No dots, no letters. They can be positive, or negative. In some languages we can specify the 'size' of the number we want to reserve (e.g. int, long int, double int, unsigned int) which helps manage the memory better.

## Float (floating point numbers)
*E.g.: 0.1, -0.333, 0.47*

*Conversion: float(3) -> 3.0*

Similar like integers, but not whole numbers. They have a dot.

Notice how a selection of numbers changes the result in calculation:
```python
>>> 3*5
15
>>> 3.0*5.0
15.0
>>> 3/5
0
>>> 3/5.0
0.6
>>> 3.0/5
0.6
```
In other words, if we want the result to be a float, we must ensure one (or all) of the numbers in the calculation is a float.

## Hex (hexadecimal)
*E.g.: 0x0000, 0xabcd, 0x0aaa, 0xdeadbeef*

*Conversion: hex(3) -> '0x3'*

Hexadecimal numbers. These can be recognized by starting with `0x`. They are often used in computer 'language' and as network related stuff.

We can see what the actual value is like so:

```python
>>> 0x123
291
```

## Binary
*E.g.: 0b1, 0b01010*

*Conversion: bin(3) -> '0b11'*

A very true language of computers! Similar like hex numbers, they start with a special beginning, in this case `0b`

We can see what the actual number is similar to hex:

```python
>>> 0b0101
5
>>> 0b111111
63
```


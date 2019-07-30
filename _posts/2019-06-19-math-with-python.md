---
title: Math with Python
description: Learn how basic mathematical operators including -- addition, subtraction, multiplication, division, floor division, the modulo operator, and controlling order of operations using  parenthesis.
tags: python
---

Python is an excellent language choice for doing math calculations. This is why popular scientific computing libraries such as NumPy and SciPy are written in Python. However, there's a lot you can do with the Python Standard Library. Lets look at some of the basic mathematical operators that exist in Python.

## Mathematical Operators

An operator is a symbol that indicates a specific operation. For example, the `+` sign indicates addition. Lets look at the most common operators that are used to do math in python. 

### Addition Operator


```python
# We'll create some variables to do math with their values
# This is to show that we can use the operators on raw values
# or between variables

five = 5
two = 2
```


```python
5 + 2
```




    7




```python
five + two
```




    7



### Subtraction Operator


```python
5 - 2
```




    3




```python
five - two
```




    3



### Multiplication Operator


```python
5 * 2
```




    10




```python
five * two
```




    10



### Division Operator


```python
5 / 2
```




    2.5




```python
five / two
```




    2.5



### Floor Division Operator (integer division)

Floor division computes division and if there is any decimal portion included with the result, the result will be rounded down to the nearest whole number. This is sometimes useful for translating floating point values into integer values and for this reason this operation is also called "integer division." 

Let's ompare the result of the regular division operator with the integer division operator.


```python
5 / 2
```




    2.5




```python
5 // 2
```




    2



Rounding a float down to the nearest whole number is also referred to as "flooring" a number. 

It's important to note that the types of values that result from these two operations are different. The division operator will always result in a float whereas the floor division operator results in an integer. you can use the `type()` function to check the variable type of any value.

When we change a variable from one type to another this is called "casting." In this case, we are casting a float to an integer. 


```python
type(5/2)
```




    float




```python
type(5//2)
```




    int




```python
division_result = 5/2
floor_division_result = 5//2
```


```python
type(division_result)
```




    float




```python
type(floor_division_result)
```




    int



### Exponent Operator


```python
5 ** 2
```




    25




```python
five ** two
```




    25



### Modulus (remainder) Operator

The modulus (or modulo) operator is represented by the percent sign `%`. It reports back the remainder after division between two numbers. At first this may not seem like a very useful operation, but is extremely useful in a variety of settings in computer programming. Think about if you wanted to apply some operation every other time or every fifth time. The modulo operator makes performing operations like this extremely easy. 


```python
5 % 2
```




    1




```python
five % two
```




    1



## Controlling Order of Operations with Parenthesis `( )` 

No discussion of mathematical operators would be complete without mentioning how Python handles order of operations when calculations are performed. You'll find that the order of operations that Python uses is similar to what you have been taught in traditional math classes. If you want to ensure that operations are calculated in a specific order then you'll need to wrap those operations in parenthesis in order to ensure that happens. 

The order of operations is typically as follows:

- Parenthesis
- Exponents
- Multiplication & Division
- Addition & Subtraction

Notice how much differently the results following calculations are depending on the placement of parenthesis.


```python
# 4**2 = 16 
# 3 / 16 = .1875
# 5 + .1875 = 5.1875

5 + 3 / 4 ** 2
```




    5.1875




```python
# 5 + 3 = 8
# 4 ** 2 = 16
# 8 / 16 = 0.5

(5 + 3) / (4 ** 2)
```




    0.5




```python
# 5 + 3 = 8
# 8 / 4 = 2.0
# 2.0 ** 2 = 4.0

(((5 + 3) / 4) ** 2)
```




    4.0



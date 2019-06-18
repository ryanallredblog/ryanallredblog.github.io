---
title: Declare Variables in Python
description: Learn how to declare variables in python, and store the three most common types of data to a variable -- integers, floats and strings. We will also learn how to print out a variable to see its value outputted
tags: python
---

A variable is unique identifier that is used to retrieve a piece of data that is stored in the computer's memory. To keep things simple, we'll start off by talking about the three most common types of data that can be stored in a variable in Python:

- Integers (whole numbers positive, negative, or zero)
- Floats (numbers with decimals)
- Strings (sequences of characters i.e. text)

In order to assign a value to a variable in Python we first type the variable name, then the `=` (equals sign -also known as the "assignment operator") and then the value that we want assigned to that variable -and that's it! Python will automatically allocate the memory and store the value in the computer under the designated variable name.

## Create a variable and assign a value to it

### Integers:

Let's create a variable and call it "my_variable" and assign the integer 5 to it.


```python
# declare the variable "my_variable" and assign the integer 5 to it.
my_variable = 5
```

If we want to see the value that has been saved under a specific variable name we can use the print statement to output the variable's value.


```python
print(my_variable)
```

    5


Google Colab and other applications for running Jupyter Notebooks will also show a variable's value in the cell's output even if the print statement is not included.


```python
my_variable
```

    5



### Floats:

Now lets try and save a float to a variable. A float is just a number that includes a decimal representation.


```python
# declare a float variable and a string variable
my_float = 0.5
print(my_float)
```

    0.5


### Strings:

Strings are sequences of characters that are wrapped in quotation marks. `""` or `''`. You can use either double or single quotes as long as they match on either end of the string. Lets create a new variable called `hello_message` and save the string `"Hello World!"` to it and then we'll print it out. 


```python
hello_message = "Hello World!"
print(hello_message)
```

    Hello World!


That's all there is to it! You now know how to:
- declare a new variable in python
- save one of three common types of data to that variable (integers, floats, and strings) 
- print out a variable to see its value outputted

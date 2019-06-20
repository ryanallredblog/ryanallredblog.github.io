---
title: Python Lists and List Methods
description: This post covers creating python lists and list methods such as append, insert, pop, contains, remove, sort, and the length function -- len() 
tags: python
---


In previous posts we have talked about three specific variable types: Integers, Floats and Strings. In this post we will introduce `Lists`. A list is an ordered container that can hold multiple pieces of information. 

## An example list to work with:


```python
my_list = ['cat', 5, 2.7, "this is a string", -400]
```

The items that we want our list to hold for us are wrapped by square brackets `[ ]` and each item in the list is separated by commas `,` in order to designate where one item starts and the other ends. Once we have created our list we will save it to a variable using the assignment operator `=`. In this case we have called the variable `my_list`. 

## Printing out a list stored in a variable

We can retrieve our list from the computer's memory in the same way that we would retrieve any other variable: We can use the print statement, or let our notebook output the contents of the variable for us.


```python
print(my_list)
```

    ['cat', 5, 2.7, 'this is a string', -400]



```python
my_list
```




    ['cat', 5, 2.7, 'this is a string', -400]



## Accessing specific items in a list

One of the most powerful aspects of lists is that they are **ordered** meaning that the list keeps track of which item comes first, second, third, etc. This means that we can access specific items in the list based on its position *in* the list. We'll access the first item in the list below.


```python
my_list[0]
```




    'cat'



We can access any item within a list by putting square brackets to the right side of the variable that the list is saved to and then "passing in" the index (position) of the item that we want to access. 

**NOTE:** As is the case with many programming languages, index locations are slightly different from our typical counting numbers in that they start at 0 and go up from there instead of starting at 1. This means that if I want to grab the first element in the list I will pass in a 0. I will pass in a 1 to get the second element, a 2 for the third element, and so on.

What would I need to write in order to access the `"this is a string"` item inside of `my_list`? 

`"this is a string"` is the fourth element in the list therefore I will pass in its index location of 3 in order to access that item.


```python
my_list[3]
```




    'this is a string'



## Adding items to the end of a list

Many Python variable types have built-in functions that we can access in order do things with them. Lists are no exception.

If I want to add an item to a list, I can use the `.append()` method. Since all lists come with this functionality, I can call this method directly on the variable that I stored my list in and use it to manipulate the underlying container.


```python
my_list.append("New Item")
```


```python
my_list
```




    ['cat', 5, 2.7, 'this is a string', -400, 'New Item']



By calling the .append() function on the list and passing the item that we wanted to add to the list inside of the parenthesis, we were able to add the string `'New Item'`.

## Adding items to a list at a specific index

Another method that exists on list objects is the `.insert()` method that we can use in order to insert new items into the list at a specific location. 

Lets add the string `"Newer Item"` to `my_list`. We can do this by passing in two parameters to the `.insert()` function, the first parameter that we need to provide is the index location where we want the new item to be located at. The second parameter is the item that we want to pass in. Lets add the string `"Newer Item"` at the index position `3`


```python
my_list.insert(3, "Newer Item")
```


```python
my_list
```




    ['cat', 5, 2.7, 'Newer Item', 'this is a string', -400, 'New Item']



We can access the item that we just inserted into the list at the same index position that we used to insert it *into* the list.


```python
my_list[3]
```




    'Newer Item'



## Remove the first instance of an item from a list

We can use the `.remove()` function to remove an item from a list. The remove function will look through the list from left to right and remove the first instance of the item that it is looking for from the list.


```python
my_list.remove(2.7)
```


```python
my_list
```




    ['cat', 5, 'Newer Item', 'this is a string', -400, 'New Item']



The `.remove()` function will return an error if the item that it is looking for doesn not exist in the list. For example, if I try and remove the integer `10` the `.remove()` function will throw an error because that item is not in our list.


```python
my_list.remove(10)
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-25-4cc6fa43bfde> in <module>
    ----> 1 my_list.remove(10)
    

    ValueError: list.remove(x): x not in list


## Remove an item at a specific index location from a list

We can use the `.pop()` function to remove an item at a specific location from our list. We only need to pass the `.pop()` function a single parameter -the index location of the item that we want to remove. Lets remove the integer -400 that is in index position `4`.


```python
my_list.pop(4)
```




    -400




```python
my_list
```




    ['cat', 5, 'Newer Item', 'this is a string', 'New Item']



## Create a new list by saving an empty list to a variable

Sometimes we won't know what we will want to put in our list right when we know that we're going to need one. We can save a blank list to a variable and then items after the fact if we want.


```python
new_list = []
```


```python
new_list
```




    []




```python
new_list.append(5)
new_list.append(2)
new_list.append(8)
new_list.append(3)
new_list.append(1)
new_list.append(4)
new_list.append(9)
new_list.append(6)
new_list.append(10)
new_list.append(7)
new_list
```




    [5, 2, 8, 3, 1, 4, 9, 6, 10, 7]



## Sort the items in a list

We have added the numbers 1-10 to our list. But they're all out of order. We can use the `sort()` method to put them in ascending order.


```python
new_list.sort()
new_list
```




    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]



If I want the list to be sorted in descending order then I can pass in the parameter `reverse=True`


```python
new_list.sort(reverse=True)
new_list
```




    [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]



If I have a list that mixed both numeric and string data types, then the .sort() method's default functionality will not be enough to sort the list. Sorting mixed type lists is possible but is beyond the scope of this post. 


```python
mixed_type_list = ['three', 1, 'two', 7, 'other', -5]
mixed_type_list.sort()
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-46-b8f2120cb542> in <module>
          1 mixed_type_list = ['three', 1, 'two', 7, 'other', -5]
    ----> 2 mixed_type_list.sort()
    

    TypeError: '<' not supported between instances of 'int' and 'str'


I **can** however sort lists that contain mixed **numeric** variable types like ints and floats.


```python
ints_and_floats = [2, 6, 3.14, 12, .5, -10]
ints_and_floats.sort()
ints_and_floats
```




    [-10, 0.5, 2, 3.14, 6, 12]



## Count the number of instances of a particular item in a list

I can count how many times a particular item occurs in a list by using the `count()` function.


```python
repetitive_list = ['cat', 'cat', 'dog', 'cat', 'dog', 'dog', 'cat', 'dog',' cat', 'dog']
```


```python
repetitive_list.count('cat')
```




    4




```python
repetitive_list.count('dog')
```




    5



## Get the length of a list (number of items in the list)

I can see how long a list is (how many items are in the list by using the `len()` function. However, the `len()` function is not a method that is specific to python lists, but comes default with the python library and can be used to find the lengths of other Python containers as well. Because of this, we won't run this function by usint "dot syntax" on the end of our list variable (like we have been doing for most of the examples in this post), but we will just call the function like normal and pass our container variable (our list variable) into the function.


```python
len(repetitive_list)
```




    10



There are a few other list methods that we haven't covered here, and the true power of lists isn't as apparent until we combine them with other topics like if statements (conditionals and for loops, so we will definitely be revisiting lists once we have given an overview of some of those other topics.

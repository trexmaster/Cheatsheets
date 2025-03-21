# Python cheatsheet

[TOC]

## Online ressources
* Python documentation : https://docs.python.org/
* Stack Overflow : https://stackoverflow.com/

## Simple data types
Display the type of an object :
```python
>>>type(1)
<class 'int'>
>>>type(1.0)
<class 'float'>
```
Assign to a variable :
```python
>>>x = 4
```
This is a string :
```python
>>>type('Hello')
<class 'str'>
```
Let's concatanate a string :
```python
>>>'Hello'+'World'
'HelloWorld'
```
String and variable concatenation :
```python
>>>name = "Nicolas"
>>>"Hello" + name
'HelloNicolas'
```
Addition :
```python
>>>1 + 1
2
```
Convert a number to a string :
```python
>>>str(1)
'1'
```
Concatanate a string and a number :
```python
>>>'Hello ' + str(1)
'Hello 1'
```
Length of a string :
```python
>>>len('Hello')
5
```
"Multiply" a string :
```python
>>>"Hello"*10
'HelloHelloHelloHelloHelloHelloHelloHelloHelloHello'
```
Variables, concatenation & multiplication :
```python
>>> a = "Happy "
>>> b = "Birthday "
>>> (a + b) * 10
'Happy Birthday Happy Birthday Happy Birthday Happy Birthday Happy Birthday Happy Birthday Happy Birthday Happy Birthday Happy Birthday Happy Birthday '
```
Length of the whole operation above :
```python
>>> len((a + b) * 10)
150
```
Print a string :
```python
>>> print("Hello")
Hello
```
Print variables :
```python
>>> print(a + b)
Happy Birthday
```

## Making choices : booleans, if and conditionals
Booleans :
```python
>>> True
True
>>> type(True)
<class 'bool'>
>>> False
False
>>> type(False)
<class 'bool'>
```
Comparison operators :
```python
False
>>> -1 < 0
True
>>> .5 <= 1
True
>>> "H" in "Hello"
True
>>> "X" not in "Hello"
True
```
If examples :
```python
>>> if 6 > 5 :
...     print("Six is greater than five")
...
Six is greater than five
>>> if 0 > 2 :
...     print("Zero is greater thant two")
...
>>> if "banana" in "bananarama" :
...     print("I miss the 80s ...")
...
I miss the 80s ...
```
If ... Else examples : 
```python
>>> if sister > brother :
...     print("Sister is older")
... else :
...     print("Brother is older")
...
Sister is older
```
Compound comparisons :
```python
>>> x = 1
>>> x > 0 and x < 2
True
>>> 1 < 2 and "x" in "abc"
False
>>> "a" in "hello" or "e" in "hello"
True
>>> 1 <= 0 or "a" not in "abc"
False
>>> x = 1
>>> x > 0 and x < 2
True
>>> 1 < 2 and "x" in "abc"
False
>>> "a" in "hello" or "e" in "hello"
True
>>> 1 <= 0 or "a" not in "abc"
False
>>> temp = 32
>>> if temp > 60 and temp < 75 :
...     print ("Nice and cozy")
... else :
...     print ("Too extreme for me")
...
Too extreme for me
>>> hour = 11
>>> if hour < 7 or hour > 23 :
...     print("Go away !")
...     print("I'm sleeping !")
... else :
...     print ("Welcome !")
...     print ("Everything is 50% off today !")
...
Welcome !
Everything is 50% off today !
```
Elif example :
```python
>>> sister = 15
>>> brother = 15
>>> if sister > brother :
...     print("Sister is older")
... elif sister == brother :
...     print("Same age!")
... else :
...     print("Brother is older")
...
Same age!
```

## Lists
Define a list :
```python
>>> your_list = ["a","b","c"]
>>> your_list
['a', 'b', 'c']
>>> type(your_list)
<class 'list'>
```
Length of a list :
```python
>>> len(your_list)
3
```
Is an item in the list :
```python
>>> "a" in your_list
True
>>> "z" in your_list
False
>>> "z" not in your_list
True
```
Accessing an item of a list directly :
```python
>>> "a" in your_list
True
>>> "z" in your_list
False
>>> "z" not in your_list
True
```
Trying to access an item out of the list range :
```python
>>> your_list[3]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: list index out of range
```
Appending an item to a list :
```python
>>> your_list.append("d")
>>> your_list
['a', 'b', 'c', 'd']
>>> len(your_list)
4
>>> your_list[3]
'd'
```
Create an empty list :
```python
>>> her_list = []
>>> len(her_list)
0
```
Replace items in a list :
```python
>>> names = ["Alice", "Amy"]
>>> names.append("Adam")
>>> names
['Alice', 'Amy', 'Adam']
>>> names[0]
'Alice'
>>> names[0]  ="Jimmy"
>>> names
['Jimmy', 'Amy', 'Adam']
>>> names [2] = "Rachel"
>>> names.append("Tim")
>>> names.append("Bob")
>>> names.append("Alexis")
>>> names
['Jimmy', 'Amy', 'Rachel', 'Tim', 'Bob', 'Alexis']
>>> len(names)
6
```
Items from the end of the list :
```python
>>> len(names) - 1
5
>>> names[len(names) - 1]
'Alexis'
>>> names[-1]
'Alexis'
>>> names[-2]
'Bob'
>>> names[-3]
'Tim'
```
Strings behave like lists :
```python
>>> my_name = "Nicolas"
>>> my_name[0]
'N'
>>> my_name[-1]
's'
```
Lists recap :
```python
>>> fruits = ["apples","bananas","oranges"]
>>> fruits[0]
'apples'
>>> fruits[-1]
'oranges'
>>> fruits[0] = "plums"
>>> fruits
['plums', 'bananas', 'oranges']
>>> fruits.append("cherries")
>>> fruits
['plums', 'bananas', 'oranges', 'cherries']
>>> len(fruits)
4
>>> "plums" in fruits
True
>>> "apples" in fruits
False
```

## Loops
For examples :
```python
>>> names = ["Alice","Bob","Cassie","Diane","Ellen"]
>>> for name in names:
...     print(name)
...
Alice
Bob
Cassie
Diane
Ellen
>>> for x in names:
...     print(x)
...
Alice
Bob
Cassie
Diane
Ellen
>>> for word in names:
...     print("Hello "+word)
...
Hello Alice
Hello Bob
Hello Cassie
Hello Diane
Hello Ellen
```
Print a name if it starts with a vowel :
```python
>>> name = "Alice"
>>> name[0]
'A'
>>> name[0] in ["A","E","I","O","U"]
True
>>> name[0] in "AEIOU"
True
>>> for name in names:
...     if name[0] in "AEIOU":
...         print(name + " starts with a vowel")
...
Alice starts with a vowel
Ellen starts with a vowel
```
Building a new list from the names starting with a vowel :
```python
>>> vowel_names = []
>>> for name in names :
...     if name[0] in "AEIOU":
...         vowel_names.append(name)
...
>>> vowel_names
['Alice', 'Ellen']
```
Calculate a total :
```python
>>> prices = [1.5,2.35,5.99,16.49]
>>> total = 0
>>> for price in prices:
...     total = total + price
...
>>> total
26.33
>>> sum(prices)
26.33
```

## Dictionaries
* Stores key-value pairs
* Doesn't care about order
* Keys must be unique
* Values don't have to be unique
Create a dictionary :
```python
>>> ice_cream = {"Alice" : "chocolate", "Bob" : "strawberry", "Cara" : "mint chocolate chip"}
```
Display the value of a key :
```python
>>> ice_cream["Alice"]
'chocolate'
>>> ice_cream["Bob"]
'strawberry'
```
If we try to access a key that doesn't exist :
```python
>>> ice_cream["Alice"]
'chocolate'
>>> ice_cream["Bob"]
'strawberry'
```
Add a key to a dictionary :
```python
>>> ice_cream["Eve"] = "rum raisin"
```
A dictionary really doesn't care about order :
```python
>>> ice_cream
{'Eve': 'rum raisin', 'Bob': 'strawberry', 'Alice': 'chocolate', 'Cara': 'mint chocolate chip'}
```
Is a key in a dictionary :
```python
>>> "Eve" in ice_cream
True
```
A key MUST be unique :
```python
>>> ice_cream["Bob"] = "vanilla"
>>> ice_cream
{'Eve': 'rum raisin', 'Bob': 'vanilla', 'Alice': 'chocolate', 'Cara': 'mint chocolate chip'}
```
Create an empty dictionary :
```python
>>> phone_numbers = {}
```
Check the type of a dictionary :
```python
>>> type(phone_numbers)
<class 'dict'>
```

## Modules
Import a module :
```python
>>> import random
>>>
```
Use a module function :
```python
>>> random.randint(1,6)
3
>>> random.randint(1,6)
5
>>> random.randint(1,6)
3
>>> random.randint(1,6)
4
```
Choose a random list item :
```python
>>> card = ["jack","queen","king","ace"]
>>> random.choice(card)
'king'
>>> random.choice(card)
'jack'
>>> random.choice(card)
'king'
>>> random.choice(card)
'jack'
>>> random.choice(card)
'jack'
>>> random.choice(card)
'queen'
>>> random.choice(card)
'ace'
>>> random.choice(card)
'jack'
```


```python
def function():
    #indenting works just fine in the fenced code block
    s = "Python syntax highlighting"
    print s
```

## Interesting functions

* Lambda functions:
  * Anonymous functions have no name, and in Python, they're called lambda functions after lambda calculus. Here's a lambda function that takes a single argument x and returns the result of x + 1:
  ```python
  lambda x: x + 1
  ```
  * [Boot.dev lesson](https://www.boot.dev/lessons/6efdb47f-520a-4fd9-8629-34eb69f57667)
  * [Python doc about lambdas](https://docs.python.org/3/reference/expressions.html#lambda)
* Map:
  * In Python, the built-in map function takes a function and an iterable (in this case a list) as inputs. It returns an iterator that applies the function to every item, yielding the results.
  * [boot.dev lesson](https://www.boot.dev/lessons/3990f287-528f-4881-bc09-73e2ba05d96d)
  * [Python doc about map](https://docs.python.org/3/library/functions.html#map)
* Filter:
  * The built-in filter function takes a function and an iterable (in this case a list) and returns an iterator that only contains elements from the original iterable where the result of the function on that item returned True.
  * [boot.dev lesson](https://www.boot.dev/lessons/c3fbe0a1-0f70-47c0-b1e4-7195b0ef9a16)
  * [Python doc about filter](https://docs.python.org/3/library/functions.html#filter)
* Reduce:
  * The built-in functools.reduce() function takes a function and a list of values, and applies the function to each value in the list, accumulating a single result as it goes.
  * [boot.dev lesson](https://www.boot.dev/lessons/7431bed0-b31a-4d8e-b389-c64a619304ad)
  * [Python doc about reduce](https://docs.python.org/3/library/functools.html#functools.reduce)
# Python cheatsheet
* [Online ressources](#online-ressources)
* [Simple data types](#simple-data-types)
* [Making choices : booleans, if and conditionals](#making-choices-booleans-if-and-conditionals)
* [Lists](#lists)
* [Loops](#loops)
* [Dictionaries](#dictionaries)

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

```python
def function():
    #indenting works just fine in the fenced code block
    s = "Python syntax highlighting"
    print s
```
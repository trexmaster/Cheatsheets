# Python cheatsheet
* [Simple data types](#simple-data-types)
* [Making choices : booleans, if and conditionals](#making-choices-booleans-if-and-conditionals)

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


```python
def function():
    #indenting works just fine in the fenced code block
    s = "Python syntax highlighting"
    print s
```
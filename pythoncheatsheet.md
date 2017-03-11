# Python cheatsheet
* [Simple data types](#simple-data-types)

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


```python
def function():
    #indenting works just fine in the fenced code block
    s = "Python syntax highlighting"
    print s
```
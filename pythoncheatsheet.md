# Python cheatsheet
[Simple data types][#simple-data-types]
## Simple data types
Display the type of an object :
```python
>>> type(1)
<class 'int'>
>>> type(1.0)
<class 'float'>
```
Assign to a variable :
```python
>>> x = 4
```
This is a string :
```python
>>> type('Hello')
<class 'str'>
```
Let's concatanate a string :
```python
>>> 'Hello'+'World'
'HelloWorld'
```
String and variable concatenation :
```python
>>> name = "Nicolas"
>>> "Hello" + name
'HelloNicolas'
```
Addition :
```python
>>> 1 + 1
2
```
Convert a number to a string :
```python
>>> str(1)
'1'
```
Concatanate a string and a number :
```python
>>> 'HEllo ' + str(1)
'HEllo 1'
```
Length of a string :
```python
>>> len('Hello')
5
```

```python
def function():
    #indenting works just fine in the fenced code block
    s = "Python syntax highlighting"
    print s
```
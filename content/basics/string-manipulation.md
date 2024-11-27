---
title: String-Manipulation
date: 2024-11-27
author: Your Name
cell_count: 46
score: 45
---

```python
# string creation ,

s1 = 'Hello'
s2 = "World"
```


```python
s3 = '''Python's String Manipulation'''
```


```python
str1 = "Hello"
str2 = "World"
```


```python
result = str1 + " " + str2
```


```python
result
```




    'Hello World'




```python
s = "Hello"
```


```python
result = s * 3
```


```python
result
```




    'HelloHelloHello'




```python
s = "Hello World"
```


```python
print(s[0:5]) 
```

    Hello



```python
print(s[-5:]) 
```

    World



```python
s = "Hello"
```


```python
print(len(s)) 
```

    5



```python
s = "hello WORLD"
```


```python
s.upper()
```




    'HELLO WORLD'




```python
s.lower()
```




    'hello world'




```python
s.capitalize()
```




    'Hello world'




```python
s.title()
```




    'Hello World'




```python
s.swapcase()
```




    'HELLO world'




```python
s = "   Hello World   "
```


```python
s.strip()
```




    'Hello World'




```python
s.lstrip()
```




    'Hello World   '




```python
s.rstrip()
```




    '   Hello World'




```python
s = "Hello World"
```


```python
s.find("World")
```




    6




```python
s.replace("World", "Python")
```




    'Hello Python'




```python
s = "apple,banana,cherry"
```


```python
s.split()
```




    ['apple,banana,cherry']




```python
fruits = s.split(",")
```


```python
fruits
```




    ['apple', 'banana', 'cherry']




```python
new_string = "-".join(fruits)
```


```python
new_string
```




    'apple-banana-cherry'




```python
name = "Alice"
```


```python
age = 30
```


```python
f"My name is {name} and I am {age} years old."
```




    'My name is Alice and I am 30 years old.'




```python
"My name is {} and I am {} years old.".format(name, age)
```




    'My name is Alice and I am 30 years old.'




```python
"My name is %s and I am %d years old." % (name, age)
```




    'My name is Alice and I am 30 years old.'




```python
# String Checking Methods
```


```python
s = "HelloWorld"
```


```python
s.isalpha()
```




    True




```python
s.isdigit()
```




    False




```python
s.isalnum()
```




    True




```python
s.isspace()
```




    False




```python
s.startswith("Hello")
```




    True




```python
s.endswith("World")
```




    True




```python

```


---
**Score: 45**

---
title: Isinstance-Poc
date: 2024-12-03
author: Your Name
cell_count: 26
score: 25
---

```python
isinstance(object, classinfo)
```


```python
x = 5
```


```python
isinstance(x, int)
```




    True




```python
y = "hello"
```


```python
isinstance(y, str)
```




    True




```python
x = 5.5
```


```python
isinstance(x, (int, float))
```




    True




```python
class Animal:
    pass

class Dog(Animal):
    pass
```


```python
dog = Dog()
```


```python
isinstance(dog, Animal)
```




    True




```python
type(dog) is Animal
```




    False




```python
value= 43
```


```python
if isinstance(value, int):
     print("The value is an integer.")
```

    The value is an integer.



```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


```python

```


---
**Score: 25**

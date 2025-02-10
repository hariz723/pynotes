---
title: Zip-Poc
date: 2025-02-10
author: Your Name
cell_count: 24
score: 20
---

```python
# zip(iterable1, iterable2, ...)
```


```python
# syntax of the zip function is above 
```


```python
list1 = [1, 2, 3]
```


```python
list2 = ['a', 'b', 'c']
```


```python
result = zip(list1, list2)
```


```python
print(list(result))
```

    [(1, 'a'), (2, 'b'), (3, 'c')]



```python
# eg.2 
```


```python
keys = ['uvid', 'userid', 'video_link']
```


```python
values = [0, 1, "link1"]
```


```python
result =dict(zip(keys, values))
```


```python
result
```




    {'uvid': 0, 'userid': 1, 'video_link': 'link1'}




```python
# eg.3
```


```python
list1 = [1, 2, 3]
```


```python
list2 = ['a', 'b', 'c']
```


```python
for num, char in zip(list1, list2):
    print(f"Number: {num}, Character: {char}")
```

    Number: 1, Character: a
    Number: 2, Character: b
    Number: 3, Character: c



```python
# eg.4
```


```python
list1 = [1, 2, 3]
```


```python
list2 = ['a', 'b', 'c']
```


```python
list3 = [10.5, 20.5, 30.5]
```


```python
for num, char, value in zip(list1, list2, list3):
    print(f"Number: {num}, Character: {char}, Value: {value}")
```

    Number: 1, Character: a, Value: 10.5
    Number: 2, Character: b, Value: 20.5
    Number: 3, Character: c, Value: 30.5



```python
keys = ['uvid', 'userid', 'video_link']
```


```python
values = [0, 1, "link1"]
```


```python
for key, value in zip(keys, values):
    print(f"{key}: {value}")
```

    uvid: 0
    userid: 1
    video_link: link1



```python
#conclusion  : with using zip function we can able to convert the list into dict 
```


---
**Score: 20**

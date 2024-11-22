---
title: Regex Python
date: 2024-11-22
author: Your Name
cell_count: 14
score: 10
---

```python
# cheatsheet for regex :
# \d : Matches any digit (0-9).
# \w : Matches any word character (letters, digits, underscore).
# \s : Matches any whitespace (space, tab, newline).
# \b : Matches a word boundary.
# .  : Matches any character except newline.
# *  : Matches 0 or more repetitions of the preceding pattern.
# +  : Matches 1 or more repetitions of the preceding pattern.
# ?  : Matches 0 or 1 repetition of the preceding pattern.
# [] : Matches any character inside the brackets.


# key methods in regex : 
# re.match()   : Matches a pattern only at the start of the string.
# re.search()  : Searches for a pattern anywhere in the string.
# re.findall() : Returns all non-overlapping matches as a list.
# re.sub()     : Replaces occurrences of a pattern.
# re.split()   : Splits a string by the occurrences of a pattern.
```


```python
import re


def func_match_word(pattern):
    # Match a word
    # pattern = r"\bis\b"  # Matches 'word' as a whole word
    text  = "This is a word in a sentence."
    match = re.search(pattern, text)  # search method search the Word we given inside
    if match:
        print(f"Matched: {match.group()}")  
    else: 
        print(f'No matches found')

func_match_word(pattern=r"\bThis\b")
func_match_word(r'\bis')

# unique char here \b{your word to find}
```

    Matched: This
    Matched: is



```python
import re


def func_find_all_matches(pattern):
    # Find all numbers in a string
    # pattern = r"\d+"  # Matches one or more digits
    text    = "The price is 100 dollars and the tax is 15 dollars."
    matches = re.findall(pattern, text)
    # print(matches)  # Output: ['100', '15']
    if matches:
        print(f"Matches : {matches}")
    else:
        print(f"No matches found")


func_find_all_matches(r"\d")
func_find_all_matches(r"\d+")

# unquie char here \d+ find all numbers
```

    Matches : ['1', '0', '0', '1', '5']
    Matches : ['100', '15']



```python
import re


def func_replace_the_char(pattern):
    # Replace all vowels with '*'
    # pattern = r"[aeiou]"
    text = "Hello World"
    result = re.sub(pattern, "*", text)
    if result:
        print(f'result : {result}')  # Output: H*ll* W*rld
    else:
        print('no Matrches found')


func_replace_the_char(r'[aei]')
func_replace_the_char(r'[He]')

# unique char here - [] matches all thee things inside this
```

    result : H*llo World
    result : **llo World



```python
import re


def func_split_the_word(pattern):
    # Split on spaces or commas
    # pattern = r"[ ,]"
    text = "apple, orange banana"
    result = re.split(pattern, text)
    print(result)  # Output: ['apple', '', 'orange', 'banana']

func_split_the_word(r'[, ]')
func_split_the_word(r'[ ,]')

# split th word [, ]

```

    ['apple', '', 'orange', 'banana']
    ['apple', '', 'orange', 'banana']



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
**Score: 10**

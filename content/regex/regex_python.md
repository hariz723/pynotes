---
title: Regex Python
date: 2025-02-10
author: Your Name
cell_count: 46
score: 45
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
```


```python
def func_match_word(pattern):

    text  = "This is a word in a sentence."
    match = re.search(pattern, text)  # search method search the Word we given inside
    if match:
        print(f"Matched: {match.group()}")  
    else:
        print(f'No matches found')

# Match a word
# pattern = r"\bis\b"  # Matches 'word' as a whole word
```


```python
func_match_word(pattern=r"\bThis\b")
func_match_word(r'\bis')

# unique char here \b{your word to find}
```

    Matched: This
    Matched: is



```python
import re
```


```python
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
```


```python
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
```


```python

def func_split_the_word(pattern):
    # Split on spaces or commas
    # pattern = r"[ ,]"
    text = "apple, orange banana"
    result = re.split(pattern, text)
    print(result)  # Output: ['apple', '', 'orange', 'banana']

```


```python

func_split_the_word(r'[, ]')
func_split_the_word(r'[ ,]')

# split th word [, ]
```

    ['apple', '', 'orange', 'banana']
    ['apple', '', 'orange', 'banana']



```python
import re
```


```python

def func_find_name_gmail(pattern):
# Extract groups from a string
    # pattern = r"(\w+)@(\w+)\.(\w+)"  # Matches an email address
    text = "My email is Hari@gmail.com."
    match = re.search(pattern, text)
    # if match:
    print(f"Username: {match.group(1)}")   # Output: Username: example
    print(f"Domain  : {match.group(2)}")   # Output: Domain: gmail
    print(f"TLD     : {match.group(3)}")   # Output: TLD: com
    # else:
    #     print(f'No matches found')
```


```python
func_find_name_gmail(r"(\w+)@(\w+).(\w+)")
```

    Username: Hari
    Domain  : gmail
    TLD     : com



```python
import re
```


```python

pattern = r"((\d+)-(\d+))-(\d+)"
text = "Example: 2024-11-22"
match = re.search(pattern, text)

```


```python
if match:
    print("Entire Match:", match.group(0))  # Output: 2024-11-22
    print("Group 1:", match.group(1))       # Output: 2024-11
    print("Group 2:", match.group(2))       # Output: 2024
    print("Group 3:", match.group(3))       # Output: 11
    print("Group 4:", match.group(4))       # Output: 22

```

    Entire Match: 2024-11-22
    Group 1: 2024-11
    Group 2: 2024
    Group 3: 11
    Group 4: 22



```python
# more e.g based on group func
import re

```

    Entire Match: 12345



```python

pattern = r"(\d+)"
text = "My number is 12345."
match = re.search(pattern, text)
```


```python

if match:
    print("Entire Match:", match.group(0))  # Output: Entire Match: 12345
```

    Entire Match: 12345



```python
import re


```

    All Groups: ('2024', '11', '22')



```python

pattern = r"(\d+)-(\d+)-(\d+)"  # Matches a date format like '2024-11-22'
text = "Today's date: 2024-11-22."
match = re.search(pattern, text)
```


```python


if match:
    print("All Groups:", match.groups())  # Output: ('2024', '11', '22')
```

    All Groups: ('2024', '11', '22')



```python
import re

```


```python
# new here re.IGNORECASE
# Case-insensitive search
pattern = r"hello"
text = "Hello world"
match = re.search(pattern, text, re.IGNORECASE)
```


```python

if match:
    print("Found:", match.group())  # Output: Found: Hello
```

    Found: Hello



```python
import re


```


```python

pattern = r"(\d{4})-(\d{2})-(\d{2})"  # Matches dates in YYYY-MM-DD format
text = "Today's date is 2024-11-22."

match = re.search(pattern, text)
```


```python
if match:
    print("Year:", match.group(1))  # Output: Year: 2024
    print("Month:", match.group(2))  # Output: Month: 11
    print("Day:", match.group(3))  # Output: Day: 22
```

    Year: 2024
    Month: 11
    Day: 22



```python
import re
```


```python

pattern = r"(\w+)\.(\w+)"  # Matches filenames with extensions
text = "file1.txt, file2.pdf, file3.docx"

matches = re.findall(pattern, text)
print(f"matches: {matches}")
```

    matches: [('file1', 'txt'), ('file2', 'pdf'), ('file3', 'docx')]



```python


for filename, extension in matches:
    print(f"Filename: {filename}, Extension: {extension}")
# Output:
# Filename: file1, Extension: txt
# Filename: file2, Extension: pdf
# Filename: file3, Extension: docx

```

    Filename: file1, Extension: txt
    Filename: file2, Extension: pdf
    Filename: file3, Extension: docx



```python
import re
```


```python
pattern = r"^(\w+)@(\w+)\.(\w+)$"  # Matches a basic email pattern
emails = ["test@gmail.com", "invalid-email", "user123@domain.org"]
```


```python

for email in emails:
    match = re.match(pattern, email)
    if match:
        print(f"Valid Email: {email}, Username: {match.group(1)}, Domain: {match.group(2)}")
    else:
        print(f"Invalid Email: {email}")
# Output:
# Valid Email: test@gmail.com, Username: test, Domain: gmail
# Invalid Email: invalid-email
# Valid Email: user123@domain.org, Username: user123, Domain: domain
```

    Valid Email: test@gmail.com, Username: test, Domain: gmail
    Invalid Email: invalid-email
    Valid Email: user123@domain.org, Username: user123, Domain: domain



```python
import re

```


```python
pattern = r"\+?(\d{1,3})-(\d{3})-(\d{3})-(\d{4})"  # Matches phone numbers like +1-123-456-7890
text = "Contact: +1-123-456-7890 or 123-456-7890."

```


```python


matches = re.findall(pattern, text)
for match in matches:
    print("Country Code:", match[0], "Phone Number:", "-".join(match[1:]))
# Output:
# Country Code: 1 Phone Number: 123-456-7890
# Country Code:  Phone Number: 123-456-7890
```

    Country Code: 1 Phone Number: 123-456-7890



```python
import re
```


```python

def check_password(password):
    pattern = r"^(?=.*[A-Z])(?=.*[a-z])(?=.*\d)(?=.*[@#$%^&+=]).{8,}$"
    if re.match(pattern, password):
        return "Strong Password"
    else:
        return "Weak Password"
```


```python
passwords = ["Password1!", "weak", "Strong1@", "1234"]
```


```python
check_password("PAssword")
```




    'Weak Password'




```python

```


```python

```


```python

```


```python

```


---
**Score: 45**

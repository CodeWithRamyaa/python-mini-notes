# Python String Methods

## 1. What are String Methods?

String methods are built-in functions in Python that perform operations on strings.

They help us:
- Change uppercase and lowercase letters.
- Remove unwanted spaces.
- Search for characters and words.
- Replace text.
- Split and join strings.
- Check whether a string contains specific characters.

**Important:** Strings are immutable. String methods generally return a new string instead of modifying the original string.

## 2. Changing Uppercase and Lowercase

### upper()

Converts all characters into uppercase.

```python
text = "hello python"

print(text.upper())
```

Output:
```text
HELLO PYTHON
```

### lower()

Converts all characters into lowercase.

```python
text = "HELLO PYTHON"

print(text.lower())
```

Output:
```text
hello python
```

### capitalize()

Converts the first character to uppercase and the remaining characters to lowercase.

```python
text = "hello PYTHON"

print(text.capitalize())
```

Output:
```text
Hello python
```

### title()

Converts the first character of each word to uppercase.

```python
text = "python programming language"

print(text.title())
```

Output:
```text
Python Programming Language
```

### swapcase()

Converts uppercase characters into lowercase and lowercase characters into uppercase.

```python
text = "Hello Python"

print(text.swapcase())
```

Output:
```text
hELLO pYTHON
```

## 3. Removing Spaces

### strip()

Removes spaces from both the beginning and ending of a string.

```python
text = "   Python   "

print(text.strip())
```

Output:
```text
Python
```

### lstrip()

Removes spaces from the left side.

```python
text = "   Python"

print(text.lstrip())
```

Output:
```text
Python
```

### rstrip()

Removes spaces from the right side.

```python
text = "Python   "

print(text.rstrip())
```

Output:
```text
Python
```

## 4. Searching in Strings

### find()

Returns the index of the first occurrence of a substring.

If the substring is not found, it returns -1.

```python
text = "Python Programming"

print(text.find("Pro"))
```

Output:
```text
7
```

### index()

Returns the index of the first occurrence of a substring.

If the substring is not found, it raises a ValueError.

```python
text = "Python Programming"

print(text.index("Python"))
```

Output:
```text
0
```

### count()

Counts how many times a character or substring appears.

```python
text = "banana"

print(text.count("a"))
```

Output:
```text
3
```

### startswith()

Checks whether a string starts with a particular value.

```python
text = "Python Programming"

print(text.startswith("Python"))
```

Output:
```text
True
```

### endswith()

Checks whether a string ends with a particular value.

```python
text = "Python Programming"

print(text.endswith("Programming"))
```

Output:
```text
True
```

## 5. Replacing Text

### replace()

Replaces one substring with another.

Syntax:

```python
string.replace(old, new, count)
```

The count argument is optional.

Example:

```python
text = "I like Java"

result = text.replace("Java", "Python")

print(result)
```

Output:
```text
I like Python
```

Replacing only the first occurrence:

```python
text = "apple apple apple"

print(text.replace("apple", "mango", 1))
```

Output:
```text
mango apple apple
```

## 6. Splitting and Joining Strings

### split()

Splits a string into a list.

```python
text = "Python is easy"

result = text.split()

print(result)
```

Output:
```text
['Python', 'is', 'easy']
```

Splitting using a comma:

```python
text = "apple,mango,orange"

result = text.split(",")

print(result)
```

Output:
```text
['apple', 'mango', 'orange']
```

### join()

Joins elements of an iterable into a single string using a separator.

```python
words = ["Python", "is", "easy"]

result = " ".join(words)

print(result)
```

Output:
```text
Python is easy
```

Using a hyphen:

```python
words = ["2026", "11", "16"]

print("-".join(words))
```

Output:
```text
2026-11-16
```

## 7. Checking String Content

These methods return True or False.

### isalpha()

Checks whether all characters are alphabets.

```python
text = "Python"

print(text.isalpha())
```

Output:
```text
True
```

### isdigit()

Checks whether all characters are digits.

```python
text = "12345"

print(text.isdigit())
```

Output:
```text
True
```

### isalnum()

Checks whether all characters are alphabets or numbers.

```python
text = "Python123"

print(text.isalnum())
```

Output:
```text
True
```

### isspace()

Checks whether all characters are whitespace.

```python
text = "   "

print(text.isspace())
```

Output:
```text
True
```

### islower()

Checks whether all cased characters are lowercase.

```python
text = "python"

print(text.islower())
```

Output:
```text
True
```

### isupper()

Checks whether all cased characters are uppercase.

```python
text = "PYTHON"

print(text.isupper())
```

Output:
```text
True
```

### istitle()

Checks whether a string follows title case.

```python
text = "Python Programming"

print(text.istitle())
```

Output:
```text
True
```

## 8. String Alignment Methods

### center()

Places a string in the center of a specified width.

```python
text = "Python"

print(text.center(12, "*"))
```

Output:
```text
***Python***
```

### ljust()

Aligns a string to the left.

```python
text = "Python"

print(text.ljust(10, "-"))
```

Output:
```text
Python----
```

### rjust()

Aligns a string to the right.

```python
text = "Python"

print(text.rjust(10, "-"))
```

Output:
```text
----Python
```

### zfill()

Adds zeros to the beginning of a string until it reaches the specified width.

```python
number = "25"

print(number.zfill(5))
```

Output:
```text
00025
```

## 9. Other Useful String Methods

### partition()

Splits a string into three parts using the first occurrence of a separator.

```python
text = "Python is easy"

print(text.partition("is"))
```

Output:
```text
('Python ', 'is', ' easy')
```

### rfind()

Returns the highest index of the specified substring.

Returns -1 if it is not found.

```python
text = "banana"

print(text.rfind("a"))
```

Output:
```text
5
```

### rindex()

Returns the highest index of the specified substring.

Raises ValueError if it is not found.

```python
text = "banana"

print(text.rindex("a"))
```

Output:
```text
5
```

### removeprefix()

Removes a specified prefix if it exists.

```python
text = "Python Programming"

print(text.removeprefix("Python "))
```

Output:
```text
Programming
```

### removesuffix()

Removes a specified suffix if it exists.

```python
text = "report.pdf"

print(text.removesuffix(".pdf"))
```

Output:
```text
report
```

## 10. Difference Between Important String Methods

| Method | Purpose |
|---|---|
| upper() | Converts to uppercase |
| lower() | Converts to lowercase |
| capitalize() | Capitalizes first character |
| title() | Capitalizes each word |
| swapcase() | Reverses letter case |
| strip() | Removes surrounding whitespace |
| find() | Finds substring, returns -1 if missing |
| index() | Finds substring, raises ValueError if missing |
| count() | Counts occurrences |
| replace() | Replaces text |
| split() | Converts string into a list |
| join() | Joins iterable elements into a string |
| startswith() | Checks starting characters |
| endswith() | Checks ending characters |
| isalpha() | Checks alphabetic characters |
| isdigit() | Checks digit characters |
| isalnum() | Checks letters and digits |
| isspace() | Checks whitespace |
| zfill() | Adds zeros to the beginning |

## 11. Common Mistakes

1. String methods do not normally modify the original string.
2. `find()` returns -1 when a substring is missing.
3. `index()` raises ValueError when a substring is missing.
4. `split()` returns a list, not a string.
5. `join()` requires an iterable of strings.
6. `replace()` does not modify the original string.
7. `isdigit()` does not accept ordinary negative numbers such as "-123" as digits.
8. `strip()` removes characters from both ends, not from the middle.

## 12. Real-World Applications

- Cleaning user input.
- Processing text files.
- Validating user information.
- Searching words in documents.
- Preparing text data for machine learning.
- Cleaning datasets using Python.
- Processing customer feedback.
- Natural Language Processing (NLP).

## 13. Important Interview Questions

**Q1. What is the difference between upper() and lower()?**

`upper()` converts characters to uppercase, whereas `lower()` converts them to lowercase.

**Q2. What is the difference between find() and index()?**

`find()` returns -1 when a substring is missing, whereas `index()` raises ValueError.

**Q3. What is the difference between split() and join()?**

`split()` converts a string into a list, whereas `join()` combines iterable elements into a string.

**Q4. What does strip() do?**

It removes leading and trailing whitespace.

**Q5. What is the difference between isalpha() and isalnum()?**

`isalpha()` checks for alphabetic characters only, whereas `isalnum()` accepts alphabetic characters and digits.

**Q6. Does replace() modify the original string?**

No. It returns a new string.

**Q7. What does count() do?**

It returns the number of occurrences of a substring.

**Q8. What is the difference between startswith() and endswith()?**

`startswith()` checks the beginning of a string, whereas `endswith()` checks the ending.

**Q9. What does zfill() do?**

It adds zeros to the beginning of a string until the specified width is reached.

**Q10. Can string methods be chained?**

Yes. Multiple string methods can be applied in a single expression.

Example:

```python
text = "  hello python  "

result = text.strip().upper()

print(result)
```

Output:
```text
HELLO PYTHON
```

## 14. Practice Programs

1. Convert a string into uppercase.
2. Convert a string into lowercase.
3. Capitalize the first character of a sentence.
4. Count how many times a character appears.
5. Remove spaces from the beginning and ending.
6. Replace all spaces with hyphens.
7. Check whether a string starts with a particular word.
8. Check whether a string ends with a particular extension.
9. Split a sentence into individual words.
10. Join a list of words into a sentence.
11. Count vowels using string methods and loops.
12. Check whether a string contains only alphabets.
13. Check whether a string contains only digits.
14. Find the first occurrence of a word.
15. Remove a given prefix or suffix.

---

**Important for Placements:**

Learn when to use each string method instead of memorizing only its definition. Practise combining string methods with loops, conditions and dictionaries to

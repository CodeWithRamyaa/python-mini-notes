# Python Strings in Python

## 1. What is a String?

A string is a built-in Python data type used to store a sequence of characters.

Characters can include:
- Alphabets
- Numbers
- Special symbols
- Spaces

Strings are enclosed within single quotes, double quotes or triple quotes.

### Example

```python
name = "Ramya"
city = 'Bangalore'
message = """Welcome to Python"""

print(name)
print(city)
print(message)
```

**Output:**
```text
Ramya
Bangalore
Welcome to Python
```

## 2. Creating Strings

Strings can be created in three ways.

### Single Quotes

```python
name = 'Python'
print(name)
```

### Double Quotes

```python
name = "Python"
print(name)
```

### Triple Quotes

Used for multiline strings.

```python
message = """Python is easy.
Python is powerful.
Python is popular."""

print(message)
```

## 3. Features of Strings

1. Strings are ordered.
2. Strings are immutable.
3. Strings support indexing.
4. Strings support slicing.
5. Strings can contain duplicate characters.
6. Strings can contain spaces and special characters.

**Important:** Immutable means we cannot directly modify an existing string.

## 4. String Indexing

Indexing means accessing individual characters using their position.

Python uses zero-based indexing.

Consider:

```python
word = "PYTHON"
```

| Character | P | Y | T | H | O | N |
|---|---|---|---|---|---|---|
| Positive Index | 0 | 1 | 2 | 3 | 4 | 5 |
| Negative Index | -6 | -5 | -4 | -3 | -2 | -1 |

### Positive Indexing

```python
word = "PYTHON"

print(word[0])
print(word[2])
print(word[5])
```

**Output:**
```text
P
T
N
```

### Negative Indexing

Negative indexing starts from the end of the string.

```python
word = "PYTHON"

print(word[-1])
print(word[-2])
```

**Output:**
```text
N
O
```

## 5. String Slicing

Slicing means extracting a portion of a string.

### Syntax

```python
string[start:end:step]
```

- start: Starting index.
- end: Ending index (not included).
- step: Number of positions to move.

### Example 1: Basic Slicing

```python
word = "PYTHON"

print(word[0:3])
```

**Output:**
```text
PYT
```

The ending index 3 is excluded.

### Example 2: Starting Index

```python
word = "PYTHON"

print(word[2:])
```

**Output:**
```text
THON
```

### Example 3: Ending Index

```python
word = "PYTHON"

print(word[:4])
```

**Output:**
```text
PYTH
```

### Example 4: Using Step

```python
word = "PYTHON"

print(word[::2])
```

**Output:**
```text
PTO
```

### Example 5: Reverse a String

```python
word = "PYTHON"

print(word[::-1])
```

**Output:**
```text
NOHTYP
```

## 6. String Length

The `len()` function returns the total number of characters in a string, including spaces.

```python
name = "Ramya Gowda"

print(len(name))
```

**Output:**
```text
11
```

## 7. String Concatenation

Concatenation means joining two or more strings.

We use the `+` operator.

```python
first = "Hello"
second = "Python"

result = first + " " + second

print(result)
```

**Output:**
```text
Hello Python
```

## 8. String Repetition

The `*` operator repeats a string multiple times.

```python
word = "Hi "

print(word * 3)
```

**Output:**
```text
Hi Hi Hi
```

## 9. Checking Characters in a String

We use the `in` and `not in` operators.

### Using in

```python
word = "Python"

print("P" in word)
print("z" in word)
```

**Output:**
```text
True
False
```

### Using not in

```python
word = "Python"

print("z" not in word)
```

**Output:**
```text
True
```

## 10. Looping Through a String

We can access every character using a loop.

### Using For Loop

```python
word = "Python"

for char in word:
    print(char)
```

**Output:**
```text
P
y
t
h
o
n
```

### Using While Loop

```python
word = "Python"

i = 0

while i < len(word):
    print(word[i])
    i += 1
```

## 11. Strings Are Immutable

Strings cannot be modified directly after creation.

### Incorrect Example

```python
word = "Python"

word[0] = "J"
```

**Output:**
```text
TypeError
```

### Correct Example

Create a new string instead.

```python
word = "Python"

new_word = "J" + word[1:]

print(new_word)
```

**Output:**
```text
Jython
```

## 12. Comparing Strings

We can compare strings using comparison operators.

```python
a = "Python"
b = "Python"

print(a == b)
print(a != b)
```

**Output:**
```text
True
False
```

String comparisons are case-sensitive.

```python
print("python" == "Python")
```

**Output:**
```text
False
```

## 13. Escape Characters

Escape characters are special characters that begin with a backslash (`\`).

| Escape Character | Meaning |
|---|---|
| `\n` | New line |
| `\t` | Tab space |
| `\\` | Backslash |
| `\'` | Single quote |
| `\"` | Double quote |

### Example

```python
print("Hello\nPython")
```

**Output:**
```text
Hello
Python
```

## 14. String Formatting

String formatting allows us to insert variables into strings.

### Using f-strings

```python
name = "Ramya"
age = 20

print(f"My name is {name} and I am {age} years old.")
```

**Output:**
```text
My name is Ramya and I am 20 years old.
```

### Using format()

```python
name = "Ramya"

print("Hello {}".format(name))
```

**Output:**
```text
Hello Ramya
```

## 15. Raw Strings

Raw strings treat backslashes as literal characters rather than escape sequences.

Use `r` before the string.

```python
path = r"C:\Users\Ramya\Documents"

print(path)
```

**Output:**
```text
C:\Users\Ramya\Documents
```

## 16. Common String Operations

| Operation | Example | Result |
|---|---|---|
| Length | `len("Python")` | 6 |
| First character | `"Python"[0]` | P |
| Last character | `"Python"[-1]` | n |
| Reverse | `"Python"[::-1]` | nohtyP |
| Concatenation | `"Py" + "thon"` | Python |
| Repetition | `"Hi" * 2` | HiHi |
| Membership | `"P" in "Python"` | True |
| Slicing | `"Python"[1:4]` | yth |

## 17. Common Mistakes

1. Remember that indexing starts from zero.
2. The ending index in slicing is excluded.
3. Strings are immutable.
4. Accessing an invalid index causes an `IndexError`.
5. String comparisons are case-sensitive.
6. `len()` counts spaces as characters.
7. You cannot directly concatenate a string and an integer using `+`.

Example:

```python
age = 20

print("Age: " + str(age))
```

**Output:**
```text
Age: 20
```

## 18. Real-World Applications

- Storing names and addresses.
- Processing user input.
- Searching text.
- Validating email formats.
- Text analysis.
- Natural Language Processing (NLP).
- Processing documents and messages.
- Preparing text data for Machine Learning.

## 19. Important Interview Questions

**Q1. What is a string in Python?**

A string is a sequence of characters enclosed in quotes.

**Q2. Are strings mutable or immutable?**

Strings are immutable. Their characters cannot be directly changed.

**Q3. What is indexing?**

Indexing is accessing individual characters using their positions.

**Q4. What is negative indexing?**

Negative indexing accesses characters from the end of a string.

**Q5. What is slicing?**

Slicing extracts a portion of a string using start, end and step values.

**Q6. What is the difference between `==` and `is`?**

`==` compares values, whereas `is` checks whether two references point to the same object.

**Q7. How do you reverse a string?**

Using slicing:

```python
word = "Python"
print(word[::-1])
```

**Q8. What is string concatenation?**

Joining two or more strings using the `+` operator.

**Q9. What does len() do?**

It returns the number of characters in a string.

**Q10. Can strings contain duplicate characters?**

Yes. Strings can contain repeated characters.

## 20. Practice Programs

1. Find the length of a string.
2. Reverse a string.
3. Check whether a string is a palindrome.
4. Count vowels in a string.
5. Count consonants in a string.
6. Count the number of spaces in a string.
7. Count uppercase and lowercase characters.
8. Find the frequency of each character.
9. Remove spaces from a string.
10. Check whether two strings are equal.
11. Find the first and last character.
12. Count the number of words in a sentence.
13. Check whether a character exists in a string.
14. Replace a character in a string.
15. Find duplicate characters in a string.

---

**Important for Placements:**

Strings are frequently used in coding interviews and DSA problems. Develop a strong understanding of indexing, slicing, loops, immutability and character-frequency problems.

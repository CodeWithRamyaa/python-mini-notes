# Python Data Types

## 1. What are Data Types?

Data types specify the type of value that a variable can store.

Python has several built-in data types used to represent different kinds of information.

## 2. Types of Python Data Types

Python has the following major built-in data type categories:

| Category | Data Types |
|---|---|
| Numeric | int, float, complex |
| Text | str |
| Boolean | bool |
| Sequence | list, tuple, range |
| Mapping | dict |
| Set | set, frozenset |
| Binary | bytes, bytearray, memoryview |
| None | NoneType |

## 3. Numeric Data Types

### A. Integer (int)

Stores whole numbers without decimal points.

```python
age = 20
marks = 95

print(age)
print(type(age))
```

Output:
```text
20
<class 'int'>
```

### B. Float (float)

Stores numbers containing decimal points.

```python
price = 99.50
percentage = 85.5

print(price)
print(type(price))
```

Output:
```text
99.5
<class 'float'>
```

### C. Complex (complex)

Stores numbers containing real and imaginary parts.

```python
x = 3 + 5j

print(x)
print(type(x))
```

Output:
```text
(3+5j)
<class 'complex'>
```

## 4. String (str)

A string is a sequence of characters enclosed in single, double or triple quotes.

```python
name = "Python"
message = 'Hello World'

print(name)
print(type(name))
```

Output:
```text
Python
<class 'str'>
```

## 5. Boolean (bool)

Boolean data types represent two values:

- True
- False

```python
is_student = True
is_employed = False

print(is_student)
print(type(is_student))
```

Output:
```text
True
<class 'bool'>
```

## 6. List (list)

A list stores multiple items in a single variable.

Features:
- Ordered
- Mutable
- Allows duplicate values
- Allows different data types

```python
numbers = [10, 20, 30, 40]

print(numbers)
print(type(numbers))
```

Output:
```text
[10, 20, 30, 40]
<class 'list'>
```

## 7. Tuple (tuple)

A tuple stores multiple items in an ordered collection.

Features:
- Ordered
- Immutable
- Allows duplicate values

```python
colors = ("red", "green", "blue")

print(colors)
print(type(colors))
```

Output:
```text
('red', 'green', 'blue')
<class 'tuple'>
```

## 8. Set (set)

A set stores unique values.

Features:
- Unordered
- Mutable
- Does not allow duplicate elements

```python
numbers = {10, 20, 30, 20}

print(numbers)
print(type(numbers))
```

Output:
```text
{10, 20, 30}
<class 'set'>
```

Note: Set display order is not guaranteed.

## 9. Dictionary (dict)

A dictionary stores data in key-value pairs.

Features:
- Mutable
- Keys must be unique
- Values can be duplicated
- Maintains insertion order

```python
student = {
    "name": "Ramya",
    "age": 20,
    "marks": 90
}

print(student)
print(type(student))
```

Output:
```text
{'name': 'Ramya', 'age': 20, 'marks': 90}
<class 'dict'>
```

## 10. Range (range)

The range data type represents a sequence of numbers.

```python
numbers = range(1, 6)

print(list(numbers))
print(type(numbers))
```

Output:
```text
[1, 2, 3, 4, 5]
<class 'range'>
```

## 11. NoneType

None represents the absence of a value.

```python
result = None

print(result)
print(type(result))
```

Output:
```text
None
<class 'NoneType'>
```

## 12. Checking Data Types

Python provides the `type()` function to identify the data type of a value.

```python
a = 100
b = 10.5
c = "Hello"
d = True

print(type(a))
print(type(b))
print(type(c))
print(type(d))
```

Output:
```text
<class 'int'>
<class 'float'>
<class 'str'>
<class 'bool'>
```

## 13. Important Interview Questions

**Q1. What are data types?**

Data types specify the kind of value stored in a variable.

**Q2. What are the numeric data types in Python?**

int, float and complex.

**Q3. What is the difference between a list and a tuple?**

A list is mutable, whereas a tuple is immutable.

**Q4. Which data type stores key-value pairs?**

Dictionary.

**Q5. Does a set allow duplicate values?**

No, sets store unique elements.

**Q6. What is the data type of True and False?**

Boolean (bool).

**Q7. Which function checks the data type of a variable?**

The type() function.

**Q8. What is NoneType?**

It represents the absence of a value.

## Conclusion

Python provides different data types to store and manage information efficiently. Understanding these types is essential for writing Python programs.

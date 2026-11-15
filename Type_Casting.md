# Python Type Casting

## 1. What is Type Casting?

Type casting is the process of converting one data type into another data type.

Python provides built-in functions to convert values between different data types.

Example:

```python
x = 10
y = float(x)

print(y)
print(type(y))
```

Output:
```text
10.0
<class 'float'>
```

## 2. Types of Type Casting

There are two main types:

1. Implicit Type Casting
2. Explicit Type Casting

## 3. Implicit Type Casting

Implicit type casting happens automatically when Python converts one data type into another compatible data type.

Example:

```python
a = 10
b = 5.5

result = a + b

print(result)
print(type(result))
```

Output:
```text
15.5
<class 'float'>
```

Here, Python automatically converts the integer into a float.

## 4. Explicit Type Casting

Explicit type casting happens when the programmer manually converts one data type into another using built-in functions.

### A. int()

Converts a compatible value into an integer.

```python
x = 10.8
y = int(x)

print(y)
```

Output:
```text
10
```

Note: Decimal values are truncated, not rounded.

### B. float()

Converts a compatible value into a floating-point number.

```python
x = 20
y = float(x)

print(y)
```

Output:
```text
20.0
```

### C. str()

Converts a compatible value into a string.

```python
age = 20
result = str(age)

print(result)
print(type(result))
```

Output:
```text
20
<class 'str'>
```

### D. bool()

Converts a value into a Boolean value.

```python
x = 1
y = bool(x)

print(y)
```

Output:
```text
True
```

### E. list()

Converts an iterable into a list.

```python
x = (10, 20, 30)
y = list(x)

print(y)
```

Output:
```text
[10, 20, 30]
```

### F. tuple()

Converts an iterable into a tuple.

```python
x = [10, 20, 30]
y = tuple(x)

print(y)
```

Output:
```text
(10, 20, 30)
```

### G. set()

Converts an iterable into a set, removing duplicate elements.

```python
x = [10, 20, 20, 30]
y = set(x)

print(y)
```

Output:
```text
{10, 20, 30}
```

Note: Set order is not guaranteed.

### H. dict()

Creates a dictionary from an iterable of key-value pairs.

```python
x = [("name", "Ramya"), ("age", 20)]
y = dict(x)

print(y)
```

Output:
```text
{'name': 'Ramya', 'age': 20}
```

## 5. Type Casting Examples

### Example 1: String to Integer

```python
number = "100"
result = int(number)

print(result + 50)
```

Output:
```text
150
```

### Example 2: Integer to String

```python
age = 20
message = "My age is " + str(age)

print(message)
```

Output:
```text
My age is 20
```

### Example 3: Float to Integer

```python
price = 99.99
result = int(price)

print(result)
```

Output:
```text
99
```

## 6. Important Points

- Implicit casting is performed automatically.
- Explicit casting is performed manually.
- Not every conversion is possible.
- Converting an invalid string into an integer raises ValueError.
- Converting a float into an integer removes its fractional part.

## 7. Important Interview Questions

**Q1. What is type casting?**

Type casting is the process of converting one data type into another.

**Q2. What are the types of type casting?**

Implicit and explicit type casting.

**Q3. What is implicit type casting?**

Automatic conversion performed by Python.

**Q4. What is explicit type casting?**

Manual conversion performed by the programmer.

**Q5. Which function converts a value into an integer?**

int().

**Q6. Which function converts a value into a string?**

str().

**Q7. What happens when int(10.9) is executed?**

It returns 10 because the fractional part is truncated.

**Q8. Can every string be converted into an integer?**

No. The string must represent a valid integer.

## Conclusion

Type casting helps programmers convert data between different types and perform operations efficiently.

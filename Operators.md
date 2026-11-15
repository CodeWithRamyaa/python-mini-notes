# Python Operators

## 1. What are Operators?

Operators are special symbols or keywords used to perform operations on variables and values.

Example:

```python
a = 10
b = 5

print(a + b)
```

Output:
```text
15
```

Here, `+` is an arithmetic operator.

## 2. Types of Python Operators

Python supports the following types of operators:

1. Arithmetic Operators
2. Comparison Operators
3. Assignment Operators
4. Logical Operators
5. Bitwise Operators
6. Membership Operators
7. Identity Operators

## 3. Arithmetic Operators

Arithmetic operators are used to perform mathematical operations.

| Operator | Description | Example |
|---|---|---|
| + | Addition | 10 + 5 = 15 |
| - | Subtraction | 10 - 5 = 5 |
| * | Multiplication | 10 * 5 = 50 |
| / | Division | 10 / 5 = 2.0 |
| % | Modulus | 10 % 3 = 1 |
| // | Floor Division | 10 // 3 = 3 |
| ** | Exponentiation | 2 ** 3 = 8 |

Example:

```python
a = 10
b = 3

print(a + b)
print(a - b)
print(a * b)
print(a / b)
print(a % b)
print(a // b)
print(a ** b)
```

Output:
```text
13
7
30
3.3333333333333335
1
3
1000
```

## 4. Comparison Operators

Comparison operators compare two values and return either True or False.

| Operator | Description |
|---|---|
| == | Equal to |
| != | Not equal to |
| > | Greater than |
| < | Less than |
| >= | Greater than or equal to |
| <= | Less than or equal to |

Example:

```python
a = 10
b = 5

print(a == b)
print(a != b)
print(a > b)
print(a < b)
print(a >= b)
print(a <= b)
```

Output:
```text
False
True
True
False
True
False
```

## 5. Assignment Operators

Assignment operators are used to assign or update variable values.

| Operator | Example | Equivalent |
|---|---|---|
| = | x = 5 | x = 5 |
| += | x += 3 | x = x + 3 |
| -= | x -= 3 | x = x - 3 |
| *= | x *= 3 | x = x * 3 |
| /= | x /= 3 | x = x / 3 |
| %= | x %= 3 | x = x % 3 |
| //= | x //= 3 | x = x // 3 |
| **= | x **= 3 | x = x ** 3 |

Example:

```python
x = 10

x += 5
print(x)

x *= 2
print(x)
```

Output:
```text
15
30
```

## 6. Logical Operators

Logical operators combine conditional statements.

| Operator | Description |
|---|---|
| and | True if both conditions are True |
| or | True if at least one condition is True |
| not | Reverses the Boolean result |

Example:

```python
a = 10
b = 5

print(a > 5 and b < 10)
print(a > 15 or b < 10)
print(not(a > 5))
```

Output:
```text
True
True
False
```

## 7. Bitwise Operators

Bitwise operators perform operations on the binary representations of integers.

| Operator | Description |
|---|---|
| & | AND |
| \| | OR |
| ^ | XOR |
| ~ | NOT |
| << | Left Shift |
| >> | Right Shift |

Example:

```python
a = 5
b = 3

print(a & b)
print(a | b)
print(a ^ b)
print(~a)
print(a << 1)
print(a >> 1)
```

Output:
```text
1
7
6
-6
10
2
```

## 8. Membership Operators

Membership operators check whether a value exists in a sequence or collection.

| Operator | Description |
|---|---|
| in | Returns True if the value exists |
| not in | Returns True if the value does not exist |

Example:

```python
fruits = ["apple", "banana", "orange"]

print("apple" in fruits)
print("grapes" not in fruits)
```

Output:
```text
True
True
```

## 9. Identity Operators

Identity operators check whether two variables refer to the same object.

| Operator | Description |
|---|---|
| is | Returns True if both refer to the same object |
| is not | Returns True if they refer to different objects |

Example:

```python
a = [10, 20, 30]
b = a
c = [10, 20, 30]

print(a is b)
print(a is c)
print(a == c)
```

Output:
```text
True
False
True
```

Note: `==` compares values, whereas `is` checks object identity.

## 10. Operator Precedence

Operator precedence determines the order in which operations are performed in an expression.

Common precedence order (higher to lower):

1. Parentheses `()`
2. Exponentiation `**`
3. Unary operators
4. Multiplication, Division, Floor Division and Modulus
5. Addition and Subtraction
6. Comparison operators
7. Logical NOT
8. Logical AND
9. Logical OR

Example:

```python
result = 10 + 5 * 2

print(result)
```

Output:
```text
20
```

Multiplication is performed before addition.

## 11. Important Interview Questions

**Q1. What are operators in Python?**

Operators are symbols or keywords used to perform operations on values and variables.

**Q2. What is the difference between / and //?**

`/` performs division and returns a float. `//` performs floor division.

**Q3. What is the modulus operator?**

The `%` operator returns the remainder of a division.

**Q4. What are logical operators?**

The logical operators are and, or and not.

**Q5. What is the difference between == and is?**

`==` compares values, whereas `is` checks object identity.

**Q6. What are membership operators?**

The `in` and `not in` operators check membership in a collection.

**Q7. What are bitwise operators?**

They perform operations on the binary representations of integers.

**Q8. What is operator precedence?**

It determines the order in which operators are evaluated.

## Conclusion

Python operators help perform mathematical calculations, comparisons, logical operations and other programming tasks.

# Python For Loop

## 1. What is a For Loop?

A for loop is used to execute a block of code repeatedly for each item in a sequence or iterable.

It is commonly used with lists, tuples, strings, dictionaries and ranges.

## 2. Syntax

```python
for variable in sequence:
    statements
```

## 3. Simple For Loop

Example:

```python
for i in range(5):
    print(i)
```

Output:

```text
0
1
2
3
4
```

Here, the loop executes five times.

## 4. Using range() Function

The range() function generates a sequence of numbers.

It supports three arguments:

- start: Starting value (default is 0).
- stop: Ending value (excluded).
- step: Difference between consecutive values (default is 1).

### Example 1: range(stop)

```python
for i in range(5):
    print(i)
```

Output:

```text
0
1
2
3
4
```

### Example 2: range(start, stop)

```python
for i in range(2, 7):
    print(i)
```

Output:

```text
2
3
4
5
6
```

### Example 3: range(start, stop, step)

```python
for i in range(2, 11, 2):
    print(i)
```

Output:

```text
2
4
6
8
10
```

## 5. For Loop with Strings

A for loop can access each character in a string.

Example:

```python
name = "Python"

for char in name:
    print(char)
```

Output:

```text
P
y
t
h
o
n
```

## 6. For Loop with Lists

A for loop can iterate through list elements.

Example:

```python
fruits = ["Apple", "Mango", "Orange"]

for fruit in fruits:
    print(fruit)
```

Output:

```text
Apple
Mango
Orange
```

## 7. For Loop with Tuples

Example:

```python
numbers = (10, 20, 30)

for num in numbers:
    print(num)
```

Output:

```text
10
20
30
```

## 8. For Loop with Dictionaries

A for loop can iterate through dictionary keys and values.

Example:

```python
student = {
    "name": "Ramya",
    "age": 20,
    "marks": 90
}

for key, value in student.items():
    print(key, value)
```

Output:

```text
name Ramya
age 20
marks 90
```

## 9. Nested For Loop

A nested for loop means placing one for loop inside another for loop.

Example:

```python
for i in range(1, 4):
    for j in range(1, 3):
        print(i, j)
```

Output:

```text
1 1
1 2
2 1
2 2
3 1
3 2
```

## 10. For Loop with Else

Python allows an else block with a for loop.

The else block executes when the loop finishes normally without being terminated by break.

Example:

```python
for i in range(3):
    print(i)
else:
    print("Loop completed")
```

Output:

```text
0
1
2
Loop completed
```

## 11. Using break in a For Loop

The break statement immediately terminates the loop.

Example:

```python
for i in range(1, 6):
    if i == 4:
        break
    print(i)
```

Output:

```text
1
2
3
```

## 12. Using continue in a For Loop

The continue statement skips the current iteration and moves to the next iteration.

Example:

```python
for i in range(1, 6):
    if i == 3:
        continue
    print(i)
```

Output:

```text
1
2
4
5
```

## 13. Real-World Applications

For loops are used in:

- Processing student marks.
- Calculating totals.
- Searching elements in a list.
- Reading files.
- Processing datasets.
- Performing repetitive calculations.

## 14. Important Interview Questions

**Q1. What is a for loop?**

A for loop executes a block of code for each item in an iterable.

**Q2. What is the purpose of range()?**

It generates a sequence of numbers.

**Q3. What is the difference between break and continue?**

break terminates the loop, whereas continue skips the current iteration.

**Q4. What is a nested for loop?**

A for loop placed inside another for loop.

**Q5. What is the default starting value of range()?**

Zero.

**Q6. Is the stop value included in range()?**

No, the stop value is excluded.

**Q7. When does the else block execute in a for loop?**

It executes when the loop finishes normally without encountering break.

## Conclusion

For loops are useful for repeating operations and processing elements in sequences efficiently.

# Python Return Statement

## 1. What is a Return Statement?

The `return` statement is used inside a function to send a result back to the place where the function was called.

It allows us to use the calculated result outside the function.

### Example

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)
```

**Output:**
```text
30
```

Explanation:

- `add()` receives two numbers.
- `a + b` calculates their sum.
- `return` sends the result back.
- The returned value is stored in `result`.

## 2. Syntax of Return

```python
def function_name():
    statements
    return value
```

The `return` keyword can return:
- Numbers
- Strings
- Lists
- Tuples
- Dictionaries
- Sets
- Boolean values
- Objects
- Multiple values

## 3. Difference Between print() and return

This is one of the most important concepts in Python.

### Using print()

```python
def add(a, b):
    print(a + b)

result = add(10, 20)

print(result)
```

**Output:**
```text
30
None
```

Why?

The function displays 30 but does not return a value. Therefore, `result` receives `None`.

### Using return

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)
```

**Output:**
```text
30
```

Here, the function returns 30, which is stored in `result`.

### Comparison

| print() | return |
|---|---|
| Displays output | Sends a value back |
| Does not automatically provide a result to the caller | Provides a result to the caller |
| Used for displaying information | Used for calculations and further operations |
| Does not terminate a function | Terminates the function |

## 4. Function Without Return Statement

If a function does not contain an explicit return statement, Python automatically returns `None`.

### Example

```python
def greet():
    print("Hello Python")

result = greet()

print(result)
```

**Output:**
```text
Hello Python
None
```

## 5. Returning a Single Value

A function can return one value.

### Example

```python
def square(n):
    return n * n

result = square(5)

print(result)
```

**Output:**
```text
25
```

## 6. Returning Multiple Values

Python allows a function to return multiple values separated by commas.

Internally, Python packs these values into a tuple.

### Example

```python
def calculate(a, b):
    return a + b, a - b

result = calculate(20, 10)

print(result)
```

**Output:**
```text
(30, 10)
```

### Unpacking Multiple Return Values

```python
def calculate(a, b):
    return a + b, a - b

addition, subtraction = calculate(20, 10)

print(addition)
print(subtraction)
```

**Output:**
```text
30
10
```

## 7. Returning Different Data Types

A function can return different types of data.

### Returning a String

```python
def greet():
    return "Welcome to Python"

print(greet())
```

**Output:**
```text
Welcome to Python
```

### Returning a List

```python
def get_numbers():
    return [10, 20, 30]

numbers = get_numbers()

print(numbers)
```

**Output:**
```text
[10, 20, 30]
```

### Returning a Dictionary

```python
def get_student():
    return {
        "name": "Ramya",
        "age": 20
    }

student = get_student()

print(student)
```

**Output:**
```text
{'name': 'Ramya', 'age': 20}
```

### Returning a Boolean

```python
def is_even(n):
    return n % 2 == 0

print(is_even(10))
print(is_even(7))
```

**Output:**
```text
True
False
```

## 8. Return Statement With Conditions

We can use `return` inside conditional statements.

### Example: Check Even or Odd

```python
def check_number(n):
    if n % 2 == 0:
        return "Even"
    else:
        return "Odd"

print(check_number(10))
print(check_number(7))
```

**Output:**
```text
Even
Odd
```

The function returns different values depending on the condition.

## 9. Early Return

An early return means returning a value before reaching the end of the function.

It is useful when a condition is satisfied and no further execution is required.

### Example

```python
def check_number(n):
    if n < 0:
        return "Negative number"

    return "Non-negative number"

print(check_number(-5))
print(check_number(10))
```

**Output:**
```text
Negative number
Non-negative number
```

Explanation:

When `n` is negative, the function immediately returns `"Negative number"`.

The remaining statements are skipped.

## 10. Return Statement Inside Loops

A return statement inside a loop immediately terminates the entire function, not just the loop.

### Example

```python
def find_number(numbers, target):
    for n in numbers:
        if n == target:
            return "Found"

    return "Not Found"

numbers = [10, 20, 30, 40]

print(find_number(numbers, 30))
```

**Output:**
```text
Found
```

Explanation:

- The function checks each number.
- When 30 is found, it immediately returns `"Found"`.
- The function stops executing.

## 11. Returning a List From a Function

Functions are commonly used to process lists and return the results.

### Example: Find Even Numbers

```python
def get_even_numbers(numbers):
    result = []

    for n in numbers:
        if n % 2 == 0:
            result.append(n)

    return result

numbers = [1, 2, 3, 4, 5, 6]

print(get_even_numbers(numbers))
```

**Output:**
```text
[2, 4, 6]
```

## 12. Returning Results From Another Function

One function can use the returned value of another function.

### Example

```python
def square(n):
    return n * n

def calculate():
    result = square(5)
    return result + 10

print(calculate())
```

**Output:**
```text
35
```

Explanation:

1. `square(5)` returns 25.
2. The value 25 is stored in `result`.
3. 10 is added to 25.
4. The final result 35 is returned.

## 13. Returning None Explicitly

We can also return `None` explicitly.

```python
def display():
    print("Hello")
    return None

result = display()

print(result)
```

**Output:**
```text
Hello
None
```

## 14. Common Mistakes

1. Confusing `print()` with `return`.
2. Forgetting to use the returned value.
3. Writing statements after an unconditional return and expecting them to execute.
4. Forgetting that a function without an explicit return statement returns `None`.
5. Placing return inside a loop unintentionally.
6. Trying to use a returned value without storing it or otherwise using it.
7. Expecting multiple return values to automatically become separate variables without unpacking.

## 15. Real-World Applications

- Returning calculation results.
- Processing student marks.
- Finding maximum and minimum values.
- Returning filtered lists.
- Validating user input.
- Processing datasets.
- Building machine learning functions.
- Developing reusable software components.

## 16. Important Interview Questions

**Q1. What is a return statement?**

A return statement sends a value from a function back to the caller.

**Q2. What happens if a function has no return statement?**

It returns `None` automatically.

**Q3. What is the difference between print() and return?**

`print()` displays information, whereas `return` sends a value back to the caller.

**Q4. Can a function return multiple values?**

Yes. Python packs multiple returned values into a tuple.

**Q5. What is early return?**

Returning a value immediately when a particular condition is satisfied.

**Q6. Can return be used inside a loop?**

Yes. It immediately terminates the function when executed.

**Q7. Can a function return a list?**

Yes. Functions can return lists and other Python objects.

**Q8. What is None in Python?**

`None` represents the absence of a value.

**Q9. Can we use the returned value of one function inside another function?**

Yes. The returned value can be passed to or used inside another function.

**Q10. Does return terminate a function?**

Yes. Once a return statement executes, the function stops.

## 17. Practice Programs

1. Create a function that returns the sum of two numbers.
2. Create a function that returns the square of a number.
3. Create a function that returns the cube of a number.
4. Create a function that returns True if a number is even.
5. Create a function that returns the largest of three numbers.
6. Create a function that returns the factorial of a number.
7. Create a function that returns the reverse of a string.
8. Create a function that returns a list of even numbers.
9. Create a function that returns the maximum and minimum values of a list.
10. Create a function that returns the sum and average of a list.
11. Create a function that checks whether a string is a palindrome.
12. Create a function that returns the number of vowels in a string.
13. Create a function that returns the frequency of each character in a string.
14. Create a function that searches for an element in a list.
15. Create a function that returns all duplicate elements in a list.

---

## Important for Placements

Understand these concepts thoroughly:

- Difference between print() and return.
- Returning single and multiple values.
- Returning lists and dictionaries.
- Return with conditions.
- Early return.
- Return inside loops.
- Using one function's return value in another function.

**Remember:** Most DSA solutions use functions that return the calculated answer instead of simply printing it.

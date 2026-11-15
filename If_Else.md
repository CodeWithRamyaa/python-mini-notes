# Python If-Else Statements

## 1. What is a Conditional Statement?

Conditional statements are used to execute different blocks of code depending on whether a condition is True or False.

Python provides the following conditional statements:

1. if statement
2. if-else statement
3. if-elif-else statement
4. Nested if statement

## 2. if Statement

The if statement executes a block of code only when the given condition is True.

### Syntax

```python
if condition:
    statement
```

### Example

```python
age = 20

if age >= 18:
    print("Eligible to vote")
```

Output:

```text
Eligible to vote
```

## 3. if-else Statement

The if-else statement executes one block when the condition is True and another block when it is False.

### Syntax

```python
if condition:
    statement1
else:
    statement2
```

### Example

```python
number = 7

if number % 2 == 0:
    print("Even number")
else:
    print("Odd number")
```

Output:

```text
Odd number
```

## 4. if-elif-else Statement

The if-elif-else statement is used to check multiple conditions.

Python executes the first block whose condition is True. If none are True, the else block executes.

### Syntax

```python
if condition1:
    statement1
elif condition2:
    statement2
else:
    statement3
```

### Example

```python
marks = 85

if marks >= 90:
    print("Grade A")
elif marks >= 75:
    print("Grade B")
elif marks >= 50:
    print("Grade C")
else:
    print("Fail")
```

Output:

```text
Grade B
```

## 5. Nested if Statement

A nested if statement means placing one if statement inside another if statement.

### Example

```python
age = 20
has_id = True

if age >= 18:
    if has_id:
        print("Entry allowed")
    else:
        print("ID required")
else:
    print("Entry not allowed")
```

Output:

```text
Entry allowed
```

## 6. Short-Hand if Statement

Python allows writing a simple if statement in one line.

### Example

```python
age = 20

if age >= 18: print("Adult")
```

Output:

```text
Adult
```

## 7. Short-Hand if-else (Ternary Operator)

A conditional expression allows writing if-else logic in one line.

### Syntax

```python
value_if_true if condition else value_if_false
```

### Example

```python
age = 16

result = "Adult" if age >= 18 else "Minor"

print(result)
```

Output:

```text
Minor
```

## 8. The pass Statement

The pass statement is used as a placeholder when a statement is required syntactically but no action needs to be performed.

### Example

```python
age = 20

if age >= 18:
    pass
else:
    print("Minor")
```

## 9. Indentation in Conditional Statements

Indentation refers to the spaces at the beginning of a code line.

Python uses indentation to identify blocks of code.

Example:

```python
number = 10

if number > 0:
    print("Positive number")
```

Incorrect indentation can cause an IndentationError.

## 10. Real-World Applications

Conditional statements are used in:

- Login authentication
- Student grading systems
- Banking applications
- Age verification
- Eligibility checking
- Decision-making programs

## 11. Important Interview Questions

**Q1. What is a conditional statement?**

A conditional statement executes code based on whether a condition is True or False.

**Q2. What is the difference between if and if-else?**

The if statement executes code only when its condition is True. The if-else statement provides an alternative block when the condition is False.

**Q3. What is elif?**

elif is used to check additional conditions when previous conditions are False.

**Q4. What is a nested if statement?**

A nested if statement is an if statement placed inside another if statement.

**Q5. What is the ternary operator in Python?**

It is a one-line conditional expression used to choose between two values.

**Q6. Why is indentation important in Python?**

Indentation defines code blocks and determines which statements belong together.

**Q7. What is the purpose of pass?**

It acts as a placeholder and performs no operation.

## Conclusion

Conditional statements help Python programs make decisions and execute different operations based on specified conditions.

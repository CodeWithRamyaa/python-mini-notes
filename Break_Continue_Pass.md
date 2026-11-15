# Python Break, Continue and Pass Statements

## 1. Introduction

Python provides three important control statements:

1. break
2. continue
3. pass

These statements control the execution of loops and conditional blocks.

## 2. Break Statement

The break statement is used to terminate a loop immediately when a particular condition is satisfied.

### Syntax

```python
break
```

### Example

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

Explanation:

When i becomes 4, the break statement terminates the loop.

### Break in While Loop

```python
i = 1

while i <= 5:
    if i == 3:
        break
    print(i)
    i += 1
```

Output:

```text
1
2
```

## 3. Continue Statement

The continue statement skips the remaining statements in the current iteration and moves to the next iteration.

### Syntax

```python
continue
```

### Example

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

Explanation:

When i becomes 3, that iteration is skipped.

### Continue in While Loop

```python
i = 0

while i < 5:
    i += 1

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

## 4. Pass Statement

The pass statement is a null statement. It does nothing when executed.

It is used as a placeholder when a statement is required syntactically but the implementation is not yet available.

### Syntax

```python
pass
```

### Example

```python
for i in range(5):
    if i == 3:
        pass
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

Explanation:

The pass statement does not terminate or skip the loop. Execution continues normally.

### Pass in Conditional Statements

```python
age = 20

if age >= 18:
    pass
else:
    print("Minor")
```

Output:

No output.

## 5. Difference Between Break, Continue and Pass

| Statement | Purpose |
|---|---|
| break | Terminates the loop. |
| continue | Skips the current iteration. |
| pass | Performs no operation. |

## 6. Real-World Applications

**Break:**
- Stopping a search after finding an element.
- Exiting a menu-driven loop.
- Ending a loop when a condition is satisfied.

**Continue:**
- Skipping invalid records.
- Ignoring unwanted values.
- Processing only selected data.

**Pass:**
- Creating placeholder functions.
- Developing program structures.
- Leaving code blocks temporarily empty.

## 7. Important Interview Questions

**Q1. What is the break statement?**

It immediately terminates the nearest enclosing loop.

**Q2. What is the continue statement?**

It skips the remaining statements in the current iteration and proceeds to the next iteration.

**Q3. What is the pass statement?**

It is a null statement that performs no operation.

**Q4. What is the difference between break and continue?**

break terminates the loop, whereas continue skips only the current iteration.

**Q5. Does pass terminate a loop?**

No. It does nothing and allows normal execution to continue.

**Q6. Can break and continue be used in nested loops?**

Yes. They affect the nearest enclosing loop in which they appear.

**Q7. Can pass be used inside a function?**

Yes. It can be used as a placeholder for an empty function body.

## Conclusion

Break, continue and pass are important Python control statements used to manage program execution and loop behaviour.

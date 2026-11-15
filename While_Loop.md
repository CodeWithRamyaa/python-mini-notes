# Python While Loop

## 1. What is a While Loop?

A while loop is used to execute a block of code repeatedly as long as a given condition is True.

It is useful when the number of iterations is not known in advance.

## 2. Syntax

```python
while condition:
    statements
```

The loop continues executing until the condition becomes False.

## 3. Simple While Loop

Example:

```python
i = 1

while i <= 5:
    print(i)
    i += 1
```

Output:

```text
1
2
3
4
5
```

## 4. While Loop with a Counter

A counter variable controls how many times the loop executes.

Example:

```python
count = 1

while count <= 3:
    print("Python Programming")
    count += 1
```

Output:

```text
Python Programming
Python Programming
Python Programming
```

## 5. While Loop with Else

Python allows an else block with a while loop.

The else block executes when the loop condition becomes False through normal completion.

Example:

```python
i = 1

while i <= 3:
    print(i)
    i += 1
else:
    print("Loop completed")
```

Output:

```text
1
2
3
Loop completed
```

## 6. Infinite While Loop

An infinite loop occurs when the condition always remains True.

Example:

```python
while True:
    print("Hello")
```

This loop continues until it is interrupted.

Note: Infinite loops should be used carefully.

## 7. Using break in a While Loop

The break statement terminates the loop immediately.

Example:

```python
i = 1

while i <= 5:
    if i == 4:
        break
    print(i)
    i += 1
```

Output:

```text
1
2
3
```

## 8. Using continue in a While Loop

The continue statement skips the remaining statements in the current iteration.

Example:

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

## 9. Difference Between For Loop and While Loop

| For Loop | While Loop |
|---|---|
| Used to iterate over a sequence or iterable. | Used to repeat while a condition is True. |
| Commonly used when iterating over a collection. | Commonly used when the stopping condition controls repetition. |
| Often uses range(). | Uses a Boolean condition. |
| Iterates over available items. | Continues until its condition becomes False or it is terminated. |

## 10. Real-World Applications

While loops are used in:

- Menu-driven programs.
- Repeated user input.
- Game loops.
- Input validation.
- Searching operations.
- Programs that wait for a condition.

## 11. Important Interview Questions

**Q1. What is a while loop?**

A while loop repeatedly executes a block of code as long as a condition is True.

**Q2. What happens if the condition is always True?**

The loop becomes infinite unless it is interrupted.

**Q3. What is the difference between for and while loops?**

A for loop iterates over an iterable, whereas a while loop repeats based on a condition.

**Q4. Can we use break in a while loop?**

Yes. It terminates the loop immediately.

**Q5. What is the purpose of continue?**

It skips the current iteration and moves to the next one.

**Q6. Can a while loop have an else block?**

Yes. The else block executes when the loop finishes normally because its condition becomes False.

**Q7. Why should we update the counter variable?**

To ensure the condition eventually becomes False and prevent an unintended infinite loop.

## Conclusion

While loops are useful for repeating operations until a particular condition is satisfied.

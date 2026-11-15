# Python Tuples

## 1. What is a Tuple?

A tuple is a built-in Python data structure used to store multiple elements in a single variable.

Tuples are created using parentheses `()`.

Example:

```python
fruits = ("Apple", "Banana", "Orange")

print(fruits)
```

Output:

```text
('Apple', 'Banana', 'Orange')
```

## 2. Features of Tuples

- Ordered collection.
- Immutable (cannot be modified after creation).
- Allows duplicate elements.
- Supports different data types.
- Supports indexing and slicing.
- Can contain nested tuples.

## 3. Creating a Tuple

```python
numbers = (10, 20, 30, 40)

names = ("Ramya", "Anu", "Ravi")

mixed = (10, "Python", 20.5, True)

empty = ()

print(numbers)
print(names)
print(mixed)
print(empty)
```

Output:

```text
(10, 20, 30, 40)
('Ramya', 'Anu', 'Ravi')
(10, 'Python', 20.5, True)
()
```

## 4. Creating a Single-Element Tuple

A comma is required when creating a tuple with one element.

Example:

```python
a = (10,)
b = (10)

print(type(a))
print(type(b))
```

Output:

```text
<class 'tuple'>
<class 'int'>
```

## 5. Accessing Tuple Elements

Tuple elements can be accessed using indexing.

Indexing starts from 0.

Example:

```python
fruits = ("Apple", "Banana", "Orange")

print(fruits[0])
print(fruits[1])
print(fruits[2])
```

Output:

```text
Apple
Banana
Orange
```

### Negative Indexing

Negative indexing accesses elements from the end.

```python
fruits = ("Apple", "Banana", "Orange")

print(fruits[-1])
print(fruits[-2])
```

Output:

```text
Orange
Banana
```

## 6. Tuple Slicing

Slicing extracts a portion of a tuple.

Syntax:

```python
tuple[start:stop:step]
```

Example:

```python
numbers = (10, 20, 30, 40, 50)

print(numbers[1:4])
print(numbers[:3])
print(numbers[2:])
```

Output:

```text
(20, 30, 40)
(10, 20, 30)
(30, 40, 50)
```

The stop index is excluded.

## 7. Tuple Immutability

Tuples cannot be modified after creation.

Example:

```python
numbers = (10, 20, 30)

numbers[1] = 50

print(numbers)
```

Output:

```text
TypeError: 'tuple' object does not support item assignment
```

Note: Although a tuple cannot be modified, it may contain mutable objects such as lists. Those nested objects can still be modified.

## 8. Tuple Methods

Python provides two main built-in tuple methods.

| Method | Description |
|---|---|
| count() | Returns the number of occurrences of a value |
| index() | Returns the index of the first occurrence |

### A. count()

```python
numbers = (10, 20, 10, 30, 10)

print(numbers.count(10))
```

Output:

```text
3
```

### B. index()

```python
numbers = (10, 20, 30, 40)

print(numbers.index(30))
```

Output:

```text
2
```

## 9. Finding the Length of a Tuple

The len() function returns the number of elements.

```python
numbers = (10, 20, 30, 40)

print(len(numbers))
```

Output:

```text
4
```

## 10. Tuple Concatenation

The + operator combines two tuples.

```python
a = (10, 20)
b = (30, 40)

result = a + b

print(result)
```

Output:

```text
(10, 20, 30, 40)
```

## 11. Tuple Repetition

The * operator repeats tuple elements.

```python
numbers = (10, 20)

print(numbers * 3)
```

Output:

```text
(10, 20, 10, 20, 10, 20)
```

## 12. Checking Elements in a Tuple

The in and not in operators check whether an element exists.

```python
fruits = ("Apple", "Banana", "Orange")

print("Apple" in fruits)
print("Mango" not in fruits)
```

Output:

```text
True
True
```

## 13. Tuple Traversal Using a Loop

A for loop can access each tuple element.

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

## 14. Nested Tuples

A nested tuple is a tuple containing other tuples.

```python
matrix = (
    (1, 2, 3),
    (4, 5, 6),
    (7, 8, 9)
)

print(matrix[0])
print(matrix[1][2])
```

Output:

```text
(1, 2, 3)
6
```

## 15. Tuple Packing and Unpacking

### Tuple Packing

Assigning multiple values to a single tuple is called packing.

```python
student = ("Ramya", 20, 90)

print(student)
```

Output:

```text
('Ramya', 20, 90)
```

### Tuple Unpacking

Assigning tuple elements to separate variables is called unpacking.

```python
student = ("Ramya", 20, 90)

name, age, marks = student

print(name)
print(age)
print(marks)
```

Output:

```text
Ramya
20
90
```

## 16. Converting a List into a Tuple

The tuple() function converts an iterable into a tuple.

```python
numbers = [10, 20, 30]

result = tuple(numbers)

print(result)
```

Output:

```text
(10, 20, 30)
```

## 17. Difference Between List and Tuple

| List | Tuple |
|---|---|
| Uses square brackets [] | Uses parentheses () |
| Mutable | Immutable |
| More modification methods | Only count() and index() methods |
| Suitable for changeable collections | Suitable for collections that should remain fixed |

## 18. Applications of Tuples

Tuples are commonly used in:

- Storing fixed data.
- Representing coordinates.
- Returning multiple values from functions.
- Storing database records.
- Representing RGB colour values.

## 19. Important Interview Questions

**Q1. What is a tuple in Python?**

A tuple is an ordered and immutable collection of elements.

**Q2. Are tuples mutable?**

No, tuples are immutable.

**Q3. Which brackets are used to create tuples?**

Parentheses ().

**Q4. Can tuples contain duplicate values?**

Yes.

**Q5. How do you create a single-element tuple?**

By placing a comma after the element, such as `(10,)`.

**Q6. What are the built-in tuple methods?**

count() and index().

**Q7. What is tuple unpacking?**

It is the process of assigning tuple elements to separate variables.

**Q8. What is the difference between a list and a tuple?**

A list is mutable, whereas a tuple is immutable.

**Q9. Can a tuple contain a list?**

Yes. A tuple can contain mutable objects such as lists.

**Q10. How do you find the length of a tuple?**

Using the len() function.

## 20. Conclusion

Tuples are useful Python data structures for storing ordered collections of elements that should not be structurally modified after creation.

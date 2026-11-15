# Python Lists

## 1. What is a List?

A list is a built-in Python data structure used to store multiple items in a single variable.

Lists are created using square brackets `[]`.

### Example

```python
fruits = ["Apple", "Banana", "Orange"]

print(fruits)
```

Output:

```text
['Apple', 'Banana', 'Orange']
```

## 2. Features of Lists

- Ordered collection.
- Mutable (can be modified).
- Allows duplicate elements.
- Can store different data types.
- Supports indexing and slicing.
- Can contain nested lists.

## 3. Creating a List

```python
numbers = [10, 20, 30, 40]

names = ["Ramya", "Anu", "Ravi"]

mixed = [10, "Python", 20.5, True]

empty = []

print(numbers)
print(names)
print(mixed)
print(empty)
```

Output:

```text
[10, 20, 30, 40]
['Ramya', 'Anu', 'Ravi']
[10, 'Python', 20.5, True]
[]
```

## 4. Accessing List Elements

List elements can be accessed using indexing.

Indexing starts from 0.

```python
fruits = ["Apple", "Banana", "Orange"]

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

Negative indexing accesses elements from the end of the list.

```python
fruits = ["Apple", "Banana", "Orange"]

print(fruits[-1])
print(fruits[-2])
```

Output:

```text
Orange
Banana
```

## 5. List Slicing

Slicing is used to access a specific portion of a list.

### Syntax

```python
list[start:stop:step]
```

Example:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[1:4])
print(numbers[:3])
print(numbers[2:])
```

Output:

```text
[20, 30, 40]
[10, 20, 30]
[30, 40, 50]
```

The stop index is excluded.

## 6. Modifying List Elements

Lists are mutable, so their elements can be changed.

```python
fruits = ["Apple", "Banana", "Orange"]

fruits[1] = "Mango"

print(fruits)
```

Output:

```text
['Apple', 'Mango', 'Orange']
```

## 7. Adding Elements to a List

Python provides different methods to add elements.

### A. append()

Adds an element at the end of the list.

```python
numbers = [10, 20, 30]

numbers.append(40)

print(numbers)
```

Output:

```text
[10, 20, 30, 40]
```

### B. insert()

Adds an element at a specified position.

```python
numbers = [10, 20, 30]

numbers.insert(1, 15)

print(numbers)
```

Output:

```text
[10, 15, 20, 30]
```

### C. extend()

Adds elements from another iterable to the end of a list.

```python
a = [10, 20]
b = [30, 40]

a.extend(b)

print(a)
```

Output:

```text
[10, 20, 30, 40]
```

## 8. Removing Elements from a List

### A. remove()

Removes the first occurrence of a specified value.

```python
numbers = [10, 20, 30, 20]

numbers.remove(20)

print(numbers)
```

Output:

```text
[10, 30, 20]
```

### B. pop()

Removes and returns an element at a specified index. If no index is provided, it removes the last element.

```python
numbers = [10, 20, 30]

numbers.pop()

print(numbers)
```

Output:

```text
[10, 20]
```

### C. del

Deletes an element or a slice.

```python
numbers = [10, 20, 30, 40]

del numbers[1]

print(numbers)
```

Output:

```text
[10, 30, 40]
```

### D. clear()

Removes all elements from the list.

```python
numbers = [10, 20, 30]

numbers.clear()

print(numbers)
```

Output:

```text
[]
```

## 9. Important List Methods

| Method | Description |
|---|---|
| append() | Adds an element at the end |
| insert() | Adds an element at a specific position |
| extend() | Adds multiple elements |
| remove() | Removes the first matching value |
| pop() | Removes and returns an element |
| clear() | Removes all elements |
| index() | Returns the index of a value |
| count() | Counts occurrences |
| sort() | Sorts the list |
| reverse() | Reverses the list |
| copy() | Creates a shallow copy |

## 10. Sorting a List

The sort() method arranges elements in ascending or descending order.

### Ascending Order

```python
numbers = [40, 10, 30, 20]

numbers.sort()

print(numbers)
```

Output:

```text
[10, 20, 30, 40]
```

### Descending Order

```python
numbers = [40, 10, 30, 20]

numbers.sort(reverse=True)

print(numbers)
```

Output:

```text
[40, 30, 20, 10]
```

## 11. Searching in a List

The in operator checks whether an element exists in a list.

```python
numbers = [10, 20, 30, 40]

if 20 in numbers:
    print("Element found")
else:
    print("Element not found")
```

Output:

```text
Element found
```

## 12. Finding Length of a List

The len() function returns the number of elements.

```python
numbers = [10, 20, 30, 40]

print(len(numbers))
```

Output:

```text
4
```

## 13. List Traversal Using a Loop

A for loop can access each element in a list.

```python
numbers = [10, 20, 30]

for num in numbers:
    print(num)
```

Output:

```text
10
20
30
```

## 14. Nested Lists

A nested list is a list containing other lists as elements.

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

print(matrix[0])
print(matrix[1][2])
```

Output:

```text
[1, 2, 3]
6
```

## 15. List Comprehension

List comprehension provides a short way to create a new list.

### Example

```python
numbers = [1, 2, 3, 4, 5]

squares = [x * x for x in numbers]

print(squares)
```

Output:

```text
[1, 4, 9, 16, 25]
```

## 16. List Operations

Python supports several operations on lists.

```python
a = [10, 20]
b = [30, 40]

print(a + b)
print(a * 2)
print(20 in a)
```

Output:

```text
[10, 20, 30, 40]
[10, 20, 10, 20]
True
```

## 17. Important Interview Questions

**Q1. What is a list in Python?**

A list is an ordered and mutable collection used to store multiple elements.

**Q2. Are lists mutable?**

Yes, list elements can be modified after creation.

**Q3. Can lists contain duplicate values?**

Yes.

**Q4. Which brackets are used to create lists?**

Square brackets [].

**Q5. What is the difference between append() and extend()?**

append() adds one object as an element, whereas extend() adds elements from an iterable individually.

**Q6. What is the difference between remove() and pop()?**

remove() deletes a specified value, whereas pop() removes and returns an element by index.

**Q7. What is list slicing?**

It extracts a portion of a list using index positions.

**Q8. What is list comprehension?**

It is a concise way to create lists using an expression and an iterable.

**Q9. What does len() do?**

It returns the number of elements in a list.

**Q10. Can a list contain different data types?**

Yes.

## 18. Conclusion

Lists are one of the most commonly used Python data structures. They provide flexible ways to store, access, modify, search and organize data.

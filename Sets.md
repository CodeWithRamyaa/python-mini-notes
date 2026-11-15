# Python Sets

## 1. Introduction to Sets

A **set** in Python is a collection of unique elements. Sets are unordered, meaning they do not maintain a guaranteed position for their elements.

### Features of Sets
- Stores unique elements only.
- Does not support indexing or slicing.
- Is mutable, so elements can be added or removed.
- Does not allow duplicate values.
- Can store elements of different data types.
- Elements must be hashable.

### Example

```python
numbers = {10, 20, 30, 20, 40}
print(numbers)
```

**Output:**
```text
{40, 10, 20, 30}
```

*Note: The order of elements may vary.*

---

## 2. Creating a Set

Sets are created using curly braces `{}` or the `set()` constructor.

```python
fruits = {"apple", "banana", "mango"}
print(fruits)
```

**Output:** (order may vary)
```text
{'apple', 'banana', 'mango'}
```

### Creating an Empty Set

```python
empty_set = set()
print(empty_set)
```

**Output:**
```text
set()
```

**Important:** `{}` creates an empty dictionary, not an empty set.

---

## 3. Adding Elements

The `add()` method adds one element to a set.

### Syntax
```python
set_name.add(element)
```

### Example
```python
numbers = {10, 20, 30}
numbers.add(40)

print(sorted(numbers))
```

**Output:**
```text
[10, 20, 30, 40]
```

---

## 4. Adding Multiple Elements

The `update()` method adds multiple elements from another iterable.

### Syntax
```python
set_name.update(iterable)
```

### Example
```python
numbers = {10, 20}
numbers.update([30, 40, 50])

print(sorted(numbers))
```

**Output:**
```text
[10, 20, 30, 40, 50]
```

---

## 5. Removing Elements

Python provides different methods to remove elements from a set.

### A. remove()

Removes the specified element. It raises a `KeyError` if the element does not exist.

```python
numbers = {10, 20, 30}
numbers.remove(20)

print(sorted(numbers))
```

**Output:**
```text
[10, 30]
```

### B. discard()

Removes the specified element. It does not raise an error if the element is missing.

```python
numbers = {10, 20, 30}
numbers.discard(50)

print(sorted(numbers))
```

**Output:**
```text
[10, 20, 30]
```

### C. pop()

Removes and returns an arbitrary element from the set.

```python
numbers = {10, 20, 30}
removed = numbers.pop()

print("Removed:", removed)
print("Remaining:", sorted(numbers))
```

*Note: The removed element is not guaranteed to be a particular value.*

### D. clear()

Removes all elements from the set.

```python
numbers = {10, 20, 30}
numbers.clear()

print(numbers)
```

**Output:**
```text
set()
```

---

## 6. Set Operations

Python supports mathematical set operations.

### A. Union

Union combines all unique elements from two sets.

**Operator:** `|`

**Method:** `union()`

```python
A = {1, 2, 3}
B = {3, 4, 5}

print(sorted(A | B))
```

**Output:**
```text
[1, 2, 3, 4, 5]
```

### B. Intersection

Intersection returns only the common elements.

**Operator:** `&`

**Method:** `intersection()`

```python
A = {1, 2, 3}
B = {3, 4, 5}

print(sorted(A & B))
```

**Output:**
```text
[3]
```

### C. Difference

Difference returns elements present in the first set but not in the second.

**Operator:** `-`

**Method:** `difference()`

```python
A = {1, 2, 3}
B = {3, 4, 5}

print(sorted(A - B))
```

**Output:**
```text
[1, 2]
```

### D. Symmetric Difference

Returns elements present in either set, but not in both.

**Operator:** `^`

**Method:** `symmetric_difference()`

```python
A = {1, 2, 3}
B = {3, 4, 5}

print(sorted(A ^ B))
```

**Output:**
```text
[1, 2, 4, 5]
```

---

## 7. Set Comparison Methods

### A. issubset()

Checks whether all elements of one set are present in another set.

```python
A = {1, 2}
B = {1, 2, 3, 4}

print(A.issubset(B))
```

**Output:**
```text
True
```

### B. issuperset()

Checks whether a set contains all elements of another set.

```python
A = {1, 2, 3, 4}
B = {1, 2}

print(A.issuperset(B))
```

**Output:**
```text
True
```

### C. isdisjoint()

Checks whether two sets have no common elements.

```python
A = {1, 2}
B = {3, 4}

print(A.isdisjoint(B))
```

**Output:**
```text
True
```

---

## 8. Membership Testing

The `in` and `not in` operators check whether an element exists in a set.

```python
fruits = {"apple", "banana", "mango"}

print("apple" in fruits)
print("orange" not in fruits)
```

**Output:**
```text
True
True
```

---

## 9. Traversing a Set

A `for` loop can be used to access set elements.

```python
fruits = {"apple", "banana", "mango"}

for fruit in sorted(fruits):
    print(fruit)
```

**Output:**
```text
apple
banana
mango
```

---

## 10. Frozenset

A `frozenset` is an immutable version of a set. Once created, its elements cannot be added or removed.

### Example

```python
numbers = frozenset([10, 20, 30])

print(numbers)
```

**Output:**
```text
frozenset({10, 20, 30})
```

Unlike a normal set, a frozenset does not support methods such as `add()` or `remove()`.

---

## 11. Set vs List vs Tuple

| Feature | List | Tuple | Set |
|---|---|---|---|
| Syntax | `[]` | `()` | `{}` |
| Ordered | Yes | Yes | No guaranteed order |
| Mutable | Yes | No | Yes |
| Duplicates | Allowed | Allowed | Not allowed |
| Indexing | Supported | Supported | Not supported |
| Slicing | Supported | Supported | Not supported |

---

## 12. Applications of Sets

Sets are useful for:

1. Removing duplicate values from a collection.
2. Finding common elements between two collections.
3. Finding differences between collections.
4. Checking membership efficiently.
5. Comparing student groups or categories.
6. Performing mathematical set operations.

### Example: Removing Duplicates from a List

```python
numbers = [10, 20, 10, 30, 20, 40]

unique_numbers = set(numbers)

print(sorted(unique_numbers))
```

**Output:**
```text
[10, 20, 30, 40]
```

---

## 13. Important Interview Questions

**Q1. What is a set in Python?**

A set is an unordered collection of unique elements.

**Q2. Can a set contain duplicate values?**

No. Sets automatically remove duplicate values.

**Q3. How do you create an empty set?**

Using `set()`. Empty curly braces `{}` create a dictionary.

**Q4. Does a set support indexing?**

No. Sets do not support indexing or slicing.

**Q5. What is the difference between remove() and discard()?**

`remove()` raises a `KeyError` if the element is missing, whereas `discard()` does not.

**Q6. What is the difference between a set and a frozenset?**

A set is mutable, whereas a frozenset is immutable.

**Q7. What is the use of the union operation?**

It combines unique elements from two or more sets.

**Q8. What is the use of the intersection operation?**

It returns the common elements between sets.

**Q9. Can a set contain a list?**

No. Lists are unhashable and cannot be set elements.

**Q10. Which method removes all elements from a set?**

The `clear()` method.

---

## 14. Conclusion

Sets are useful Python data structures for storing unique elements and performing mathematical operations. They help remove duplicates, compare collections, and find common or different elements efficiently.

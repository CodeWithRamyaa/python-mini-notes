# Python Dictionaries

## 1. What is a Dictionary?

A dictionary is a built-in Python data type used to store data in **key-value pairs**.

Each key is connected to a value.

Think of a dictionary like a student record:
- Key: Student Name
- Value: Ramya

### Example

```python
student = {
    "name": "Ramya",
    "age": 20,
    "course": "AI & DS"
}

print(student)
```

**Output:**
```text
{'name': 'Ramya', 'age': 20, 'course': 'AI & DS'}
```

## 2. Features of Dictionaries

- Stores data in key-value pairs.
- Dictionaries are ordered.
- Dictionaries are mutable (can be modified).
- Keys must be unique.
- Values can be duplicated.
- Keys must be immutable types such as strings, numbers or tuples.
- Values can contain different data types.

## 3. Creating a Dictionary

### Syntax

```python
dictionary_name = {
    key1: value1,
    key2: value2
}
```

### Example

```python
person = {
    "name": "Rahul",
    "age": 21,
    "city": "Bangalore"
}

print(person)
```

## 4. Accessing Dictionary Elements

We can access values using their keys.

### Using Square Brackets

```python
student = {"name": "Ramya", "age": 20}

print(student["name"])
print(student["age"])
```

**Output:**
```text
Ramya
20
```

### Using get()

The `get()` method retrieves a value without raising a KeyError if the key is missing.

```python
student = {"name": "Ramya", "age": 20}

print(student.get("name"))
print(student.get("marks"))
```

**Output:**
```text
Ramya
None
```

We can also provide a default value:

```python
print(student.get("marks", 0))
```

**Output:**
```text
0
```

## 5. Adding Elements

We can add a new key-value pair by assigning a value to a new key.

```python
student = {"name": "Ramya", "age": 20}

student["marks"] = 90

print(student)
```

**Output:**
```text
{'name': 'Ramya', 'age': 20, 'marks': 90}
```

## 6. Updating Elements

We can change an existing value by assigning a new value to its key.

```python
student = {"name": "Ramya", "age": 20}

student["age"] = 21

print(student)
```

**Output:**
```text
{'name': 'Ramya', 'age': 21}
```

### Using update()

```python
student = {"name": "Ramya", "age": 20}

student.update({"age": 21, "marks": 90})

print(student)
```

**Output:**
```text
{'name': 'Ramya', 'age': 21, 'marks': 90}
```

## 7. Removing Elements

### pop()

Removes an element using its key and returns its value.

```python
student = {"name": "Ramya", "age": 20}

student.pop("age")

print(student)
```

**Output:**
```text
{'name': 'Ramya'}
```

### popitem()

Removes and returns the last inserted key-value pair.

```python
student = {"name": "Ramya", "age": 20}

student.popitem()

print(student)
```

**Output:**
```text
{'name': 'Ramya'}
```

### del

Deletes an element using its key.

```python
student = {"name": "Ramya", "age": 20}

del student["age"]

print(student)
```

### clear()

Removes all elements.

```python
student = {"name": "Ramya", "age": 20}

student.clear()

print(student)
```

**Output:**
```text
{}
```

## 8. Dictionary Methods

| Method | Description |
|---|---|
| `get()` | Returns the value of a key |
| `keys()` | Returns all keys |
| `values()` | Returns all values |
| `items()` | Returns key-value pairs |
| `update()` | Adds or updates elements |
| `pop()` | Removes an element using its key |
| `popitem()` | Removes the last inserted pair |
| `clear()` | Removes all elements |
| `copy()` | Creates a shallow copy |
| `setdefault()` | Returns a value or inserts a default |
| `fromkeys()` | Creates a dictionary from given keys |

## 9. Looping Through a Dictionary

### Loop Through Keys

```python
student = {"name": "Ramya", "age": 20, "marks": 90}

for key in student:
    print(key)
```

**Output:**
```text
name
age
marks
```

### Loop Through Values

```python
for value in student.values():
    print(value)
```

### Loop Through Keys and Values

We use `items()` to access both keys and values.

```python
for key, value in student.items():
    print(key, value)
```

**Output:**
```text
name Ramya
age 20
marks 90
```

## 10. Checking Whether a Key Exists

We use the `in` operator to check whether a key exists.

```python
student = {"name": "Ramya", "age": 20}

if "name" in student:
    print("Key exists")
else:
    print("Key does not exist")
```

**Output:**
```text
Key exists
```

## 11. Dictionary Length

The `len()` function returns the number of key-value pairs.

```python
student = {
    "name": "Ramya",
    "age": 20,
    "marks": 90
}

print(len(student))
```

**Output:**
```text
3
```

## 12. Nested Dictionaries

A dictionary can contain another dictionary.

```python
students = {
    "student1": {
        "name": "Ramya",
        "age": 20
    },
    "student2": {
        "name": "Rahul",
        "age": 21
    }
}

print(students["student1"]["name"])
```

**Output:**
```text
Ramya
```

## 13. Dictionary Comprehension

Dictionary comprehension provides a shorter way to create dictionaries.

### Syntax

```python
new_dictionary = {key: value for item in iterable}
```

### Example

```python
numbers = [1, 2, 3, 4, 5]

squares = {n: n*n for n in numbers}

print(squares)
```

**Output:**
```text
{1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

## 14. Common Mistakes

1. Accessing a missing key using square brackets causes a `KeyError`.
2. Dictionary keys must be unique.
3. Dictionaries use keys to access values, not numerical indexes.
4. Using an unhashable object such as a list as a key causes a `TypeError`.
5. `pop()` requires a key unless a default value is supplied.
6. Dictionary values can be duplicated, but keys cannot be duplicated.

## 15. Real-World Applications

- Storing student information.
- Managing employee records.
- Storing product details.
- Maintaining contact information.
- Representing JSON data.
- Counting word or character frequencies.
- Storing configuration settings.

## 16. Important Interview Questions

**Q1. What is a dictionary in Python?**

A dictionary is a built-in data type that stores information in key-value pairs.

**Q2. Are dictionaries mutable?**

Yes. We can add, update and remove elements.

**Q3. Can dictionary keys be duplicated?**

No. Every key must be unique.

**Q4. Can dictionary values be duplicated?**

Yes. Multiple keys can have the same value.

**Q5. What is the difference between get() and square brackets?**

Square brackets raise a KeyError if a key is missing, whereas `get()` returns None or a specified default value.

**Q6. What does items() return?**

It returns a view containing key-value pairs.

**Q7. What is a nested dictionary?**

A dictionary containing another dictionary as its value.

**Q8. What is the difference between pop() and popitem()?**

`pop()` removes an element using a specified key, whereas `popitem()` removes the last inserted pair.

**Q9. Can a dictionary contain different data types?**

Yes. Both keys and values can contain different supported data types.

**Q10. What is dictionary comprehension?**

It is a shorter way of creating dictionaries using a single expression.

## 17. Practice Programs

1. Create a dictionary containing student details.
2. Add a new key-value pair to an existing dictionary.
3. Update the marks of a student.
4. Find the length of a dictionary.
5. Print all dictionary keys.
6. Print all dictionary values.
7. Check whether a particular key exists.
8. Find the sum of all numeric values in a dictionary.
9. Count the frequency of each element in a list using a dictionary.
10. Find the key with the maximum value in a dictionary.

---

**Remember:** Dictionaries are especially important in DSA because they help solve frequency-counting, duplicate detection and lookup problems efficiently.

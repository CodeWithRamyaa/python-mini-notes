# Python Function Arguments

## 1. What are Function Arguments?

Function arguments are the actual values passed to a function when calling it.

They provide information that a function needs to perform a task.

### Example

```python
def greet(name):
    print("Hello", name)

greet("Ramya")
```

**Output:**
```text
Hello Ramya
```

Explanation:
- `name` is a parameter.
- `"Ramya"` is an argument.
- The argument is passed when the function is called.

## 2. Difference Between Parameters and Arguments

| Parameters | Arguments |
|---|---|
| Variables defined in a function definition | Actual values passed during a function call |
| Receive information | Provide information |
| Example: `name` | Example: `"Ramya"` |

Example:

```python
def add(a, b):
    print(a + b)

add(10, 20)
```

Here:
- `a` and `b` are parameters.
- `10` and `20` are arguments.

## 3. Types of Function Arguments

Python supports different ways of passing arguments.

1. Positional Arguments
2. Keyword Arguments
3. Default Arguments
4. Arbitrary Positional Arguments (`*args`)
5. Arbitrary Keyword Arguments (`**kwargs`)

## 4. Positional Arguments

Positional arguments are passed according to the position of parameters.

The first argument is assigned to the first parameter, the second argument to the second parameter, and so on.

### Example

```python
def student(name, age):
    print("Name:", name)
    print("Age:", age)

student("Ramya", 20)
```

**Output:**
```text
Name: Ramya
Age: 20
```

Explanation:

- `"Ramya"` is assigned to `name`.
- `20` is assigned to `age`.

### Important

Changing the order of positional arguments changes the assigned values.

```python
def student(name, age):
    print(name)
    print(age)

student(20, "Ramya")
```

**Output:**
```text
20
Ramya
```

Python assigns values based on position, not meaning.

## 5. Keyword Arguments

Keyword arguments are passed using parameter names.

We specify which value belongs to which parameter.

### Example

```python
def student(name, age):
    print("Name:", name)
    print("Age:", age)

student(age=20, name="Ramya")
```

**Output:**
```text
Name: Ramya
Age: 20
```

Explanation:

Even though the order is changed, Python assigns the values correctly because parameter names are specified.

### Advantages

- Improves readability.
- Allows arguments to be passed in a different order.
- Makes function calls easier to understand.

## 6. Default Arguments

Default arguments are parameters that have predefined values.

If no argument is provided, Python uses the default value.

### Example

```python
def greet(name="Student"):
    print("Hello", name)

greet()
greet("Ramya")
```

**Output:**
```text
Hello Student
Hello Ramya
```

Explanation:

- First call: No argument is provided, so `"Student"` is used.
- Second call: `"Ramya"` is provided, so it replaces the default value.

### Example 2

```python
def calculate(a, b=10):
    print(a + b)

calculate(5)
calculate(5, 20)
```

**Output:**
```text
15
25
```

### Important Rule

Non-default parameters must come before default parameters.

Correct:

```python
def display(name, age=20):
    print(name, age)
```

Incorrect:

```python
def display(age=20, name):
    print(name, age)
```

The incorrect definition raises a SyntaxError.

## 7. Arbitrary Positional Arguments (*args)

Sometimes we do not know how many arguments will be passed.

We use `*args` to accept multiple positional arguments.

Python collects these arguments into a tuple.

### Syntax

```python
def function_name(*args):
    statements
```

### Example 1

```python
def add(*numbers):
    print(sum(numbers))

add(10, 20, 30)
```

**Output:**
```text
60
```

Explanation:

The values are collected into a tuple:

```python
(10, 20, 30)
```

### Example 2

```python
def display(*names):
    for name in names:
        print(name)

display("Ramya", "Rahul", "Neha")
```

**Output:**
```text
Ramya
Rahul
Neha
```

### Example 3: Find the Maximum Number

```python
def find_max(*numbers):
    print(max(numbers))

find_max(10, 50, 30, 80, 20)
```

**Output:**
```text
80
```

## 8. Arbitrary Keyword Arguments (**kwargs)

Sometimes we do not know how many keyword arguments will be passed.

We use `**kwargs` to accept multiple keyword arguments.

Python collects these arguments into a dictionary.

### Syntax

```python
def function_name(**kwargs):
    statements
```

### Example 1

```python
def student(**details):
    print(details)

student(name="Ramya", age=20, course="AI & DS")
```

**Output:**
```text
{'name': 'Ramya', 'age': 20, 'course': 'AI & DS'}
```

### Example 2: Access Dictionary Values

```python
def student(**details):
    print(details["name"])
    print(details["course"])

student(name="Ramya", course="AI & DS")
```

**Output:**
```text
Ramya
AI & DS
```

### Example 3: Loop Through kwargs

```python
def display(**details):
    for key, value in details.items():
        print(key, value)

display(name="Ramya", age=20, city="Bangalore")
```

**Output:**
```text
name Ramya
age 20
city Bangalore
```

## 9. Combining Different Types of Arguments

Python allows us to combine different argument types by following the correct parameter order.

### Example

```python
def student(name, age=20, *marks, **details):
    print(name)
    print(age)
    print(marks)
    print(details)

student("Ramya", 21, 90, 85, city="Bangalore")
```

**Output:**
```text
Ramya
21
(90, 85)
{'city': 'Bangalore'}
```

Explanation:

- `"Ramya"` goes to `name`.
- `21` goes to `age`.
- `90` and `85` are collected in `marks`.
- `city="Bangalore"` is collected in `details`.

## 10. Positional and Keyword Arguments Together

We can use positional and keyword arguments in the same function call.

However, positional arguments must come before keyword arguments.

Correct:

```python
def student(name, age):
    print(name, age)

student("Ramya", age=20)
```

**Output:**
```text
Ramya 20
```

Incorrect:

```python
student(name="Ramya", 20)
```

This raises a SyntaxError because a positional argument follows a keyword argument.

## 11. Argument Unpacking

Argument unpacking means passing elements of a collection as individual arguments.

### Using * with a List

```python
def add(a, b, c):
    print(a + b + c)

numbers = [10, 20, 30]

add(*numbers)
```

**Output:**
```text
60
```

Here, `*numbers` unpacks the list into three positional arguments.

### Using ** with a Dictionary

```python
def student(name, age):
    print(name, age)

details = {
    "name": "Ramya",
    "age": 20
}

student(**details)
```

**Output:**
```text
Ramya 20
```

Here, `**details` unpacks dictionary entries into keyword arguments.

## 12. Keyword-Only Arguments

Keyword-only arguments must be passed using their parameter names.

We use `*` to separate positional parameters from keyword-only parameters.

### Example

```python
def student(name, *, age):
    print(name, age)

student("Ramya", age=20)
```

**Output:**
```text
Ramya 20
```

Incorrect:

```python
student("Ramya", 20)
```

This raises a TypeError because `age` must be passed as a keyword argument.

## 13. Positional-Only Arguments

Positional-only arguments must be passed according to their position.

We use `/` to indicate positional-only parameters.

### Example

```python
def student(name, /, age):
    print(name, age)

student("Ramya", 20)
```

**Output:**
```text
Ramya 20
```

The following call is incorrect:

```python
student(name="Ramya", age=20)
```

It raises a TypeError because `name` is positional-only.

## 14. Mutable Default Arguments

A mutable default argument, such as a list, can retain changes between function calls.

### Problematic Example

```python
def add_item(item, items=[]):
    items.append(item)
    return items

print(add_item(10))
print(add_item(20))
```

**Output:**
```text
[10]
[10, 20]
```

Why?

Python creates the default list once when the function is defined. The same list is reused across calls.

### Recommended Approach

Use `None` as the default value.

```python
def add_item(item, items=None):
    if items is None:
        items = []

    items.append(item)
    return items

print(add_item(10))
print(add_item(20))
```

**Output:**
```text
[10]
[20]
```

## 15. Difference Between *args and **kwargs

| Feature | *args | **kwargs |
|---|---|---|
| Purpose | Accepts multiple positional arguments | Accepts multiple keyword arguments |
| Data type | Tuple | Dictionary |
| Symbol | Single asterisk | Double asterisk |
| Example | `func(10, 20)` | `func(name="Ramya")` |

## 16. Common Mistakes

1. Confusing parameters with arguments.
2. Passing the wrong number of positional arguments.
3. Placing positional arguments after keyword arguments.
4. Placing non-default parameters after default parameters.
5. Forgetting that `*args` collects values into a tuple.
6. Forgetting that `**kwargs` collects values into a dictionary.
7. Using `*` and `**` incorrectly during unpacking.
8. Passing positional-only parameters using keywords.
9. Passing keyword-only parameters positionally.
10. Using mutable objects as default arguments without understanding their behavior.

## 17. Real-World Applications

- Creating reusable functions.
- Building flexible APIs.
- Handling student and employee records.
- Processing multiple inputs.
- Developing machine learning functions.
- Writing reusable libraries.
- Passing configuration options to functions.

## 18. Important Interview Questions

**Q1. What are function arguments?**

Arguments are actual values passed to a function when it is called.

**Q2. What is the difference between positional and keyword arguments?**

Positional arguments are assigned according to position, whereas keyword arguments are assigned using parameter names.

**Q3. What are default arguments?**

Arguments that have predefined values in a function definition.

**Q4. What is *args?**

It allows a function to accept multiple positional arguments as a tuple.

**Q5. What is **kwargs?**

It allows a function to accept multiple keyword arguments as a dictionary.

**Q6. What is argument unpacking?**

It is the process of passing elements of a collection as individual function arguments.

**Q7. Can positional and keyword arguments be combined?**

Yes, but positional arguments must come before keyword arguments.

**Q8. What is a keyword-only argument?**

An argument that must be passed using its parameter name.

**Q9. What is a positional-only argument?**

An argument that must be passed according to its position.

**Q10. Why should mutable default arguments be avoided?**

Because the same mutable object can be reused across multiple function calls, causing unexpected results.

## 19. Practice Programs

1. Create a function that accepts two positional arguments.
2. Create a function that accepts keyword arguments.
3. Create a function with default arguments.
4. Create a function that accepts multiple numbers using `*args`.
5. Find the sum of all numbers using `*args`.
6. Find the maximum number using `*args`.
7. Create a function that accepts student details using `**kwargs`.
8. Print all key-value pairs using `**kwargs`.
9. Pass a list to a function using argument unpacking.
10. Pass a dictionary to a function using keyword unpacking.
11. Create a function with keyword-only arguments.
12. Create a function with positional-only arguments.
13. Create a function that accepts a name and any number of marks.
14. Create a function that calculates the average of multiple numbers.
15. Create a function that accepts employee details using `**kwargs`.

---

## Important for Placements

Make sure you understand these concepts:

- Positional arguments
- Keyword arguments
- Default arguments
- `*args`
- `**kwargs`
- Argument unpacking
- Keyword-only arguments
- Positional-only arguments

These concepts help you write flexible functions and understand how Python handles inputs.

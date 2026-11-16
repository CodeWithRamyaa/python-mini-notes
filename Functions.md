# Python Functions

## 1. What is a Function?

A function is a reusable block of code that performs a specific task.

Instead of writing the same code repeatedly, we can create a function and call it whenever required.

### Example

```python
def greet():
    print("Hello, Welcome to Python")

greet()
```

**Output:**
```text
Hello, Welcome to Python
```

Here:
- `def` is the keyword used to define a function.
- `greet` is the function name.
- `()` contains parameters, if required.
- The indented code is the function body.
- `greet()` calls the function.

## 2. Why Do We Use Functions?

Functions help us:

1. Reuse code.
2. Avoid repetition.
3. Organize programs.
4. Make code easier to understand.
5. Simplify debugging.
6. Divide large programs into smaller tasks.

## 3. Function Syntax

```python
def function_name(parameters):
    # Function body
    statements

function_name(arguments)
```

**Explanation:**

- `def`: Defines a function.
- `function_name`: Name of the function.
- `parameters`: Inputs received by the function.
- `statements`: Instructions executed by the function.
- `arguments`: Actual values passed during the function call.

## 4. Types of Functions

Python functions can be classified into two main categories.

### A. Built-in Functions

These are functions already provided by Python.

Examples:

| Function | Purpose |
|---|---|
| `print()` | Displays output |
| `len()` | Returns length |
| `max()` | Returns maximum value |
| `min()` | Returns minimum value |
| `sum()` | Calculates sum |
| `type()` | Returns data type |
| `range()` | Generates a sequence of numbers |
| `sorted()` | Returns a sorted list |
| `abs()` | Returns absolute value |

Example:

```python
numbers = [10, 20, 30, 40]

print(len(numbers))
print(max(numbers))
print(sum(numbers))
```

**Output:**
```text
4
40
100
```

### B. User-Defined Functions

These are functions created by programmers using the `def` keyword.

Example:

```python
def add():
    a = 10
    b = 20

    print(a + b)

add()
```

**Output:**
```text
30
```

## 5. Function Without Parameters

A function can work without receiving any input.

Example:

```python
def welcome():
    print("Welcome to Python Programming")

welcome()
```

**Output:**
```text
Welcome to Python Programming
```

## 6. Function With Parameters

Parameters allow us to pass information into a function.

Example:

```python
def greet(name):
    print("Hello", name)

greet("Ramya")
```

**Output:**
```text
Hello Ramya
```

Here:
- `name` is the parameter.
- `"Ramya"` is the argument.

## 7. Function With Multiple Parameters

A function can accept multiple parameters.

Example:

```python
def add(a, b):
    print(a + b)

add(10, 20)
```

**Output:**
```text
30
```

Here:
- `a` receives 10.
- `b` receives 20.

## 8. Return Statement

The `return` statement sends a result back from a function.

Example:

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

### Important Difference Between print() and return

**Using print():**

```python
def add(a, b):
    print(a + b)

result = add(10, 20)

print(result)
```

Output:
```text
30
None
```

**Using return:**

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)
```

Output:
```text
30
```

**Remember:**

- `print()` displays information on the screen.
- `return` sends a value back to the caller.
- A function without an explicit return statement returns `None`.

## 9. Default Parameters

Default parameters have predefined values.

If an argument is not provided, Python uses the default value.

Example:

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

## 10. Keyword Arguments

We can pass arguments using parameter names.

Example:

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

The order of keyword arguments does not need to match the parameter order.

## 11. Positional Arguments

Values are assigned according to their position.

Example:

```python
def student(name, age):
    print(name)
    print(age)

student("Ramya", 20)
```

**Output:**
```text
Ramya
20
```

Here:
- First argument goes to `name`.
- Second argument goes to `age`.

## 12. Arbitrary Positional Arguments (*args)

Sometimes we do not know how many arguments will be passed.

We use `*args` to accept multiple positional arguments.

The arguments are collected into a tuple.

Example:

```python
def add(*numbers):
    print(sum(numbers))

add(10, 20, 30)
```

**Output:**
```text
60
```

Another example:

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

## 13. Arbitrary Keyword Arguments (**kwargs)

We use `**kwargs` to accept multiple keyword arguments.

They are collected into a dictionary.

Example:

```python
def student(**details):
    print(details)

student(name="Ramya", age=20, course="AI & DS")
```

**Output:**
```text
{'name': 'Ramya', 'age': 20, 'course': 'AI & DS'}
```

Accessing individual values:

```python
def student(**details):
    print(details["name"])
    print(details["age"])

student(name="Ramya", age=20)
```

**Output:**
```text
Ramya
20
```

## 14. Scope of Variables in Functions

Scope determines where a variable can be accessed.

There are two important types.

### Local Variable

A variable created inside a function is called a local variable.

It can normally be accessed only inside that function.

Example:

```python
def display():
    x = 10
    print(x)

display()
```

**Output:**
```text
10
```

### Global Variable

A variable created outside a function is called a global variable.

It can be accessed inside functions.

Example:

```python
x = 100

def display():
    print(x)

display()
```

**Output:**
```text
100
```

### Using the global Keyword

The `global` keyword allows us to modify a global variable inside a function.

Example:

```python
x = 10

def change():
    global x
    x = 20

change()

print(x)
```

**Output:**
```text
20
```

## 15. Passing a List to a Function

We can pass lists as arguments.

Example:

```python
def display(numbers):
    for n in numbers:
        print(n)

values = [10, 20, 30]

display(values)
```

**Output:**
```text
10
20
30
```

## 16. Returning Multiple Values

Python allows a function to return multiple values.

Example:

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

Python packs the returned values into a tuple.

## 17. Function Calling Another Function

One function can call another function.

Example:

```python
def square(n):
    return n * n

def display():
    result = square(5)
    print(result)

display()
```

**Output:**
```text
25
```

This helps divide complex programs into smaller tasks.

## 18. Lambda Functions

A lambda function is a small anonymous function created using the `lambda` keyword.

It can contain only one expression.

Syntax:

```python
lambda arguments: expression
```

Example:

```python
square = lambda n: n * n

print(square(5))
```

**Output:**
```text
25
```

Another example:

```python
add = lambda a, b: a + b

print(add(10, 20))
```

**Output:**
```text
30
```

For more details, refer to `Lambda_Functions.md`.

## 19. Common Mistakes

1. Forgetting the colon after the function definition.
2. Incorrect indentation inside the function.
3. Calling a function without required arguments.
4. Confusing parameters with arguments.
5. Using `print()` when a returned value is needed.
6. Forgetting to call the function.
7. Trying to access local variables outside their function.
8. Forgetting that a function without an explicit return statement returns `None`.
9. Using the wrong number of arguments.
10. Placing required parameters after default parameters in a function definition.

## 20. Real-World Applications

- Creating calculators.
- Processing student records.
- Performing mathematical calculations.
- Building machine learning applications.
- Reusing code in large projects.
- Processing datasets.
- Creating reusable application components.
- Developing APIs and software applications.

## 21. Important Interview Questions

**Q1. What is a function in Python?**

A function is a reusable block of code designed to perform a specific task.

**Q2. Which keyword is used to define a function?**

The `def` keyword.

**Q3. What is the difference between parameters and arguments?**

Parameters are variables defined in a function, whereas arguments are actual values passed when calling the function.

**Q4. What is the difference between print() and return?**

`print()` displays information, whereas `return` sends a value back from a function.

**Q5. What happens if a function does not have a return statement?**

It returns `None` by default.

**Q6. What are default arguments?**

Arguments that have predefined values in a function definition.

**Q7. What is *args?**

It allows a function to accept multiple positional arguments as a tuple.

**Q8. What is **kwargs?**

It allows a function to accept multiple keyword arguments as a dictionary.

**Q9. What is a local variable?**

A variable created inside a function that is normally accessible only within that function.

**Q10. What is a global variable?**

A variable defined outside functions that can be accessed throughout the module, subject to scope rules.

**Q11. Can a function return multiple values?**

Yes. Python can return multiple values, which are packed into a tuple.

**Q12. Can one function call another function?**

Yes. A function can call another function.

**Q13. What is a lambda function?**

A small anonymous function created using the `lambda` keyword.

**Q14. Can a function accept a list as an argument?**

Yes. Lists can be passed to functions like other Python objects.

**Q15. Why are functions important in programming?**

They improve code reusability, organization, readability and maintainability.

## 22. Practice Programs

1. Create a function to print a welcome message.
2. Create a function to add two numbers.
3. Create a function to find the largest of two numbers.
4. Create a function to check whether a number is even or odd.
5. Create a function to calculate factorial.
6. Create a function to check whether a number is prime.
7. Create a function to reverse a string.
8. Create a function to check whether a string is a palindrome.
9. Create a function to find the sum of elements in a list.
10. Create a function to find the largest element in a list.
11. Create a function to count vowels in a string.
12. Create a function to calculate the average of numbers.
13. Create a function that accepts multiple numbers using `*args`.
14. Create a function that accepts student details using `**kwargs`.
15. Create a function that returns both the maximum and minimum values in a list.

---

## Important for Placements

Functions are essential for writing clean and reusable code.

Before moving to DSA, make sure you understand:

- Function definition and calling.
- Parameters and arguments.
- Return statements.
- Local and global variables.
- Default arguments.
- `*args` and `**kwargs`.
- Passing lists to functions.

**Remember:** In coding interviews, you will frequently be asked to write solutions inside functions rather than writing all your logic directly in the main program.

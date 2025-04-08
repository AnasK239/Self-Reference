## Writing (Defining) a Function

In Python, a function is defined using the `def` keyword:

### Syntax:

```python
def function_name(parameters):
    """Optional docstring explaining the function."""
    # Function body
    return value  # Optional
```

### Example:

```python
def greet(name):
    """Greets the person by name."""
    print(f"Hello, {name}!")
```

- `function_name`: The name you give your function.
- `parameters`: Inputs (also called arguments) to the function.
- `return`: Returns a result (optional).

---

### Functions with Return Values:

```python
def add(a, b):
    return a + b

result = add(3, 5)
print(result)  # Output: 8
```

```python

    def h (y):
    x+=1
    print(x)

h(1)
```
> Error X is Referenced before assignment
---

## Types of Function Arguments

Python functions support different kinds of arguments:

1. **Positional Arguments**
2. **Keyword Arguments**
3. **Default Arguments**
4. **Variable-Length Arguments** (`*args`, `**kwargs`)

---
### Example:

```python
def describe_pet(animal_type, pet_name="Unknown", *traits, **details):
    print(f"\nI have a {animal_type} named {pet_name}.")
    for trait in traits:
        print(f"- Trait: {trait}")
    for key, value in details.items():
        print(f"- {key.title()}: {value}")

describe_pet("dog", "Buddy", "loyal", "furry", age=5, color="brown")
```

---

### Naming Conventions

- Use **snake_case** for function names: `calculate_total`
- Name functions clearly and descriptively: `get_user_input()`

---
### Avoid Side Effects

Prefer **pure functions** (same output for same input, no external changes) when possible.

---
### Type Hints (Python 3.5+)

Helps readability and debugging:

```python
def multiply(a: int, b: int) -> int:
    return a * b
```

---
### Handling Errors

```python
def divide(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return "Cannot divide by zero."
```

---

##  Lambda (Anonymous) Functions

For short, simple functions:

```python
square = lambda x: x ** 2
print(square(4))  # Output: 16
```

Used often with `map()`, `filter()`, `sorted()`.

---

## First-Class Functions

In Python, functions are first-class citizens. You can:

- Assign them to variables
- Pass them as arguments
- Return them from other functions

```python
def shout(text):
    return text.upper()

def greet(func):
    return func("hello")

print(greet(shout))  # Output: HELLO
```

---

## Using `*args` and `**kwargs`

- `*args` lets you pass a variable number of **positional arguments**.
- `**kwargs` lets you pass a variable number of **keyword arguments**.

```python
def show_args(*args, **kwargs):
    print(args)
    print(kwargs)

show_args(1, 2, 3, name="Alice", age=30)
```

---

## Decorators 

Decorators are functions that modify the behavior of other functions.

```python
def decorator(func):
    def wrapper():
        print("Before the function call.")
        func()
        print("After the function call.")
    return wrapper

@decorator
def say_hello():
    print("Hello!")

say_hello()
```

---

## Summary

| Concept                 | Example                         |
|------------------------|---------------------------------|
| Define Function         | `def my_func():`               |
| Call Function           | `my_func()`                    |
| Return Value            | `return value`                 |
| Positional Argument     | `my_func(1, 2)`                |
| Keyword Argument        | `my_func(x=1, y=2)`            |
| Default Value           | `def my_func(x=10):`           |
| Variable-Length Args    | `*args`, `**kwargs`            |
| Lambda Function         | `lambda x: x + 1`              |
| Type Hinting            | `def f(x: int) -> int:`        |

---

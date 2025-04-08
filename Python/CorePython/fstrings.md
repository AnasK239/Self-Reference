> F-strings (formatted string literals) are a feature introduced in Python 3.6 

 Makes string interpolation easier and more readable. F-strings are prefixed with the letter `f` or `F` and allow expressions to be embedded directly within string literals using curly braces `{}`.

---

## Basic Syntax
```python
name = "Alice"
age = 30
message = f"My name is {name} and I am {age} years old."
print(message)
# Output: My name is Alice and I am 30 years old.
```

---

## Expressions Inside F-strings

You can include any valid Python expression inside `{}`.

```python
a = 5
b = 10
print(f"The sum of {a} and {b} is {a + b}.")
# Output: The sum of 5 and 10 is 15.

print(f"Uppercase: {'hello'.upper()}")
# Output: Uppercase: HELLO
```

---

## Number Formatting

### 1. Fixed decimal places

```python
pi = 3.14159
print(f"Pi rounded to 2 decimals: {pi:.2f}")
# Output: Pi rounded to 2 decimals: 3.14
```

### 2. Padding numbers

```python
for i in range(1, 4):
    print(f"{i:02}")  # Pad with zeros to 2 digits
# Output:
# 01
# 02
# 03
```

### 3. Thousands separator

```python
num = 1000000
print(f"{num:,}")
# Output: 1,000,000
```

---

## Date Formatting
F-strings can use format specifiers for datetime objects.

```python
from datetime import datetime
now = datetime.now()
print(f"Current time: {now:%Y-%m-%d %H:%M}")
# Output: Current time: 2025-04-08 14:35 (example)
```

---

## Using Functions Inside F-strings

```python
def greet(name):
    return f"Hello, {name}!"

print(f"{greet('Bob')}")
# Output: Hello, Bob!
```

---

## Multi-line F-strings

You can use triple quotes with f-strings for multi-line formatting:

```python
name = "Luna"
score = 95
report = f"""
Student: {name}
Score: {score}
Result: {"Pass" if score >= 50 else "Fail"}
"""
print(report)
```

---

## Using `=` for Debugging (Python 3.8+)

This prints the expression along with its value.

```python
x = 10
print(f"{x=}")
# Output: x=10

print(f"{x * 2=}")
# Output: x * 2=20
```

---

## Nested F-strings (String in string)

You can use nested f-strings by evaluating them ahead of time:

```python
name = "Sky"
msg = f"Welcome, {f'{name.upper()}'}!"
print(msg)
# Output: Welcome, SKY!
```

---

## F-strings are evaluated at runtime

Because f-strings evaluate expressions **at runtime**, they can be dynamic and context-sensitive.

```python
import math
angle = 90
print(f"Sine of {angle} degrees is {math.sin(math.radians(angle)):.2f}")
# Output: Sine of 90 degrees is 1.00
```

---

## Summary 

| Feature                  | Example                               | Output                                |
|--------------------------|---------------------------------------|----------------------------------------|
| Variable substitution    | `f"Name: {name}"`                     | `Name: Alice`                          |
| Expressions              | `f"{a + b}"`                          | `15`                                   |
| Format float             | `f"{pi:.2f}"`                         | `3.14`                                 |
| Thousands separator      | `f"{1000000:,}"`                      | `1,000,000`                            |
| Date formatting          | `f"{now:%Y-%m-%d}"`                   | `2025-04-08`                           |
| Debugging with `=`       | `f"{x=}"`                             | `x=10`                                 |

---
# Abstraction in Object-Oriented Programming

## Key Concepts
- A **class** has **Attributes**, **Methods**, and **Constructors**.
- **Abstraction** hides implementation details, meaning you don’t need to worry about what happens under the hood.

---

## Abstract Classes
```java
public abstract class <ClassName> {
    // Abstract class definition
}
```

- You **cannot** create an object of an abstract class; it serves as a blueprint for other classes.
- Other classes **inherit** the abstract class’s properties (e.g., a gas pedal is connected to the engine in some way).

---

## Abstract vs. Concrete Methods
### Abstract Methods
- Must be implemented by child classes.
- Example: A `Shape` abstract class **must** contain an `area` method.

```java
abstract class Shape {
    abstract double area();
}
```

- Each subclass of `Shape` should have its **own definition** of `area()` by **overriding** the parent method.
- Example subclasses:

```java
class Triangle extends Shape {
    @Override
    double area() {
        // Implementation for Triangle
    }
}

class Rectangle extends Shape {
    @Override
    double area() {
        // Implementation for Rectangle
    }
}
```

### Concrete Methods
- Unlike abstract methods, **they can be implemented or not**.
- They are **inherited by all child classes** **without overriding**.

```java
abstract class Vehicle {
    void start() {
        System.out.println("Vehicle is starting");
    }
}
```

In this case, `start()` is a concrete method that **all child classes inherit** as-is.

---

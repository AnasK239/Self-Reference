# Interfaces

* Using interfaces allows a class to have multiple parents and inherit their attributes,  
unlike normal inheritance where a class can only have one parent.

* Think of it like this : the class implements a blue-print defined by the interface.

---
## Defining an Interface

If a class inherits from an interface, it **must** implement all methods defined in the interface.

**Example:**  
```java
public class MyClass implements MyInterface {
    @Override
    public void myMethod() {
        // Implement method
    }
}
```
---
## Multiple Interfaces

A class can implement multiple interfaces:

* Think of it like this : Some animals considered preyand predators at the same time so they implement both blue prints.

```java
public class Animal implements Predator, Prey {
    @Override
    public void hunt() {
        // Implementation
    }

    @Override
    public void flee() {
        // Implementation
    }
}
```

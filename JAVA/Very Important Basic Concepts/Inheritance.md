# Inheritance

After making a new class, if you want another class to inherit its attributes:

## Example:  
```java
class Animals { }
class Cat extends Animals { }
```

## Syntax when forming the new class

```java
public class <ChildClass> extends <ParentClass> {
    // Class body
}
```

The Parent Class can be referred to as `super`, and the child class inherits attributes from the `super` class.

---

### Constructor Inheritance

If the super constructor requires two arguments, e.g., `Parent(a1, a2)`,  
and the child constructor requires three arguments, e.g., `Child(a1, a2, a3)`,  
then you must provide the first two arguments to the Parent first.

**Syntax:**  
```java
super(a1, a2);
this.a3 = a3;
```
**Example**
```java
consider Animal class as a super
Animal(a1,a2){
    // super class construction
}

cat(a1,a2,a3){
    super(a1, a2); // Animal is the super of cat so we have to pass the super argumentsat child construction.
    this.a3 = a3;
}
```

**Note:** `a1` and `a2` are still accessible to any methods in the child class using `this.<aX>`.

---
## Method Overriding

Method overriding is defining the same method inherited by the child inside the child itself with different parameters.

**Example:**  
```java
class Parent {
    void show() {
        System.out.println("Parent method");
    }
}

class Child extends Parent {
    @Override
    void show() {
        System.out.println("Child method");
    }
}
```

The overridden method is used when calling `child.method()`.

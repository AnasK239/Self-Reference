# Anonymous Classes

An **anonymous class** is a class that doesn't have a name and **cannot be reused**.

## Why Use Anonymous Classes?

- Allows adding **custom behavior** without creating a new named class.
- Often used for **one-time** use cases, such as:
  - `TimerTask`
  - `Runnable`
  - `Callbacks`
- Useful when you need to create an object of a certain class with **slightly different methods**.

Instead of defining a new class for **just one object**, you can use an **anonymous class**.

---
## Example

Suppose that we have created a `Dog` class. Normally, when a `Dog` speaks, it says `"woof"`.
However, we want to create a `Dog` object named **Scooby-Doo**, which speaks English.

### Normal Class Object:
```java
Dog dog1 = new Dog(); // This is a normal dog
dog1.speak(); // Output: woof
```

### Anonymous Class Object:
```java
Dog scoobyDoo = new Dog() {	
    @Override
    void speak() {
        System.out.println("english mumble");
    }
}; 

// This is Scooby-Doo
scoobyDoo.speak(); // Output: english mumble
```

In this example, instead of creating a separate subclass of `Dog`, we use an **anonymous class** to override the `speak` method for just this one instance. So now **scoobyDoo** is an object of an anonymous class that isnt defined.

---

This makes anonymous classes a **powerful tool** when slight modifications are needed for a **specific object**, without adding unnecessary complexity.


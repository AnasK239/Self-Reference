# Static Keyword

---
## Tracking Class Instances

To track the number of times a class is instantiated, use a `static` variable.

```java
public class Example {
    static int track = 0;

    public Example() {
        track++;
    }
}
```

### Why `static`?
- A static variable is **shared** by all instances of the class.
- Access it via the **class name**, not individual objects.

#### Example:
```java
Example obj1 = new Example();
Example obj2 = new Example();

System.out.println(Example.track); // Output: 2
```

## `static` Keyword
- **Owned by the class**, not instances.
- **Shared** among all objects of the class.

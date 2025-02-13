# toString Method

By default, `toString()` returns a hash code. To make it useful, **override it**.

---
## Default Behavior

```java
public String toString() {
    return getClass().getName() + "@" + Integer.toHexString(hashCode());
}
```
---
## Overriding `toString()`

```java
@Override
public String toString() {
    return "This is a useful string representation of an object.";
}
```

Now, when calling `System.out.println(object)`, the overridden `toString()` will be used instead of a hash.

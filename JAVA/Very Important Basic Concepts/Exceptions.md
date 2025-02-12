# Exceptions

**Exception** = An event that interrupts the normal flow of a program  
*(Examples: dividing by zero, file not found, mismatch input type)*

Surround any dangerous code with a `try {}` block:  
`try {}`, `catch {}`, `finally {}`

## Note:

When catching exceptions, if you want a safety net to handle any unknown exception, use:

```java
catch(Exception e) {
    System.out.println("Something went wrong");
}
```

---

## Method 1: Standard Try-Catch-Finally

```java
try {
    // Block of code
} 
catch (ExceptionType e) {
    // Handle exception
} 
finally {
    // Close any open resources (e.g., Scanner)
}
```

---

## Method 2: Try-With-Resources

```java
try (Scanner scanner = new Scanner(System.in)) {
    // Block of code
} 
catch (ExceptionType e) {
    // Handle exception
} 
finally {
    // Resources are automatically closed, no manual cleanup needed
}
```
---
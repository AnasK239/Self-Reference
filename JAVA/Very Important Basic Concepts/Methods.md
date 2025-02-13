# Methods and Arrays

## Variable Scope in `main`
Placing a variable (like a Scanner) after `public class Main` makes it accessible to any method below.

---
## Arrays

### Declaring an Array
```java
String[] fruit = {"Apple", "Banana", "Cherry"};
```

### Getting Array Length
```java
int length = fruit.length;
```

### For-Each Loop
```java
for (String c : fruit) {
    System.out.println(c);
}
```

### Sorting an Array
```java
Arrays.sort(fruit);
```

### Filling an Array
```java
Arrays.fill(fruit, "Mango"); // All elements set to "Mango"
```

# Generics

Generics allow you to write a class, interface, or method that is compatible with different data types.

- `<T>` is a type parameter (placeholder that gets replaced with a real type).
- `<String>`, `<Integer>`, etc., are type arguments that specify the type.

---

## Example 1: Generic Class

```java
public class Box<T> {
    private T item;

    public void setItem(T item) {
        this.item = item;
    }

    public T getItem() {
        return this.item;
    }
}

// Usage in main:
Box<String> box = new Box<>();
box.setItem("Banana");
System.out.println(box.getItem());
```
---

## Example 2: Multiple Type Parameters

```java
public class Product<T, U> {
    private T item;
    private U price;

    public Product(T item, U price) {
        this.item = item;
        this.price = price;
    }

    public U getPrice() {
        return this.price;
    }
}

// Usage in main:
Product<String, Double> product1 = new Product<>("Apple", 0.50);
Product<String, Integer> product2 = new Product<>("Ticket", 15);
System.out.println(product2.getPrice());
```

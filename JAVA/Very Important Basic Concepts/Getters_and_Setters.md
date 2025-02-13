# Getters and Setters

Getters and Setters help control access to private attributes, preventing accidental modification.

- **Getters** make an attribute **readable**.
- **Setters** make an attribute **writable**.

---
## Example: Car Class

```java
public class Car {
    private String model;
    private String color;
    private int price;

    public Car(String model, String color, int price) {
        this.model = model;
        this.color = color;
        this.price = price;
    }

    // Getters
    public String getModel() {
        return this.model;
    }

    public String getColor() {
        return this.color;
    }

    public int getPrice() {
        return this.price;
    }

    // Setter for color
    public void setColor(String color) {
        this.color = color;
    }
}

// Usage in main:
Car car = new Car("Corvette", "Yellow", 20000);
System.out.println(car.getColor() + " " + car.getModel() + " " + car.getPrice());
car.setColor("Blue"); // Change color
```

This prevents direct modification of attributes while allowing controlled updates.

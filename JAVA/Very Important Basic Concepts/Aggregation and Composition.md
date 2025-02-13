# Java Object Relationships: Aggregation & Composition

## Aggregation

Aggregation in Java represents a "has-a" relationship between objects, where one object (the whole) contains another object (the part). 

### Key Characteristics:
* The part object can exist independently of the whole object.
* The lifecycle of the part is not controlled by the whole—if the whole is destroyed, the part can continue to exist.
* So aggregation Represents a "has-a" Relationship between objects where
One object contains another object as part of its structure.

**Example:**  
A Library has Books, but Books can exist without a Library.

---
## Composition

Composition is a fundamental object-oriented programming (OOP) concept that establishes a "whole-part" relationship between classes.

### Key Characteristics:
* Enforces a strong dependency between objects
* The lifecycle of the "part" (child object) is tightly controlled by the "whole" (parent object)
* If the parent is destroyed, all child objects are also destroyed
* Models a strict "has-a" relationship
* Used to design modular, reusable, and maintainable systems

### Implementation Example
- Just a heads up, when looking at any code snippet try to skip the Main and get a sense for defined classes first
```java
public class Main {
    public static void main(String[] args) {
        Car car = new Car("Mustang", 2024, "v10");
        
        // Note: engine.type is used to access the string value
        // because engine is a constructed object from Engine class
        System.out.println(car.model + " " + car.year + " " + car.engine.type);
    }
}

public class Car {
    String model;
    int year;
    Engine engine;

    Car(String model, int year, String engineType) {
        this.model = model;
        this.year = year;
        // engine variable holds reference to Engine object
        this.engine = new Engine(engineType);
    }
}

public class Engine {
    String type;

    Engine(String type) {
        this.type = type;
    }
}
```

### Important Note
When accessing the engine type in the example above, we use `engine.type` because `engine` is a reference to an Engine object, not the string value itself. To access the actual string value of the engine type, we need to use the `.type` property.

---

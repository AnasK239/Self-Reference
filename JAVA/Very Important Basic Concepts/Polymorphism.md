# Polymorphism

Polymorphism allows objects of different classes to be treated as objects of a common superclass.

---
## Example: Vehicle Types

Assume an abstract class `Vehicle`, with three subclasses that extend it: `Car`, `Boat`, and `Bike`.
Now if we want to group up the 3 types in an array what should the type be ? well it should be something that all the classes have in common.

```java
Vehicle[] vehicles = {new Car(), new Bike(), new Boat()};
```

Since all these classes inherit from `Vehicle`, they can be stored in an array of `Vehicle` type.

Any Car object identifies as Car but also identifies as a vehicle  same goes for others.

* This can be achieved by an abstract class or an interface whichever you prefer.

---
## Runtime Polymorphism

The method executed is determined at **runtime** based on user input.

### Example: Animal Shelter
Assume an abstract class Animal  which has two children either a dog or a cat , suppose this is an animal rescue shelter.

The user will have to choose wether they take a cat or a dog home.

If the cat is picked it says MEOW  ,, if the dog is picked it says woof. 

so we will need to morph the object to the user's liking.

```java
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Animal animal;

        System.out.println("Would you like a cat or a dog? (1. Dog, 2. Cat)");
        int choice = scanner.nextInt();

        if (choice == 1) {
            animal = new Dog();
        } else {
            animal = new Cat();
        }

        animal.speak();
        scanner.close();
    }
}
```

Here, `animal.speak()` calls the appropriate method based on the user's choice, `.speak()` is an animal defined method.

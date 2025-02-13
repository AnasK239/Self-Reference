# User Input

Java provides the `Scanner` class for reading user input.

## Import and Setup

```java
import java.util.Scanner;

Scanner scanner = new Scanner(System.in);
```

---
## Reading Different Types of Input
A problem arises when accepting strings after integers because when you hit enter it picks up on the ` \n ` and thinks its the input, to clear the input buffer do as follows:
```java
System.out.print("Enter your name: ");
String name = scanner.nextLine(); // Reads full line (including spaces)

System.out.print("Enter your age: ");
int age = scanner.nextInt(); // Reads integer

scanner.nextLine(); // Clear input buffer (needed after nextInt())

System.out.print("Enter your favorite color: ");
String color = scanner.nextLine();

scanner.close(); // Always close the scanner when done
```
---
## Handling Different Input Types

- `scanner.nextLine()` → Reads a full string with spaces.
- `scanner.next()` → Reads a single word (stops at space).
- `scanner.nextInt()` → Reads an integer.
- `scanner.nextDouble()` → Reads a decimal number.

---
## Important notes
Types of variables :

1- `primitive` = a normal variable which takes a set value.

2- `Reference` = memory address (stack) points to (heap).

`Concatenation` is acceptable in sout     (you can do it with variables or strings whatever) 
**Syntax**:

			sout("Hi" + X) (X is a variable or string)
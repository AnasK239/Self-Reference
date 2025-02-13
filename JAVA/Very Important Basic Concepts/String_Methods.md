# String Methods

Java provides several useful string methods.

## Common Methods

```java
string.length();         // Returns the length of the string (including spaces)
string.charAt(x);        // Returns character at index x
string.indexOf("x");     // Returns first index of "x"
string.lastIndexOf("x"); // Returns last index of "x"
string.toUpperCase();    // Converts to uppercase
string.toLowerCase();    // Converts to lowercase
string.trim();           // Removes leading/trailing spaces
string.replace("x","y"); // Replaces all occurrences of "x" with "y"
string.isEmpty();        // Returns true if string is empty
string.contains("x");    // Returns true if "x" is found in the string
string.equals("x");      // Case-sensitive comparison
string.equalsIgnoreCase("x"); // Case-insensitive comparison
string.substring(start, end); // Extracts substring (end index is exclusive)
```
---
## Enhanced Switch

```java
switch (case) {
    case x -> doSomething();
    case y, z -> doAnotherThing();
    case w -> {
        if (condition) {
            System.out.println("Action performed");
        }
    }
    default -> doDefaultAction();
}
```
---
## Thread Sleeping

```java
Thread.sleep(1000); // Pauses execution for 1000ms (1 second)
```

Make sure to add `throws InterruptedException` in the method signature when using `Thread.sleep()`.

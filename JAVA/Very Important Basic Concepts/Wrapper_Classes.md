# Wrapper Classes
Wrapper classes **convert primitive types into objects**.

`Wrapper classes` = Allow **primitive** values (int, char, double, boolean) to be used as objects. `"Wrap them in an object"`. Generally, don't wrap primitives unless you need an object.

Allows use of Collections Framework and static Utility Methods.

---
## AutoBoxing (Primitive → Object)
```java
Integer a = 123; // Be careful, this is not a primitive type (int). This is an object from the class Integer.
```
---
## Unboxing (Unwrapping the object)
```java
int b = a; // b is now a primitive type int with the value assigned to a, which is 123.
```

### Disclaimer:
If you try to return or use an object, you will get a reference value instead of the desired output.

### Note:
There is an object class and a primitive type for everything except String, which only has an object.

---
## What You Can Do with Wrapper Classes and Why It's Useful

### Convert an Integer to a String
```java
String a = Integer.toString(123); // Wraps the transformed-to-string Integer object in a String object.
```
This allows you to wrap multiple objects as strings (a, b, c, d) and concatenate them together:
```java
String x = a + b + c; // Even though they are of different types (Boolean, int, double, etc.), they can be combined.
```
---
### Convert a String to an Integer, Boolean, or Other Type Using Parsing
```java
int a = Integer.parseInt("123"); // a is now a primitive type integer (a normal number ready to be used).
char c = "Pizza".charAt(0); // Retrieves the first character ('P').
```
---
### Using Object Functions to Determine Validity
```java
char c = 'b';
boolean isLetter = Character.isLetter(c); // Returns a boolean indicating if it's actually a letter.
```

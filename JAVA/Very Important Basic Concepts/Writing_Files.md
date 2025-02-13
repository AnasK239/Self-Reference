# Writing Files

You have 4 options for writing files:

1. **FileWriter**: Good for small or medium-sized text files.
2. **BufferedReader**: Better performance for large amounts of text.
3. **PrintWriter**: Best for structured data, like reports or logs.
4. **FileOutputStream**: Best for binary files (e.g., images, audio files).

---
## Handling Exceptions When Writing Files

Writing files is inherently risky, so exceptions need to be handled properly:

```java
try (FileWriter writer = new FileWriter("Location\\test.txt");) { 
    // **Note:** When adding a location, use \\ instead of \.
    // You can also replace what's inside FileWriter() with a String object.

    writer.write("I like onion rings");

} catch (IOException e) {
    System.out.println("Couldn't write file");
}
```
This will create a `.txt` file containing your message.

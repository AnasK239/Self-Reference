# Reading Files in Java

There are three common ways to read files:

1. **BufferedReader + FileReader** (Best for text files)
2. **FileInputStream** (Best for binary files like images, audio)
3. **RandomAccessFile** (Best for reading/writing specific portions of large files)

---
## Example: Reading a Text File

```java
String filePath = "example.txt";

try (BufferedReader reader = new BufferedReader(new FileReader(filePath))) {
    String line;
    while ((line = reader.readLine()) != null) {
        System.out.println(line);
    }
} catch (FileNotFoundException e) {
    System.out.println("Could not locate file");
} catch (IOException e) {
    System.out.println("Something went wrong");
}
```

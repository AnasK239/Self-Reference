

## **1. Attributes (Fields)**
| **Modifier** | **Field Name**  | **Type** | **Description** |
|-------------|---------------|---------|---------------|
| **`- value`** | `value` | `int` | Stores the integer value of the object (private). |
| **`+ MAX_VALUE`** | `MAX_VALUE` | `int` | The maximum value an `int` can hold (`2^31 - 1`). |
| **`+ MIN_VALUE`** | `MIN_VALUE` | `int` | The minimum value an `int` can hold (`-2^31`). |

### **Explanation:**
- The `value` field is **private (`-`)**, meaning it cannot be accessed directly from outside the class.
- `MAX_VALUE` and `MIN_VALUE` are **public (`+`) constants**, meaning they can be accessed directly using `Integer.MAX_VALUE` and `Integer.MIN_VALUE`.

---

## **2. Constructors**
| **Method Signature** | **Description** |
|----------------------|----------------|
| **`+ Integer(value: int)`** | Constructs an `Integer` object with the specified `int` value. |
| **`+ Integer(s: String)`** | Constructs an `Integer` object by parsing the provided `String`. |

### **Explanation:**
- `Integer(int value)`: Creates an `Integer` object from an **int**.
- `Integer(String s)`: Creates an `Integer` object by converting a **string** representation of an integer into an `int`.

---

## **3. Methods**
| **Method Signature** | **Return Type** | **Description** |
|----------------------|---------------|----------------|
| **`+ byteValue()`** | `byte` | Returns the integer value as a `byte`. |
| **`+ shortValue()`** | `short` | Returns the integer value as a `short`. |
| **`+ intValue()`** | `int` | Returns the integer value. |
| **`+ longValue()`** | `long` | Returns the integer value as a `long`. |
| **`+ floatValue()`** | `float` | Returns the integer value as a `float`. |
| **`+ doubleValue()`** | `double` | Returns the integer value as a `double`. |
| **`+ compareTo(o: Integer)`** | `int` | Compares this `Integer` object with another `Integer` object. |
| **`+ toString()`** | `String` | Returns the `String` representation of the integer value. |
| **`+ valueOf(s: String): Integer`** | `Integer` | Converts a `String` to an `Integer` object. |
| **`+ valueOf(s: String, radix: int): Integer`** | `Integer` | Converts a `String` to an `Integer` object using a specified base (`radix`). |
| **`+ parseInt(s: String): int`** | `int` | Parses a `String` and returns an `int` value. |
| **`+ parseInt(s: String, radix: int): int`** | `int` | Parses a `String` using a specific `radix` and returns an `int`. |

---

## **4. Explanation of Important Methods**
### **Conversion Methods**
- `byteValue()`, `shortValue()`, `intValue()`, `longValue()`, `floatValue()`, and `doubleValue()`: Convert the `Integer` object into different primitive data types.

### **Comparison Method**
- `compareTo(Integer o)`: Compares two `Integer` objects numerically. Returns:
  - `0` if both are equal,
  - A negative value if this object is smaller,
  - A positive value if this object is larger.

### **String Conversion Methods**
- `toString()`: Converts the integer to a `String`.
- `valueOf(String s)`: Converts a `String` into an `Integer` object.
- `valueOf(String s, int radix)`: Converts a `String` into an `Integer` object based on the specified **radix** (number system, e.g., binary = 2, decimal = 10, hexadecimal = 16).

### **Parsing Methods**
- `parseInt(String s)`: Parses a `String` and returns an **int**.
- `parseInt(String s, int radix)`: Parses a `String` in a **specific base** and returns an **int**.

---

## **Example Usage in Java**
### **1. Creating Integer Objects**
```java
Integer num1 = new Integer(100);  // Using int constructor (Deprecated)
Integer num2 = Integer.valueOf("200");  // Using valueOf() method
Integer num3 = Integer.valueOf("FF", 16);  // Parses "FF" as hexadecimal (255)
```

### **2. Converting Integer to Other Types**
```java
int intValue = num1.intValue();   // 100
double doubleValue = num1.doubleValue();  // 100.0
String strValue = num1.toString();  // "100"
```

### **3. Parsing Strings**
```java
int num4 = Integer.parseInt("123");  // 123
int num5 = Integer.parseInt("1010", 2);  // Binary to decimal (10)
```

### **4. Comparing Integer Objects**
```java
Integer a = 50;
Integer b = 100;
System.out.println(a.compareTo(b));  // Output: -1 (a is smaller)
System.out.println(b.compareTo(a));  // Output: 1 (b is larger)
System.out.println(a.compareTo(50)); // Output: 0 (equal)
```

---

## **Summary of `java.lang.Integer` Class**
| Feature | Description |
|---------|------------|
| **Type** | Wrapper class for `int` |
| **Key Fields** | `value`, `MAX_VALUE`, `MIN_VALUE` |
| **Key Constructors** | `Integer(int)`, `Integer(String)` |
| **Key Methods** | `byteValue()`, `intValue()`, `toString()`, `parseInt()`, `valueOf()`, `compareTo()` |
| **Usage** | Converting, parsing, comparing integers |

---



### **Composition, Aggregation, and Association in Object-Oriented Design**

In Object-Oriented Programming (OOP), relationships between objects are important for designing efficient and logical systems. Three key relationships are **Association, Aggregation, and Composition**.

---

### **1. Association**
- **Definition**: Association is a general relationship between two classes where one class is related to another.
- **Nature**: It represents a "uses-a" or "knows-a" relationship.
- **Example**: A teacher **teaches** students. Both Teacher and Student exist independently.
- **Types**:
  - **One-to-One (1:1)** – Each object in class A is related to one object in class B.
  - **One-to-Many (1:N)** – One object in class A is related to multiple objects in class B.
  - **Many-to-Many (M:N)** – Many objects in class A are related to many objects in class B.

---

### **2. Aggregation (Has-A Relationship)**
- **Definition**: Aggregation is a special form of association where one class owns another, but both can exist independently.
- **Nature**: It represents a **weak "has-a"** relationship (partial ownership).
- **Example**: A **Student** has **one or more Addresses**, but an **Address** can exist without the Student.
- **Key Feature**: Objects have an independent lifecycle. Deleting the owner object **does not** delete the owned object.

🔹 **Example** (From Slides):
- The **Student** class aggregates the **Address** class with a **1..3** multiplicity (a student can have multiple addresses).
- The relationship is denoted by a **hollow diamond**.

---

### **3. Composition (Strong Has-A Relationship)**
- **Definition**: Composition is a **stronger form of Aggregation** where the child object **cannot exist without** the parent.
- **Nature**: It represents a **strong "has-a"** relationship (strong ownership).
- **Example**: A **Student** has a **Name**, but a **Name** does not exist without a Student.
- **Key Feature**: If the parent is destroyed, the child is also destroyed.

🔹 **Example** (From Slides):
- The **Student** class **composes** the **Name** class.
- The relationship is denoted by a **filled diamond**.

---

### **Summary of Differences**
| Feature | Association | Aggregation | Composition |
|---------|------------|-------------|-------------|
| **Definition** | General relationship | Weak ownership | Strong ownership |
| **Symbol in UML** | Simple line | Hollow diamond | Filled diamond |
| **Dependency** | No dependency | Child can exist independently | Child cannot exist independently |
| **Example** | Teacher teaches Student | Student has Address | Student has Name |

---
## Classes Represented in Java

```java
Aggregated Class (Name)

public class Name {
    ...
}
```
```java
Aggregated Class (Address)
java
Copy
Edit
public class Address {
    ...
}
```

The aggregated classes are usually represented as data fields in aggregating class.
```java
Aggregating Class (Student)

public class Student {
    private Name name;
    private Address address;
    ...
}
```
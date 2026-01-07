
---

## Wrapper Classes

### 1. What are Wrapper Classes?

* **Wrapper classes** are Java classes that **wrap primitive data types into objects**.
* They allow primitives to be used where **objects are required** (e.g., Collections, Generics, APIs).
* Wrapper classes are mainly present in:

  * `java.lang` package (most common)
  * `java.util` package (utilities using wrappers)

Examples:

* `Integer`, `Long`, `Boolean`, `Character`, etc.

---

### 2. Primitive → Object Conversion (Boxing)

#### (a) Using `valueOf()` method (Recommended)

* Static method of wrapper classes
* Converts primitive to wrapper object

```java
int i = 10;
Integer iObject = Integer.valueOf(i); // converting int to Integer
```

---

#### (b) Using `parseInt()` method

* Takes **String input**
* Returns primitive `int` (or can be auto-boxed to Integer)

```java
String str = "20";
int num = Integer.parseInt(str);      // returns int
Integer numObj = Integer.parseInt(str); // auto-boxing to Integer
```

---

#### (c) Using Constructor (Deprecated approach)

* Every wrapper class had constructors earlier
* **Not recommended** (deprecated since Java 9)

```java
int i = 10;
Integer iObject = new Integer(i); // using constructor
```

---

#### (d) Using `newInstance()` (Reflection-based, rarely used)

* Creates a new instance dynamically
* Not commonly used for wrapper classes directly

```java
Integer obj = Integer.class.newInstance(); // throws exception, not practical
```

---

### 3. Primitive Data Types and Wrapper Classes

| Primitive Data Type | Wrapper Class |
| ------------------- | ------------- |
| byte                | Byte          |
| short               | Short         |
| int                 | Integer       |
| long                | Long          |
| float               | Float         |
| double              | Double        |
| boolean             | Boolean       |
| char                | Character     |

---

### 4. Wrapper Class Utility Methods

Wrapper classes provide methods to **convert wrapper objects back to primitive types** (Unboxing).

| Method          | Description                |
| --------------- | -------------------------- |
| `byteValue()`   | Converts Integer to byte   |
| `shortValue()`  | Converts Integer to short  |
| `intValue()`    | Converts Integer to int    |
| `longValue()`   | Converts Integer to long   |
| `floatValue()`  | Converts Integer to float  |
| `doubleValue()` | Converts Integer to double |

#### Example:

```java
Integer num = Integer.valueOf(50);

int i = num.intValue();
double d = num.doubleValue();
```

📌 **Note:**

* These methods exist for **all numeric wrapper classes**
* `Character` does not have numeric conversion methods

---

### 5. Object → Primitive Conversion (Unboxing)

```java
Integer obj = Integer.valueOf(100);
int value = obj; // auto-unboxing
```

---

### 6. Why Wrapper Classes Are Important?

* Required for **Collections Framework**
* Used in **Generics**
* Helps in **type conversion**
* Provides **utility methods**
* Supports **autoboxing & unboxing**

---

### 7. Real-World Example (Collections API)

`Collections.max()` expects **primitive values or comparable objects**

```java
import java.util.*;

public class WrapperExample {
    public static void main(String[] args) {
        Integer a = 10;
        Integer b = 20;

        int maxValue = Collections.max(Arrays.asList(a, b));
        System.out.println(maxValue);
    }
}
```

✔ Wrapper objects are automatically **unboxed** when required.

---

### 8. Autoboxing & Unboxing (Java Feature)

```java
// Autoboxing
int x = 5;
Integer obj = x;

// Unboxing
Integer y = 10;
int z = y;
```

---

### 9. Key Exam Points ⭐

* Wrapper classes convert **primitive ↔ object**
* `valueOf()` is preferred over constructors
* Constructors are **deprecated**
* Needed for **Collections & Generics**
* Supports **autoboxing/unboxing**
* All wrapper classes except `Character` provide numeric conversion methods

---

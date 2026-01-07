
---

## `var` Keyword in Java

### Definition

* The **`var` keyword** is used to declare variables in Java.
* It allows the **compiler to infer the variable’s data type** from the initializer expression.
* Introduced in **Java 10**.

---

### Purpose of Variables

* Variables are used to **store data** in Java programs.
* They can be:

  * **Local variables** → declared inside methods or blocks
  * **Fields (instance/static variables)** → declared inside a class, outside methods

⚠️ **Important:**
`var` **can only be used for local variables**, **not for fields** or method parameters.

---

### Using `var` with Local Variables

#### Traditional Declaration

```java
int x = 10;
```

#### Using `var`

```java
var x = 10;   // Compiler infers type as int
```

✔️ Both statements are equivalent.

---

### Type Inference

* The **type is determined at compile time**
* Once inferred, the type **cannot change**

```java
var name = "Anubhav";  // inferred as String
var price = 99.99;    // inferred as double
```

---

### Using `var` with Arrays

```java
var myArray = new int[10];  // inferred type: int[]
```

---

### Rules & Limitations of `var`

#### 1. Must Have an Initializer

```java
var a;        // ❌ Compile-time error
```

```java
var a = 5;    // ✅ Valid
```

---

#### 2. Only Allowed for Local Variables

```java
class Test {
    var x = 10;   // ❌ Not allowed (field)
}
```

---

#### 3. Must Be on the Left-Hand Side

```java
var x = 10;     // ✅ Valid
```

```java
int y = var;    // ❌ Does not compile
```

---

#### 4. Cannot Be Initialized with `null`

```java
var value = null;  // ❌ Compiler cannot infer type
```

---

### Key Points to Remember (Quick Revision)

* `var` performs **compile-time type inference**
* Introduced in **Java 10**
* Works **only for local variables**
* Requires an **initializer**
* Improves **readability**, not dynamic typing
* Type is **fixed once inferred**

---

### Example Program

```java
public class VarExample {
    public static void main(String[] args) {
        var count = 10;           // int
        var message = "Hello";    // String
        var numbers = new int[5]; // int[]

        System.out.println(count);
        System.out.println(message);
        System.out.println(numbers.length);
    }
}
```

---

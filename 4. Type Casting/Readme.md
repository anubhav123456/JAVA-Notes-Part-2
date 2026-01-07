
---

## **Type Casting in Java**

Type casting is the process of converting a value from one data type to another.

Java supports **two types of type casting**:

1. **Implicit (Widening) Type Casting**
2. **Explicit (Narrowing) Type Casting**

---

## **1. Implicit / Widening Type Casting**

### **Definition**

Widening casting happens **automatically** when a value of a **smaller data type** is converted to a **larger data type**.

### **Order of Widening Conversion**

```
byte → short → char → int → long → float → double
```

👉 You can cast **any data type to the right** of it in the above sequence.

### **Key Points**

* Done **automatically by Java**
* No data loss
* Safe conversion

---

### **Example**

```java
public class Main {
    public static void main(String[] args) {
        int myInt = 9;
        double myDouble = myInt; // automatic conversion
        System.out.println(myInt);
        System.out.println(myDouble);
    }
}
```

### **Output**

```
9
9.0
```

---

### **Course Example (Implicit Casting)**

```java
package com.amigoscode;

public class Main {
    public static void main(String[] args) {
        // Implicit Type (Widening) Casting
        System.out.println("Implicit Type (Widening) Casting");

        int balance = 100;
        double balanceInDouble = balance;

        System.out.println(balance);
        System.out.println(balanceInDouble);
    }
}
```

---

## **2. Explicit / Narrowing Type Casting**

### **Definition**

Narrowing casting must be done **manually** because it converts a **larger data type** into a **smaller data type**.

### **Order of Narrowing Conversion**

```
double → float → long → int → char → short → byte
```

### **Key Points**

* Requires **manual casting**
* Risk of **data loss**
* Fractional values are **truncated**

---

### **Syntax**

```java
(targetType) value
```

---

### **Example**

```java
public class Main {
    public static void main(String[] args) {
        double myDouble = 9.78;
        int myInt = (int) myDouble; // manual conversion

        System.out.println(myDouble);
        System.out.println(myInt);
    }
}
```

### **Output**

```
9.78
9
```

📌 **Note:** Decimal part is removed (not rounded).

---

### **Course Example (Explicit Casting)**

```java
package com.amigoscode;

public class Main {
    public static void main(String[] args) {
        // Explicit Type (Narrowing) Casting
        System.out.println("Explicit Type (Narrowing) Casting");

        double remainingBalance = 100.55;
        int remainingBalanceInt = (int) remainingBalance;

        System.out.println(remainingBalance);
        System.out.println(remainingBalanceInt);
    }
}
```

---

## **Comparison Table**

| Feature              | Widening Casting | Narrowing Casting |
| -------------------- | ---------------- | ----------------- |
| Automatic            | ✅ Yes            | ❌ No              |
| Manual Cast Required | ❌ No             | ✅ Yes             |
| Data Loss            | ❌ No             | ✅ Possible        |
| Example              | int → double     | double → int      |

---

## **Summary**

* **Widening casting** is safe and automatic
* **Narrowing casting** is manual and may cause data loss
* Fractional values are **truncated** during narrowing

---

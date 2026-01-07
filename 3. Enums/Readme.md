
---

## 📘 Java Enums

### 🔹 What is an Enum?

* An **enum (enumeration)** is a special Java type used to define a **fixed set of constants**.
* It represents a **finite collection of related values**.
* Common use cases:

  * Days of the week
  * Months of the year
  * Status values (ACTIVE, INACTIVE, PENDING)
  * Roles (ADMIN, USER, GUEST)

---

### 🔹 Why Use Enums?

* Improves **code readability**
* Provides **type safety** (prevents invalid values)
* Makes code **more maintainable**
* Eliminates the need for magic strings or numbers

---

### 🔹 Defining an Enum

* Enums are declared using the `enum` keyword.
* Enum constants are **public, static, and final by default**.
* Constants are written in **UPPERCASE** by convention.

```java
enum Weekday {
    MONDAY,
    TUESDAY,
    WEDNESDAY,
    THURSDAY,
    FRIDAY,
    SATURDAY,
    SUNDAY
}
```

---

### 🔹 Using an Enum

* You can create variables of the enum type.
* Enum values are accessed using the **enum name** followed by the constant.

```java
Weekday day1 = Weekday.MONDAY;
```

---

### 🔹 Enums in Conditional Logic

* Enums work perfectly with `if-else`, `switch`, and collections.
* Enum values should be compared using `==` (safe and recommended).

---

### 🔹 Example: Checking Weekend Using Enum

```java
public static void isWeekend(Weekday day) {
    if (day == Weekday.SATURDAY || day == Weekday.SUNDAY) {
        System.out.println("Yay, it's the weekend! :)");
    } else {
        System.out.println("Nope, it's a plain old weekday :(");
    }
}
```

---

### 🔹 Alternative Approach Using Set

* Useful when checking against **multiple enum values**.

```java
if (Set.of(Weekday.SATURDAY, Weekday.SUNDAY).contains(day)) {
    System.out.println("Yay, it's the weekend! :)");
}
```

---

### 🔹 Complete Example

```java
package com.amigoscode;

public class Main {

    enum Weekday {
        MONDAY,
        TUESDAY,
        WEDNESDAY,
        THURSDAY,
        FRIDAY,
        SATURDAY,
        SUNDAY
    }

    public static void main(String[] args) {
        Weekday day1 = Weekday.MONDAY;
        isWeekend(day1);
    }

    public static void isWeekend(Weekday day) {
        if (day == Weekday.SATURDAY || day == Weekday.SUNDAY) {
            System.out.println("Yay, it's the weekend! :)");
        } else {
            System.out.println("Nope, it's a plain old weekday :(");
        }
    }
}
```

---

### 🔹 Key Takeaways

* Enums define a **restricted set of valid values**
* They act like **types**, not just constants
* Enum comparison should be done using `==`
* Enums help implement **clean and safe business logic**

---


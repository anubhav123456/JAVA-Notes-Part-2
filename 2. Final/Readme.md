# Java `final` Keyword

The `final` keyword in Java is used to **restrict modification**. It can be applied to:

* Variables
* Methods
* Classes

Depending on where it is used, its behavior changes.

---

## 1. Final Variable

When the `final` keyword is used with a variable:

* The value of the variable **cannot be changed** once assigned.
* It makes the variable a **constant**.

### Why use a final variable?

* When a value should remain the same across all instances of a class.
* To prevent accidental modification.

### Example

```java
public class FinalKeyword {

    private final int number = 3;
}
```

### Best Practice: `static final`

Generally, a `final` variable is also declared as `static` so:

* Only **one copy** exists across all instances of the class.
* Memory is optimized.

```java
public class FinalKeyword {

    public static final int NUMBER = 3;
}
```

---

## 2. Final Method

When the `final` keyword is applied to a method:

* The method **cannot be overridden** by subclasses.
* The method implementation remains fixed.

### Why use a final method?

* When the logic of a method should never change.
* To enforce consistent behavior in inheritance.

### Example

```java
public class FinalKeyword {

    public final void method() {
        // method implementation
    }
}
```

---

## 3. Final Class

When the `final` keyword is applied to a class:

* The class **cannot be extended**.
* No subclass can inherit from it.

### Why use a final class?

* When the class represents a complete, immutable concept.
* For security or design reasons.

### Example

```java
public final class FinalKeyword {
    // class implementation
}
```

---

## Summary Table

| Usage            | Effect                  |
| ---------------- | ----------------------- |
| `final` variable | Value cannot be changed |
| `final` method   | Cannot be overridden    |
| `final` class    | Cannot be inherited     |

---

## Key Takeaway

The `final` keyword helps in:

* Enforcing immutability
* Preventing unwanted inheritance
* Writing safer and more predictable code

---
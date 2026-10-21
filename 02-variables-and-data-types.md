# Chapter 2 — Variables and Data Types

> **Goal:** Store information and choose an appropriate type.

## What is a variable?

A variable is a named place used to store a value.

```java
int age = 15;
System.out.println(age);
```

`int` is the type, `age` is the name, and `15` is the value.

## Common data types

| Type | Stores | Example |
|---|---|---|
| `int` | Whole numbers | `int age = 15;` |
| `long` | Larger whole numbers | `long count = 8000000L;` |
| `float` | Decimal values | `float price = 12.5f;` |
| `double` | Decimal values | `double average = 78.65;` |
| `char` | One UTF-16 code unit | `char grade = 'A';` |
| `boolean` | `true` or `false` | `boolean passed = true;` |
| `String` | Text | `String name = "Riya";` |

`String` is a class, not a primitive type.

## Declaration and assignment

```java
int marks;       // Declaration
marks = 85;      // Assignment
int score = 90;  // Both together
```

Local variables must be assigned before they are read.

## Naming rules

Use meaningful names such as `totalMarks` and `studentName`. Names cannot start with a digit, contain spaces, or use Java keywords. `age` and `Age` are different names.

## Constants

```java
final double PI = 3.14159;
```

A `final` variable cannot be reassigned after initialization.

## Practice

1. Store your name, age and favourite character.
2. Store marks in three subjects and display them.
3. Store an item's price and quantity.
4. Change a variable's value and print it before and after.
5. Choose suitable data types for a price, grade, count and yes/no answer.
6. Fix invalid variable names in a short program.

<details><summary>Hints</summary>

- **Tip 1:** Decide what kind of value is stored.
- **Tip 2:** Use double quotes for `String`, single quotes for `char`.
- **Tip 3:** Choose descriptive variable names.
</details>

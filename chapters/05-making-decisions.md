# Chapter 5: Making Decisions with `if` and `else`

> **Today’s goal:** Make a program choose what to do based on a condition.

---

## 1. Programs can make decisions

Imagine a program checking whether a student passed.

```text
             Marks entered
                   │
                   ▼
             Are marks >= 40?
                /       \
              Yes        No
               │          │
               ▼          ▼
             Pass        Fail
```

We can write this logic using `if` and `else`.

---

## 2. A simple `if`

```java
int age = 18;

if (age >= 18) {
    System.out.println("You can vote.");
}
```

The code inside the braces runs only when the condition is true.

---

## 3. `if-else`

```java
int marks = 35;

if (marks >= 40) {
    System.out.println("Pass");
} else {
    System.out.println("Fail");
}
```

Output:

```text
Fail
```

If the condition is true, Java runs the `if` block. Otherwise, it runs the `else` block.

---

## 4. Comparison operators

| Operator | Meaning | Example |
|---|---|---|
| `==` | Equal to | `a == b` |
| `!=` | Not equal to | `a != b` |
| `>` | Greater than | `a > b` |
| `<` | Less than | `a < b` |
| `>=` | Greater than or equal to | `a >= b` |
| `<=` | Less than or equal to | `a <= b` |

Remember: `=` assigns a value. `==` compares two values.

---

## 5. More than two outcomes

```java
int marks = 76;

if (marks >= 80) {
    System.out.println("Grade A");
} else if (marks >= 60) {
    System.out.println("Grade B");
} else if (marks >= 40) {
    System.out.println("Pass");
} else {
    System.out.println("Fail");
}
```

Java checks each condition from top to bottom. The first true condition wins, so place higher ranges first.

---

## 6. Combining conditions

- `&&` means **AND**: both conditions must be true.
- `||` means **OR**: at least one condition must be true.
- `!` means **NOT**: it reverses true/false.

Example:

```java
int age = 20;
boolean hasTicket = true;

if (age >= 18 && hasTicket) {
    System.out.println("Entry allowed");
}
```

---

## Practice time

1. Check whether a number is positive, negative or zero.
2. Check whether a student passed using 40 as the pass mark.
3. Find the larger of two numbers.
4. Find the largest of three numbers.
5. Check whether a number is divisible by 3.
6. Check whether a number is divisible by both 3 and 5.
7. Check whether a person can vote using age 18.
8. Check whether a number is between 10 and 50, inclusive.
9. Display a grade based on marks.
10. Check whether a year is a leap year.
11. Check whether three lengths can form a triangle.
12. Apply a discount if a bill reaches a chosen amount.
13. Check whether a number has two digits.

<details>
<summary>Need a hint? Open this</summary>

- **Tip 1:** Write down all possible outcomes before coding.
- **Tip 2:** Use `&&` when both conditions must be true.
- **Tip 3:** Test values near the boundary, such as 39, 40 and 41.
</details>

---

## Quick recap

Conditions help a program choose what to do. Start with one simple `if`, then practise `if-else`, and only then move to several conditions.

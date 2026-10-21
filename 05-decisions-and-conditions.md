# Chapter 5 — Decisions and Conditions

> **Goal:** Make a program choose what to do based on a condition.

## Comparison operators

`==` equal, `!=` not equal, `>` greater, `<` less, `>=` greater than or equal, `<=` less than or equal.

## `if` and `if-else`

```java
int marks = 75;

if (marks >= 40) {
    System.out.println("Pass");
} else {
    System.out.println("Fail");
}
```

## `else-if` ladder

```java
if (marks >= 90) {
    System.out.println("Grade A+");
} else if (marks >= 80) {
    System.out.println("Grade A");
} else if (marks >= 70) {
    System.out.println("Grade B");
} else if (marks >= 40) {
    System.out.println("Pass");
} else {
    System.out.println("Fail");
}
```

Conditions are checked from top to bottom. Put higher ranges first.

## Logical operators

- `&&`: both conditions must be true.
- `||`: at least one condition must be true.
- `!`: reverses a boolean value.

```java
if (age >= 18 && hasID) {
    System.out.println("Entry allowed");
}
```

## Practice

1. Check whether a number is positive, negative or zero.
2. Display Pass or Fail using 40 as the pass mark.
3. Find the larger of two numbers and handle equality.
4. Find the largest of three numbers.
5. Check divisibility by both 3 and 5.
6. Check whether a year is a leap year.
7. Check voting eligibility.
8. Check whether a number lies between 10 and 50, inclusive.
9. Display a grade based on marks.
10. Check whether three lengths can form a triangle.
11. Classify a character as uppercase, lowercase, digit or other.
12. Apply a discount above a specified bill amount.
13. Check whether a number has two digits.
14. Display three numbers in ascending order.
15. Allow entry if the user is old enough or has permission.

<details><summary>Hints</summary>

- **Tip 1:** List the possible outcomes first.
- **Tip 2:** Use `&&` when all conditions must be true, `||` when one is enough.
- **Tip 3:** Test boundary values such as 39, 40 and 41.
</details>

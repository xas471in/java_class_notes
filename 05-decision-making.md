# Decision Making in Java — Class 10

## Goal
Use `if`, `if-else`, `else-if`, nested conditions and logical operators to make a program choose what to do.

## 1. Boolean conditions

A condition evaluates to `true` or `false`.

```java
int age = 18;
System.out.println(age >= 18); // true
```

## 2. `if`

```java
int marks = 75;

if (marks >= 40) {
    System.out.println("Pass");
}
```

The block runs only when the condition is true.

## 3. `if-else`

```java
int marks = 32;

if (marks >= 40) {
    System.out.println("Pass");
} else {
    System.out.println("Fail");
}
```

## 4. `else-if` ladder

```java
int marks = 86;

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

Conditions are checked from top to bottom. Put more specific or higher ranges first.

## 5. Relational operators

`==`, `!=`, `>`, `<`, `>=`, `<=`

```java
if (number != 0) {
    System.out.println("Not zero");
}
```

Remember: `=` assigns a value; `==` compares values.

## 6. Logical operators

- `&&` — AND: both conditions must be true.
- `||` — OR: at least one condition must be true.
- `!` — NOT: reverses a boolean value.

```java
int age = 20;
boolean hasID = true;

if (age >= 18 && hasID) {
    System.out.println("Entry allowed");
}
```

## 7. Nested `if`

```java
int marks = 75;
boolean submittedProject = true;

if (marks >= 40) {
    if (submittedProject) {
        System.out.println("Passed all requirements");
    } else {
        System.out.println("Project missing");
    }
} else {
    System.out.println("Failed marks requirement");
}
```

Use nested conditions when a decision depends on an earlier decision. Avoid unnecessary nesting when one clear logical condition is enough.

## Practice questions

1. Take an integer and display whether it is positive, negative or zero.
2. Take marks and display Pass or Fail. Pass mark: 40.
3. Take two numbers and display the larger; handle equality too.
4. Take three numbers and display the largest.
5. Check whether a number is divisible by both 3 and 5.
6. Check whether a year is a leap year.
7. Take age and check voting eligibility (18 or above).
8. Take a number and check whether it is between 10 and 50 inclusive.
9. Take marks and display a grade using an `else-if` ladder.
10. Check whether three side lengths can form a triangle.
11. Take a character and classify it as uppercase, lowercase, digit or other.
12. Take a bill total and apply a discount only when it meets a threshold.
13. Check whether a number is a two-digit number.
14. Take three numbers and display them in ascending order using conditions.
15. Take age and a permission boolean; allow entry if age is at least 18 or permission is true.

<details>
<summary>Hints</summary>

- **Tip 1:** Identify the possible outcomes before writing code.
- **Tip 2:** Use `&&` when every condition must be true and `||` when at least one must be true.
- **Tip 3:** Test boundary values such as 39, 40 and 41 for a pass-mark problem.
</details>

## Common mistakes

- Using `=` instead of `==`.
- Putting conditions in the wrong order.
- Forgetting braces or mismatching them.
- Using `||` when both conditions must be true.
- Forgetting boundary cases when using `>=` or `<=`.

## Checklist

- [ ] I can write `if` and `if-else`.
- [ ] I can use an `else-if` ladder.
- [ ] I understand relational and logical operators.
- [ ] I can trace nested conditions.

# Chapter 9: Patterns with Nested Loops

> **Today’s goal:** Use one loop inside another to print rows and columns.

---

## 1. What does “nested” mean?

A nested loop is a loop inside another loop.

Think of a classroom seating plan: the outer loop moves through rows, and the inner loop visits seats in each row.

```text
Outer loop: Row 1
   Inner loop: Seat 1, Seat 2, Seat 3

Outer loop: Row 2
   Inner loop: Seat 1, Seat 2, Seat 3
```

---

## 2. Print a rectangle

```java
for (int row = 1; row <= 3; row++) {
    for (int col = 1; col <= 4; col++) {
        System.out.print("* ");
    }

    System.out.println();
}
```

Output:

```text
* * * *
* * * *
* * * *
```

The outer loop runs 3 times. Each time it runs, the inner loop prints 4 stars.

---

## 3. Print a triangle

```java
for (int row = 1; row <= 4; row++) {
    for (int col = 1; col <= row; col++) {
        System.out.print("* ");
    }

    System.out.println();
}
```

Output:

```text
*
* *
* * *
* * * *
```

The number of stars depends on the current row.

---

## 4. Print a number triangle

```java
for (int row = 1; row <= 4; row++) {
    for (int col = 1; col <= row; col++) {
        System.out.print(col + " ");
    }

    System.out.println();
}
```

---

## Practice time

1. Print a square of stars.
2. Print a rectangle with 3 rows and 6 columns.
3. Print a right triangle.
4. Print an inverted triangle.
5. Print a number triangle.
6. Print the row number repeatedly in each row.
7. Print a multiplication grid.
8. Print a triangle of letters.
9. Print a right-aligned triangle.
10. Print a pyramid of stars.
11. Print a hollow square.
12. Print a grid showing row and column numbers.

<details>
<summary>Need a hint? Open this</summary>

- **Tip 1:** First decide how many rows you need.
- **Tip 2:** Then decide how many items each row needs.
- **Tip 3:** Print a newline after the inner loop finishes.
</details>

---

## Quick recap

The outer loop usually controls rows. The inner loop controls what is printed in each row. Practise tracing both loop variables.

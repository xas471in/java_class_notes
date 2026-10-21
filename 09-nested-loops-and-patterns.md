# Chapter 9 — Nested Loops and Patterns

> **Goal:** Use an inner loop to print columns or repeated items in each row.

## Rectangle pattern

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

The outer loop controls rows; the inner loop controls columns.

## Right triangle

```java
for (int row = 1; row <= 4; row++) {
    for (int col = 1; col <= row; col++) {
        System.out.print("* ");
    }
    System.out.println();
}
```

## Number triangle

```java
for (int row = 1; row <= 4; row++) {
    for (int col = 1; col <= row; col++) {
        System.out.print(col + " ");
    }
    System.out.println();
}
```

## Practice

1. Print a square of stars.
2. Print a rectangle of 3 rows and 6 columns.
3. Print a right triangle and an inverted triangle.
4. Print a number triangle from 1 to the row number.
5. Repeat the row number that many times.
6. Print a multiplication grid.
7. Print a triangle of letters.
8. Print a right-aligned triangle.
9. Print a pyramid of stars.
10. Print a hollow square.
11. Print a pattern whose row lengths decrease each row.
12. Print an `n × n` grid showing row and column numbers.

<details><summary>Hints</summary>

- **Tip 1:** Decide how many rows are needed.
- **Tip 2:** Decide how many items each row contains.
- **Tip 3:** Print a newline after the inner loop finishes.
</details>

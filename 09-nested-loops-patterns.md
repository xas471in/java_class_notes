# Nested Loops and Patterns — Class 10 Java

## Goal
Understand nested loops and use row/column tracking to print simple patterns.

## 1. What is a nested loop?

A nested loop is a loop inside another loop. The outer loop often controls rows, while the inner loop controls columns or repeated items in each row.

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

The inner loop completes all its iterations for every outer-loop iteration.

## 2. Right triangle pattern

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

The number of columns depends on the current row.

## 3. Number triangle

```java
for (int row = 1; row <= 4; row++) {
    for (int col = 1; col <= row; col++) {
        System.out.print(col + " ");
    }
    System.out.println();
}
```

Output:
```text
1
1 2
1 2 3
1 2 3 4
```

## 4. Fixed columns vs row-based columns

- Rectangle: inner loop runs a fixed number of times.
- Triangle: inner loop limit depends on `row`.
- Inverted triangle: inner loop often runs from `row` through the total row count, or its limit decreases each row.

## 5. Trace table

For a triangle with 3 rows:

| Outer row | Inner loop values |
|---:|---|
| 1 | 1 |
| 2 | 1, 2 |
| 3 | 1, 2, 3 |

Trace one row at a time rather than trying to imagine the whole output at once.

## Practice questions

1. Print a 5 × 5 square of stars.
2. Print a rectangle of 3 rows and 6 columns.
3. Print a right triangle of stars with 5 rows.
4. Print an inverted right triangle.
5. Print rows containing `1`, then `1 2`, then `1 2 3`, up to `n`.
6. Print rows containing the row number repeated that many times.
7. Print a number triangle where each row contains numbers from 1 to the row number.
8. Print a multiplication grid from 1 to 5.
9. Print a triangle of letters starting from A.
10. Print a right-aligned triangle using spaces and stars.
11. Print a pyramid pattern using spaces and stars.
12. Print a hollow square pattern.
13. Print a 1-to-5 multiplication table using nested loops.
14. Print a pattern whose row lengths decrease from `n` to 1.
15. For a given `n`, print an `n × n` grid where each position displays its row and column numbers.

<details>
<summary>Hints</summary>

- **Tip 1:** Decide how many rows are needed.
- **Tip 2:** Decide how many characters or numbers belong in each row.
- **Tip 3:** Print a newline after the inner loop finishes, not inside it.
</details>

## Common mistakes

- Printing a newline inside the inner loop.
- Using a fixed inner-loop limit when the pattern requires a changing limit.
- Confusing row and column variables.
- Forgetting spaces between symbols.
- Updating the outer-loop variable inside the inner loop.

## Checklist

- [ ] I understand how nested loops execute.
- [ ] I can print rectangles and triangles.
- [ ] I can adjust the inner-loop limit to change a pattern.

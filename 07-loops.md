# Chapter 7 — Loops

> **Goal:** Repeat instructions using `for`, `while` and `do-while`.

## `for` loop

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

## `while` loop

```java
int i = 1;
while (i <= 5) {
    System.out.println(i);
    i++;
}
```

## `do-while` loop

```java
int i = 1;
do {
    System.out.println(i);
    i++;
} while (i <= 5);
```

A `do-while` body runs at least once. Notice the semicolon after its condition.

## Counters and accumulators

```java
int count = 0;
int sum = 0;

for (int i = 1; i <= 5; i++) {
    count++;
    sum += i;
}
```

A counter counts events. An accumulator keeps a running total.

## Practice

1. Print 1 to 10 and then 10 to 1.
2. Print even numbers from 1 to 100.
3. Calculate the sum from 1 to `n`.
4. Display a multiplication table.
5. Calculate factorial.
6. Count digits in a number.
7. Calculate digit sum.
8. Reverse an integer.
9. Check whether a number is a palindrome.
10. Check whether a number is prime.
11. Print numbers divisible by 7 in a range.
12. Accept numbers until 0 is entered, then display their sum.
13. Print a square of stars.
14. Print the first `n` multiples of a number.
15. Compare equivalent `for`, `while` and `do-while` loops.

<details><summary>Hints</summary>

- **Tip 1:** Identify the start, condition and update.
- **Tip 2:** Start sums at 0 and products at 1.
- **Tip 3:** Trace the loop with a small input first.
</details>

## Common mistakes

- Forgetting to update the loop variable.
- Creating an infinite loop.
- Using the wrong loop boundary.
- Starting a product accumulator at 0.

# Loops in Java — Class 10

## Goal
Repeat statements using `for`, `while` and `do-while` loops. Learn counters, accumulators and loop tracing.

## 1. Why use loops?

A loop repeats code while a condition or loop rule allows it. It avoids writing the same statement many times.

## 2. `for` loop

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

Parts:
- Initialization: `int i = 1`
- Condition: `i <= 5`
- Update: `i++`

## 3. `while` loop

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
}
```

The condition is checked before each iteration. If it is false at the start, the body does not run.

## 4. `do-while` loop

```java
int i = 1;

do {
    System.out.println(i);
    i++;
} while (i <= 5);
```

The body runs at least once because the condition is checked after the body. Remember the semicolon after `while (...)`.

## 5. Counters and accumulators

A **counter** counts events; an **accumulator** collects a running total.

```java
int count = 0;
int sum = 0;

for (int i = 1; i <= 5; i++) {
    count++;
    sum += i;
}

System.out.println("Count = " + count); // 5
System.out.println("Sum = " + sum);     // 15
```

## 6. Looping with a condition

```java
for (int i = 1; i <= 10; i++) {
    if (i % 2 == 0) {
        System.out.println(i);
    }
}
```

## 7. `break` and `continue`

- `break` exits the loop.
- `continue` skips the rest of the current iteration and moves to the next iteration.

```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) {
        continue;
    }
    System.out.println(i);
}
// 3 is skipped
```

Use these carefully; simple loops are easier to trace.

## Practice questions

1. Print numbers from 1 to 10.
2. Print numbers from 10 to 1.
3. Print all even numbers from 1 to 100.
4. Print all odd numbers from 1 to 100.
5. Calculate the sum of numbers from 1 to `n`.
6. Display the multiplication table of a number.
7. Calculate the factorial of a positive integer.
8. Count down from a number entered by the user to 1.
9. Count how many digits are in a positive integer.
10. Calculate the sum of digits of a number.
11. Reverse the digits of an integer.
12. Check whether a number is a palindrome.
13. Check whether a number is prime.
14. Display all numbers divisible by 7 in a given range.
15. Keep asking for numbers until the user enters 0, then display their sum.
16. Print a simple square of stars using a loop.
17. Print a sequence of the first `n` multiples of a number.
18. Compare the outputs of equivalent `for`, `while` and `do-while` loops.

<details>
<summary>Hints</summary>

- **Tip 1:** Write down the starting value, condition and update.
- **Tip 2:** For sums, initialize the accumulator to 0; for products such as factorial, initialize it to 1.
- **Tip 3:** Trace the loop with a small input before trying a large one.
</details>

## Common mistakes

- Forgetting to update the loop variable, creating an infinite loop.
- Using `<=` when `<` is intended, or vice versa.
- Initializing a sum to 1 or a product to 0 by mistake.
- Forgetting the semicolon after the `do-while` condition.
- Changing the loop variable unexpectedly inside the loop.

## Checklist

- [ ] I can use `for`, `while` and `do-while`.
- [ ] I understand counters and accumulators.
- [ ] I can use `break` and `continue`.
- [ ] I can trace a loop manually.

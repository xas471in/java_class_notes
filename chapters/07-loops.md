# Chapter 7: Repeating Work with Loops

> **Today’s goal:** Make Java repeat instructions without writing the same line again and again.

---

## 1. Why do we need loops?

Imagine displaying the numbers 1 to 100. Writing 100 print statements would be tedious.

A loop repeats a block of code for us.

```text
Start ──► Check condition ──► Run instructions
               ▲                    │
               └──── Update ◄───────┘
```

When the condition becomes false, the loop stops.

---

## 2. Your first `for` loop

```java
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

Output:

```text
1
2
3
4
5
```

Read it in three parts:

- `int i = 1` — start at 1.
- `i <= 5` — keep going while `i` is at most 5.
- `i++` — increase `i` by 1 each time.

---

## 3. A `while` loop

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
}
```

A `while` loop checks the condition before each repetition.

---

## 4. A `do-while` loop

```java
int i = 1;

do {
    System.out.println(i);
    i++;
} while (i <= 5);
```

A `do-while` loop runs its body at least once. Notice the semicolon after the condition.

---

## 5. Counters and totals

A **counter** counts how many times something happens. A **sum** variable keeps adding values.

```java
int sum = 0;

for (int i = 1; i <= 5; i++) {
    sum = sum + i;
}

System.out.println(sum); // 15
```

The values added are 1 + 2 + 3 + 4 + 5.

---

## Practice time

1. Print numbers from 1 to 10.
2. Print numbers from 10 down to 1.
3. Print even numbers from 1 to 100.
4. Display the multiplication table of a number.
5. Calculate the sum from 1 to `n`.
6. Calculate factorial of a number.
7. Count the digits in a number.
8. Find the sum of a number's digits.
9. Reverse a number.
10. Check whether a number is a palindrome.
11. Check whether a number is prime.
12. Keep accepting numbers until the user enters 0, then display their sum.
13. Print a square of stars.
14. Print the first `n` multiples of a number.

<details>
<summary>Need a hint? Open this</summary>

- **Tip 1:** Identify the starting value, stopping condition and update.
- **Tip 2:** Start a sum at `0`.
- **Tip 3:** Update the loop variable, or the loop may never stop.
</details>

---

## Quick recap

Loops are useful whenever an action must be repeated. Practise tracing the loop variable on paper before writing longer programs.

# Chapter 8: Number Puzzles with Digits

> **Today’s goal:** Break a number into digits and use those digits to solve small problems.

---

## 1. The secret of `% 10` and `/ 10`

Suppose the number is `583`.

```text
583 % 10  ──►  3       Gets the last digit
583 / 10  ──►  58      Removes the last digit (integer division)
```

Repeat the process to work through a number one digit at a time.

---

## 2. Find the sum of digits

For `583`, the sum is `5 + 8 + 3 = 16`.

```java
int number = 583;
int sum = 0;

while (number > 0) {
    int digit = number % 10;
    sum = sum + digit;
    number = number / 10;
}

System.out.println(sum); // 16
```

Try tracing `number` and `sum` after every loop.

---

## 3. Reverse a number

For example, `1234` becomes `4321`.

```java
int number = 1234;
int reversed = 0;

while (number > 0) {
    int digit = number % 10;
    reversed = reversed * 10 + digit;
    number = number / 10;
}

System.out.println(reversed); // 4321
```

Keep the original number separately if you need it for a later comparison.

---

## 4. Palindrome numbers

A number is a palindrome when it reads the same forward and backward.

Examples: `121`, `1331`, `7`.

Approach:

1. Save the original number.
2. Reverse its digits.
3. Compare the reversed number with the original.

---

## 5. Armstrong numbers

For a three-digit number, add the cube of each digit.

```text
153 = 1³ + 5³ + 3³
153 = 1 + 125 + 27
153 = 153
```

Since the sum equals the original number, 153 is a three-digit Armstrong number.

---

## Practice time

1. Display the last digit of a positive number.
2. Calculate the sum of digits.
3. Count the digits.
4. Reverse a number.
5. Check whether a number is a palindrome.
6. Check whether a three-digit number is Armstrong.
7. Display the first and last digits.
8. Count even and odd digits.
9. Find the largest digit.
10. Find the smallest digit.
11. Check whether a number contains digit 7.
12. Display all three-digit Armstrong numbers.
13. Display palindrome numbers in a range.
14. Check whether a number is a strong number.

<details>
<summary>Need a hint? Open this</summary>

- **Tip 1:** `% 10` gives the last digit.
- **Tip 2:** `/ 10` removes the last digit from a positive integer.
- **Tip 3:** Save the original number before changing it.
</details>

---

## Quick recap

Many number puzzles use the same two operations. Learn to extract one digit, process it, and remove it before moving to the next.

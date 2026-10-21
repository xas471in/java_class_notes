# Chapter 8 — Number and Digit Problems

> **Goal:** Use integer division and remainder to inspect digits.

## Extract and remove a digit

```java
int number = 583;
int lastDigit = number % 10; // 3
number = number / 10;        // 58
```

For positive integers, `% 10` gets the last digit and `/ 10` removes it.

## Sum of digits

```java
int number = 583;
int sum = 0;

while (number > 0) {
    int digit = number % 10;
    sum += digit;
    number /= 10;
}
System.out.println(sum); // 16
```

## Reverse a number

```java
int number = 1234;
int reversed = 0;

while (number > 0) {
    int digit = number % 10;
    reversed = reversed * 10 + digit;
    number /= 10;
}
System.out.println(reversed); // 4321
```

Save the original number if you need to compare it later.

## Palindrome

A palindrome reads the same forward and backward, such as 121. Save the original, reverse its digits, then compare the two values.

## Armstrong number

For a three-digit number, add the cube of each digit. `153 = 1³ + 5³ + 3³`.

```java
int number = 153;
int original = number;
int sum = 0;

while (number > 0) {
    int digit = number % 10;
    sum += digit * digit * digit;
    number /= 10;
}

System.out.println(sum == original ? "Armstrong" : "Not Armstrong");
```

This example uses the three-digit definition.

## Practice

1. Display the last digit of a positive number.
2. Calculate the sum and product of digits.
3. Count digits.
4. Reverse a number.
5. Check whether a number is a palindrome.
6. Check whether a three-digit number is Armstrong.
7. Display the first and last digits.
8. Count even and odd digits.
9. Find the largest and smallest digit.
10. Check whether a number contains digit 7.
11. Check whether a number is a strong number.
12. Display palindrome numbers in a range.
13. Display all three-digit Armstrong numbers.
14. Check whether a number is perfect.

<details><summary>Hints</summary>

- **Tip 1:** `% 10` extracts the last digit.
- **Tip 2:** `/ 10` removes the last digit.
- **Tip 3:** Save the original value before changing it.
</details>

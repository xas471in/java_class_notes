# Number Breakdown Algorithms — Class 10 Java

## Goal
Use integer division (`/`) and remainder (`%`) to examine digits, reverse numbers, and solve palindrome and Armstrong-number problems.

## 1. Extract the last digit

For a non-negative integer:

```java
int number = 583;
int lastDigit = number % 10;

System.out.println(lastDigit); // 3
```

## 2. Remove the last digit

```java
int number = 583;
number = number / 10;

System.out.println(number); // 58
```

Integer division removes the fractional part.

## 3. Sum the digits

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

Each loop extracts one digit and removes it from the number.

## 4. Count digits

```java
int number = 5830;
int count = 0;

if (number == 0) {
    count = 1;
} else {
    while (number > 0) {
        count++;
        number /= 10;
    }
}

System.out.println(count); // 4
```

This version assumes a non-negative input.

## 5. Reverse a number

```java
int number = 1234;
int original = number;
int reversed = 0;

while (number > 0) {
    int digit = number % 10;
    reversed = reversed * 10 + digit;
    number /= 10;
}

System.out.println(reversed); // 4321
```

The `reversed * 10` step shifts existing digits left before adding the new last digit.

## 6. Palindrome number

A palindrome reads the same forwards and backwards, such as 121 or 1331.

```java
int number = 121;
int original = number;
int reversed = 0;

while (number > 0) {
    int digit = number % 10;
    reversed = reversed * 10 + digit;
    number /= 10;
}

if (original == reversed) {
    System.out.println("Palindrome");
} else {
    System.out.println("Not a palindrome");
}
```

Keep the original number because the loop reduces `number` to zero.

## 7. Armstrong number (three-digit version)

A three-digit Armstrong number equals the sum of the cubes of its digits. For example, `153 = 1³ + 5³ + 3³`.

```java
int number = 153;
int original = number;
int sum = 0;

while (number > 0) {
    int digit = number % 10;
    sum += digit * digit * digit;
    number /= 10;
}

if (sum == original) {
    System.out.println("Armstrong number");
} else {
    System.out.println("Not an Armstrong number");
}
```

This example checks the three-digit definition. A general Armstrong-number algorithm raises each digit to the total number of digits.

## Practice questions

1. Display the last digit of a positive integer.
2. Remove the last digit from a positive integer.
3. Calculate the sum of the digits.
4. Calculate the product of the digits.
5. Count the digits in a number.
6. Reverse a number.
7. Check whether a number is a palindrome.
8. Check whether a three-digit number is an Armstrong number.
9. Display the first and last digits of a positive integer.
10. Count how many digits are even and how many are odd.
11. Find the largest digit in a number.
12. Find the smallest digit in a number.
13. Check whether a number contains the digit 7.
14. Check whether a number is a strong number (sum of factorials of its digits equals the number).
15. Display all palindrome numbers in a given range.
16. Display all three-digit Armstrong numbers.
17. Check whether a number is a perfect number.
18. Reverse a number and compare it with the original without using String conversion.

<details>
<summary>Hints</summary>

- **Tip 1:** `% 10` extracts the last digit.
- **Tip 2:** `/ 10` removes the last digit.
- **Tip 3:** Save the original number before the loop if you need to compare it afterwards.
</details>

## Common mistakes

- Forgetting to save the original number.
- Using `number % 10` after the number has already become 0.
- Forgetting to update `number /= 10`, causing an infinite loop.
- Not handling 0 as a special case for digit counting.
- Using cubes for every Armstrong-number definition; the power depends on the number of digits in the general definition.

## Checklist

- [ ] I can extract and remove digits.
- [ ] I can calculate a digit sum.
- [ ] I can reverse a number.
- [ ] I can test palindrome and Armstrong numbers.

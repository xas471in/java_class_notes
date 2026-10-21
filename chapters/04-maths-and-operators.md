# Chapter 4: Making Calculations

> **Today’s goal:** Use Java to do the calculations we already know from maths.

---

## 1. Java can be a calculator

```java
int a = 10;
int b = 3;

System.out.println(a + b); // Addition
System.out.println(a - b); // Subtraction
System.out.println(a * b); // Multiplication
System.out.println(a / b); // Division
System.out.println(a % b); // Remainder
```

Output:

```text
13
7
30
3
1
```

The `%` operator gives the remainder. For example, `10 % 3` is `1` because 3 goes into 10 three times with 1 left over.

---

## 2. An important division rule

When both numbers are integers, Java keeps only the whole-number part of the answer.

```java
System.out.println(10 / 3);   // 3
System.out.println(10.0 / 3); // 3.333...
```

Use `double` when you need a decimal answer.

---

## 3. Order of calculations

Java follows the usual order of operations.

```java
System.out.println(2 + 3 * 4);   // 14
System.out.println((2 + 3) * 4); // 20
```

Use brackets when you want a particular part calculated first.

---

## 4. Useful methods from `Math`

| Method | What it does | Example |
|---|---|---|
| `Math.sqrt(25)` | Square root | `5.0` |
| `Math.pow(2, 3)` | Power | `8.0` |
| `Math.abs(-7)` | Removes the negative sign | `7` |
| `Math.max(4, 9)` | Returns the larger value | `9` |
| `Math.min(4, 9)` | Returns the smaller value | `4` |

In Java, `^` does **not** mean “power”. Use `Math.pow()`.

---

## 5. Example: Calculate simple interest

Formula:

```text
Simple Interest = (Principal × Rate × Time) / 100
```

Java code:

```java
double principal = 1000;
double rate = 5;
double time = 2;

double interest = (principal * rate * time) / 100;

System.out.println("Simple interest = " + interest);
```

Output:

```text
Simple interest = 100.0
```

---

## Practice time

1. Read two numbers and display their sum, difference and product.
2. Calculate the area of a rectangle.
3. Calculate the perimeter of a rectangle.
4. Calculate the average of three marks.
5. Display the square and cube of a number.
6. Find the square root of a number.
7. Calculate simple interest.
8. Convert Celsius to Fahrenheit.
9. Convert seconds into minutes and remaining seconds.
10. Calculate the total cost of items with the same price.
11. Predict the output of `2 + 5 * 3` and `(2 + 5) * 3`.

<details>
<summary>Need a hint? Open this</summary>

- **Tip 1:** Write the maths formula first.
- **Tip 2:** Use `double` if the answer may contain decimals.
- **Tip 3:** Test your result with small numbers you can calculate by hand.
</details>

---

## Quick recap

Java uses familiar arithmetic symbols. Remember that integer division drops the decimal part, and parentheses help control the order of calculations.

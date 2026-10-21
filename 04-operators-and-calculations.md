# Chapter 4 — Operators and Calculations

> **Goal:** Perform calculations and translate formulas into Java.

## Arithmetic operators

| Operator | Meaning |
|---|---|
| `+` | Addition |
| `-` | Subtraction |
| `*` | Multiplication |
| `/` | Division |
| `%` | Remainder |

```java
int a = 17;
int b = 5;

System.out.println(a + b); // 22
System.out.println(a - b); // 12
System.out.println(a * b); // 85
System.out.println(a / b); // 3
System.out.println(a % b); // 2
```

Integer division discards the fractional part. `17.0 / 5` gives `3.4`.

## Operator precedence

```java
System.out.println(2 + 3 * 4);   // 14
System.out.println((2 + 3) * 4); // 20
```

## Math methods

| Method | Purpose |
|---|---|
| `Math.pow(a, b)` | a raised to power b |
| `Math.sqrt(x)` | Square root |
| `Math.abs(x)` | Absolute value |
| `Math.max(a, b)` | Larger value |
| `Math.min(a, b)` | Smaller value |
| `Math.round(x)` | Round to nearest whole value |

`^` is not the power operator in Java; use `Math.pow()`.

## Example: Simple interest

```java
double principal = 1000;
double rate = 5;
double time = 2;

double interest = (principal * rate * time) / 100;
System.out.println(interest); // 100.0
```

## Practice

1. Display all arithmetic results for two numbers.
2. Calculate rectangle area and perimeter.
3. Calculate circle area and circumference.
4. Calculate the average of three marks without losing decimals.
5. Display the square and cube of a number.
6. Find a square root.
7. Calculate simple interest.
8. Convert Celsius to Fahrenheit.
9. Convert seconds to minutes and remaining seconds.
10. Calculate a right triangle's hypotenuse.
11. Predict results of expressions using parentheses.
12. Calculate the cost of several identical items.

<details><summary>Hints</summary>

- **Tip 1:** Write the formula first.
- **Tip 2:** Use `double` when decimal results matter.
- **Tip 3:** Test with values you can calculate manually.
</details>

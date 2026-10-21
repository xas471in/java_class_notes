# Calculations and Math Functions — Class 10 Java

## Goal
Perform arithmetic, understand operator precedence and use common methods from Java's `Math` class.

## 1. Arithmetic operators

| Operator | Meaning | Example |
|---|---|---|
| `+` | Addition | `a + b` |
| `-` | Subtraction | `a - b` |
| `*` | Multiplication | `a * b` |
| `/` | Division | `a / b` |
| `%` | Remainder | `a % b` |

```java
int a = 17;
int b = 5;

System.out.println(a + b); // 22
System.out.println(a - b); // 12
System.out.println(a * b); // 85
System.out.println(a / b); // 3
System.out.println(a % b); // 2
```

When both operands are integers, division discards the fractional part. Use a `double` operand for decimal division.

```java
System.out.println(17 / 5);       // 3
System.out.println(17.0 / 5);     // 3.4
System.out.println((double) 17 / 5); // 3.4
```

## 2. Operator precedence

Multiplication and division are performed before addition and subtraction. Parentheses can change the order.

```java
System.out.println(2 + 3 * 4);   // 14
System.out.println((2 + 3) * 4); // 20
```

## 3. Assignment shortcuts

```java
int x = 10;
x += 5; // x = x + 5
x -= 2; // x = x - 2
x *= 3; // x = x * 3
x /= 2; // x = x / 2
```

## 4. Useful Math methods

| Method | Purpose | Example |
|---|---|---|
| `Math.pow(a, b)` | a raised to power b | `Math.pow(2, 3)` → `8.0` |
| `Math.sqrt(x)` | Square root | `Math.sqrt(25)` → `5.0` |
| `Math.abs(x)` | Absolute value | `Math.abs(-7)` → `7` |
| `Math.max(a, b)` | Larger value | `Math.max(4, 9)` → `9` |
| `Math.min(a, b)` | Smaller value | `Math.min(4, 9)` → `4` |
| `Math.round(x)` | Rounds to nearest long/int form | `Math.round(4.6)` → `5` |
| `Math.ceil(x)` | Rounds upward to an integer-valued double | `Math.ceil(4.1)` → `5.0` |
| `Math.floor(x)` | Rounds downward to an integer-valued double | `Math.floor(4.9)` → `4.0` |

`Math.pow()` returns a `double`, so use a suitable variable type or cast only when you understand the possible loss of information.

## 5. Formula examples

### Area of a rectangle

```java
double length = 8.5;
double breadth = 4.0;
double area = length * breadth;

System.out.println("Area = " + area);
```

### Area of a circle

```java
double radius = 7;
double area = Math.PI * radius * radius;

System.out.println("Area = " + area);
```

### Pythagorean theorem

For a right-angled triangle: `c = sqrt(a² + b²)`.

```java
double a = 3;
double b = 4;
double c = Math.sqrt(Math.pow(a, 2) + Math.pow(b, 2));

System.out.println(c); // 5.0
```

## Practice questions

1. Take two numbers and display all five arithmetic results.
2. Calculate the area and perimeter of a rectangle.
3. Calculate the area and circumference of a circle.
4. Take three marks and calculate their average without integer truncation.
5. Take a number and display its square and cube using `Math.pow()`.
6. Take a positive number and display its square root.
7. Take two numbers and display the larger using `Math.max()`.
8. Take a negative or positive number and display its absolute value.
9. Convert total seconds into minutes and remaining seconds using `/` and `%`.
10. Calculate the hypotenuse of a right-angled triangle.
11. Predict the output of expressions with parentheses and mixed operators.
12. Calculate simple interest using `SI = (P * R * T) / 100`.

<details>
<summary>Hints</summary>

- **Tip 1:** Write the formula on paper before coding.
- **Tip 2:** Use `double` for calculations that may contain decimals.
- **Tip 3:** Test with small values whose answers you can calculate manually.
</details>

## Common mistakes

- Expecting `17 / 5` to return `3.4`.
- Forgetting parentheses in a formula.
- Using `^` for powers: in Java, `^` is bitwise XOR, not exponentiation.
- Forgetting that `Math.pow()` returns a `double`.
- Using an incorrect formula or mixing units.

## Checklist

- [ ] I can use arithmetic operators.
- [ ] I understand integer division and remainder.
- [ ] I can trace operator precedence.
- [ ] I can use `Math.pow()` and `Math.sqrt()`.
- [ ] I can translate a formula into Java.

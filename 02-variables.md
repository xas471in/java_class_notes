# Java Variables — Class 10 Learning Guide

> **Goal:** Understand how variables work in Java, choose the right data type, and practise writing programs independently.
>
> **How to use this guide**
> 1. Read one concept at a time.
> 2. Type and run each example yourself.
> 3. Predict the output before running the program.
> 4. Attempt the practice questions before opening the hints.
> 5. Use **Tip 1** first. Read Tip 2 only if you are still stuck.

---

## Contents

- [Level 1 — Basics](#level-1--basic-variables)
- [Level 2 — Intermediate](#level-2--intermediate-variables)
- [Level 3 — Advanced](#level-3--advanced-variables)
- [Level 4 — Mixed Practice](#level-4--mixed-practice)
- [Common Mistakes](#common-mistakes)
- [Answer Key](#answer-key)

---

# Level 1 — Basic Variables

## 1. What is a variable?

A **variable** is a named place used to store a value in a program. The value can be used or changed while the program runs, depending on how the variable is declared.

```java
int age = 15;
System.out.println(age); // 15
```

Here:
- `int` is the data type.
- `age` is the variable name.
- `15` is the value stored in the variable.
- `=` is the assignment operator.

## 2. Declaring and initializing a variable

### Declaration

Declaration tells Java the variable's name and data type.

```java
int marks;
```

### Initialization

Initialization means giving a variable its first value.

```java
marks = 85;
```

### Declaration and initialization together

```java
int marks = 85;
```

A variable declared without a value cannot be read until it has been assigned a value.

## 3. Basic data types

Java has several primitive data types. These are the most common ones for beginner programs.

| Data type | Stores | Example |
|---|---|---|
| `int` | Whole numbers | `int age = 15;` |
| `long` | Larger whole numbers | `long population = 8000000L;` |
| `float` | Decimal values, lower precision | `float price = 12.5f;` |
| `double` | Decimal values, higher precision | `double average = 78.65;` |
| `char` | One character | `char grade = 'A';` |
| `boolean` | `true` or `false` | `boolean passed = true;` |

Text is commonly stored in a `String`. `String` is a class, not a primitive data type.

```java
String name = "Riya";
```

**Remember:**
- A `char` value uses single quotes: `'A'`.
- A `String` value uses double quotes: `"Java"`.
- Use `f` at the end of a decimal literal when assigning it directly to a `float`.
- Use `L` for a `long` literal when needed.

## 4. Printing variables

```java
int age = 15;
String name = "Riya";

System.out.println(name);
System.out.println(age);
System.out.println("Name: " + name);
System.out.println("Age: " + age);
```

The `+` operator joins text and values when one side is a `String`.

## 5. Changing a variable's value

```java
int score = 10;
System.out.println(score); // 10

score = 20;
System.out.println(score); // 20
```

The variable is still named `score`, but its stored value changes.

## 6. Taking input with `Scanner`

The `Scanner` class lets a program read input from the user.

```java
import java.util.Scanner;

class UserInput {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your age: ");
        int age = sc.nextInt();

        System.out.println("Your age is " + age);

        sc.close();
    }
}
```

Useful `Scanner` methods:

| Method | Input type |
|---|---|
| `nextInt()` | Integer |
| `nextLong()` | Long integer |
| `nextFloat()` | Float |
| `nextDouble()` | Double |
| `nextBoolean()` | Boolean |
| `next()` | One word/token |
| `nextLine()` | A complete line of text |

### Important: `nextLine()` after `nextInt()`

Methods such as `nextInt()` leave the line break in the input. If you then call `nextLine()`, it may read that remaining line break instead of the text you expect.

```java
int age = sc.nextInt();
sc.nextLine(); // Consume the leftover line break
String name = sc.nextLine();
```

## 7. Operators used with variables

### Arithmetic operators

| Operator | Meaning | Example |
|---|---|---|
| `+` | Addition | `a + b` |
| `-` | Subtraction | `a - b` |
| `*` | Multiplication | `a * b` |
| `/` | Division | `a / b` |
| `%` | Remainder | `a % b` |

Example:

```java
int a = 17;
int b = 5;

System.out.println(a + b); // 22
System.out.println(a - b); // 12
System.out.println(a * b); // 85
System.out.println(a / b); // 3
System.out.println(a % b); // 2
```

**Important:** When both operands are integers, `/` performs integer division. The decimal part is discarded.

```java
System.out.println(17 / 5);        // 3
System.out.println(17.0 / 5);      // 3.4
System.out.println((double) 17 / 5); // 3.4
```

### Assignment operators

```java
int x = 10;

x += 5; // Same idea as x = x + 5
x -= 2; // Same idea as x = x - 2
x *= 3; // Same idea as x = x * 3
x /= 2; // Same idea as x = x / 2
x %= 4; // Same idea as x = x % 4
```

### Increment and decrement

```java
int x = 5;

x++; // Increase x by 1
x--; // Decrease x by 1
```

The difference between `x++` and `++x` matters when the expression's value is used in a larger expression. Learn the simple update first, then practise prefix and postfix examples carefully.

## 8. Naming variables

Valid examples:

```java
int age;
double totalMarks;
String studentName;
int number2;
```

Invalid examples:

```java
// int 2number = 10;   // Cannot start with a digit
// int student name;   // Spaces are not allowed
// int class = 10;     // 'class' is a Java keyword
```

Common naming rules:
1. A variable name cannot start with a digit.
2. It may contain letters, digits, `_` and `$`.
3. Spaces are not allowed.
4. Java keywords cannot be used as variable names.
5. Java is case-sensitive: `age` and `Age` are different names.
6. Use meaningful names such as `totalMarks` instead of `x` when possible.

## 9. Type conversion

### Widening conversion

A value can often be stored in a wider compatible type automatically.

```java
int number = 25;
double value = number;

System.out.println(value); // 25.0
```

### Narrowing conversion

A conversion from a wider type to a narrower type may need an explicit cast and may lose information.

```java
double price = 19.75;
int wholePrice = (int) price;

System.out.println(wholePrice); // 19
```

Casting a `double` to an `int` removes the decimal part; it does not round to the nearest integer.

## 10. Local variables and fields

For now, most exercises will use variables declared inside `main()`.

```java
class Example {
    public static void main(String args[]) {
        int age = 15; // Local variable
        System.out.println(age);
    }
}
```

A local variable must be assigned a value before it is read. Fields (variables declared in a class but outside a method) have default values, but local variables do not.

## 11. Basic practice questions

Write a separate Java program for each question.

1. Declare an integer variable and display its value.
2. Store your name, age and class in variables and display them.
3. Take two integers from the user and display their sum.
4. Take two numbers and display their sum, difference, product and quotient.
5. Take the length and breadth of a rectangle and calculate its area.
6. Take the side of a square and calculate its perimeter.
7. Take the radius of a circle and calculate its area using `3.14`.
8. Take marks in three subjects and calculate the total and average.
9. Take a temperature in Celsius and convert it to Fahrenheit using `F = (C * 9 / 5) + 32`. Use decimal values when needed.
10. Take a number and display its remainder when divided by 2.
11. Swap two variables using a temporary variable.
12. Convert a `double` value to an `int` using casting and display both values.
13. Take a student's name and favourite character and display both.
14. Take the price and quantity of an item and calculate the total cost.
15. Take a number of seconds and convert it into whole minutes and remaining seconds.

### Hints for selected basic questions

<details>
<summary>Question 4 — Arithmetic operations</summary>

- **Tip 1:** Store the two input numbers in separate variables.
- **Tip 2:** Calculate each operation separately.
- **Tip 3:** Check that the divisor is not zero before dividing.
</details>

<details>
<summary>Question 8 — Total and average</summary>

- **Tip 1:** Add all three marks to calculate the total.
- **Tip 2:** Divide the total by 3 to calculate the average.
- **Tip 3:** Use `double` or cast one operand to `double` if you need a decimal average.
</details>

<details>
<summary>Question 11 — Swap two values</summary>

- **Tip 1:** Create a third variable called `temp`.
- **Tip 2:** Store the first value in `temp`.
- **Tip 3:** Copy the second value to the first, then copy `temp` to the second.
</details>

---

# Level 2 — Intermediate Variables

## 1. Comparison operators

Comparison operators compare two values and produce a boolean result (`true` or `false`).

| Operator | Meaning |
|---|---|
| `==` | Equal to |
| `!=` | Not equal to |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |

```java
int a = 10;
int b = 20;

System.out.println(a == b); // false
System.out.println(a != b); // true
System.out.println(a < b);  // true
System.out.println(a >= b); // false
```

Do not confuse `=` (assignment) with `==` (comparison).

## 2. Logical operators

Logical operators combine or reverse boolean conditions.

| Operator | Meaning |
|---|---|
| `&&` | AND — both conditions must be true |
| `||` | OR — at least one condition must be true |
| `!` | NOT — reverses a boolean result |

```java
int age = 16;
boolean hasPermission = true;

System.out.println(age >= 18 && hasPermission); // false
System.out.println(age >= 18 || hasPermission); // true
System.out.println(!hasPermission);             // false
```

Java's `&&` and `||` use short-circuit evaluation: Java may skip the second condition when the first condition already determines the result.

## 3. Variables with `if-else`

```java
int marks = 65;

if (marks >= 40) {
    System.out.println("Pass");
} else {
    System.out.println("Fail");
}
```

The condition `marks >= 40` evaluates to either `true` or `false`.

## 4. Ternary operator

The ternary operator is a shorter way to choose between two values based on a condition.

Syntax:

```java
result = condition ? valueIfTrue : valueIfFalse;
```

Example:

```java
int age = 17;
String result = age >= 18 ? "Adult" : "Minor";

System.out.println(result); // Minor
```

For beginners, use `if-else` when it makes the logic easier to understand.

## 5. Variable scope

**Scope** means the part of the program where a variable can be accessed.

```java
int number = 10;

if (number > 0) {
    int messageCode = 1;
    System.out.println(messageCode);
}

// messageCode cannot be accessed here.
```

A variable declared inside a block `{ }` is generally accessible only within that block.

## 6. `final` variables (constants)

Use `final` when a variable should not be reassigned after it has been initialized.

```java
final double PI = 3.14159;

System.out.println(PI);

// PI = 3.14; // Compilation error
```

Constant names are often written in uppercase by convention.

## 7. Prefix and postfix increment

```java
int a = 5;
int first = a++;
System.out.println(first); // 5
System.out.println(a);     // 6

int b = 5;
int second = ++b;
System.out.println(second); // 6
System.out.println(b);      // 6
```

- `a++`: use the old value in the expression, then increase the variable.
- `++b`: increase the variable first, then use the new value.

When learning, avoid putting multiple `++` operations into one complicated expression.

## 8. Intermediate practice questions

1. Take two numbers and display whether they are equal.
2. Take a number and check whether it is divisible by both 3 and 5.
3. Take a student's marks and display Pass or Fail (pass mark: 40).
4. Take a person's age and display whether they are eligible to vote, assuming the minimum age is 18.
5. Take three numbers and display the largest.
6. Take a year and check whether it is a leap year.
7. Take a character and check whether it is an uppercase or lowercase English letter.
8. Take a number and check whether it lies between 10 and 100, inclusive.
9. Take a bill amount and apply a 10% discount if the bill is at least 1,000.
10. Use the ternary operator to display the larger of two numbers.
11. Use a `final` variable to store a fixed tax rate and calculate the tax on an amount.
12. Predict the output of prefix and postfix increment examples before running them.
13. Take a number and check whether it is a two-digit number.
14. Take marks and display a grade using an `if-else-if` ladder.
15. Take three side lengths and check whether they can form a triangle.

### Hints for selected intermediate questions

<details>
<summary>Question 2 — Divisible by both 3 and 5</summary>

- **Tip 1:** Use the remainder operator `%`.
- **Tip 2:** A number is divisible by 3 when `number % 3 == 0`.
- **Tip 3:** Combine both checks using `&&`.
</details>

<details>
<summary>Question 6 — Leap year</summary>

- **Tip 1:** A year divisible by 400 is a leap year.
- **Tip 2:** Otherwise, a year divisible by 100 is not a leap year.
- **Tip 3:** Otherwise, a year divisible by 4 is a leap year.
</details>

<details>
<summary>Question 9 — Discount</summary>

- **Tip 1:** Store the bill amount in a numeric variable.
- **Tip 2:** Check whether the amount is at least 1000.
- **Tip 3:** Calculate the discount as `amount * 0.10` and subtract it from the original amount.
</details>

---

# Level 3 — Advanced Variable Practice

This level focuses on combining variables, expressions, casting, conditions and careful tracing. These are not separate advanced data structures.

## 1. Integer division and casting

```java
int total = 7;
int count = 2;

double average = (double) total / count;

System.out.println(average); // 3.5
```

Casting `total` before division makes the division use decimal arithmetic.

This does **not** work the same way:

```java
double average = total / count;
```

Since both operands are integers, `total / count` is evaluated as integer division first, producing `3`, which is then stored as `3.0`.

## 2. Operator precedence

Java evaluates some operators before others. Parentheses can make the intended order clear.

```java
int result1 = 2 + 3 * 4;   // 14
int result2 = (2 + 3) * 4; // 20
```

Multiplication happens before addition unless parentheses change the order.

## 3. Numeric limits and overflow

An `int` has a limited range. If a calculation exceeds that range, the result can overflow.

```java
int number = 2_000_000_000;
long larger = 2_000_000_000L;

System.out.println(number);
System.out.println(larger);
```

Use a suitable data type for the expected size of the value. Storing an already-overflowed `int` result in a `long` does not undo the overflow; the calculation itself must use a wider type where appropriate.

## 4. Floating-point values

Floating-point values can have small representation inaccuracies.

```java
double value = 0.1 + 0.2;
System.out.println(value);
```

The displayed result may not be exactly `0.3`. For beginner calculations, this is a useful reminder that decimal values are not always represented perfectly in binary.

## 5. Character values and numeric codes

A `char` stores one UTF-16 code unit. English letters and digits can be checked using methods from `Character`.

```java
char ch = 'A';

System.out.println(Character.isLetter(ch)); // true
System.out.println(Character.isDigit(ch));  // false
System.out.println(Character.isUpperCase(ch)); // true
```

For normal Class 10 programs, use these methods rather than memorising numeric character codes.

## 6. Advanced practice questions

1. Take two integers and swap their values using a temporary variable.
2. Take three numbers and rotate their values: first gets second, second gets third, third gets first.
3. Take total marks and maximum marks, then calculate the percentage as a decimal.
4. Predict the result of expressions mixing `int` and `double`.
5. Take a number of seconds and convert it into hours, minutes and seconds.
6. Take an amount and calculate how many notes of denominations 500, 200, 100, 50, 20 and 10 are needed using the largest denominations first. Assume a non-negative amount divisible by 10.
7. Take a three-digit integer and calculate the sum of its digits using `/` and `%`.
8. Take a three-digit integer and reverse its digits.
9. Take a character and display whether it is a letter, digit or other character.
10. Take the base and exponent for a small non-negative integer power and calculate the result using repeated multiplication.
11. Take a bill amount and calculate the final amount after a discount and tax.
12. Given two integer values, calculate their average without accidentally performing integer division.
13. Read a number and check whether it is within the range 1 to 100.
14. Trace a program containing `x++`, `++x`, `+=` and parentheses; write each variable's value after every statement.
15. Explain why assigning an overflowed `int` result to a `long` does not recover the correct mathematical result.

### Hints for selected advanced questions

<details>
<summary>Question 5 — Convert seconds</summary>

- **Tip 1:** One hour contains 3600 seconds; one minute contains 60 seconds.
- **Tip 2:** Use integer division to calculate whole hours.
- **Tip 3:** Use `%` to find the remaining seconds and minutes.
</details>

<details>
<summary>Question 7 — Sum of digits</summary>

- **Tip 1:** The last digit is `number % 10`.
- **Tip 2:** Remove the last digit using `number / 10`.
- **Tip 3:** Repeat the process for the remaining digits. Decide how you will handle negative input.
</details>

<details>
<summary>Question 11 — Discount and tax</summary>

- **Tip 1:** Calculate the discount first.
- **Tip 2:** Subtract the discount from the original amount.
- **Tip 3:** Apply tax to the amount specified by the question; tax rules differ depending on whether tax is applied before or after the discount.
</details>

---

# Level 4 — Mixed Practice

**Rules**
- Solve each question in a separate Java program.
- Use `Scanner` for user input where needed.
- Do not open the hints until you have tried.
- Show the working steps in comments or on paper.
- Test normal values and boundary values.

## Mixed questions

### M1. Student result

Take a student's name and marks in five subjects. Display the name, total, percentage and Pass/Fail status. Assume a student must score at least 40 in every subject to pass.

<details>
<summary>Hints</summary>

- **Tip 1:** Use a `String` for the name and numeric variables for marks.
- **Tip 2:** Add the marks and calculate the percentage.
- **Tip 3:** The student passes only if every subject mark is at least 40.
</details>

### M2. Shopping bill

Take the price and quantity of an item. Calculate the total. If the total is at least 2,000, apply a 5% discount. Display the original total, discount and final bill.

<details>
<summary>Hints</summary>

- **Tip 1:** Calculate `price * quantity`.
- **Tip 2:** Use an `if` condition to decide whether the discount applies.
- **Tip 3:** Subtract the discount from the original total.
</details>

### M3. Time converter

Take a total number of seconds and display the equivalent hours, minutes and seconds.

<details>
<summary>Hints</summary>

- **Tip 1:** Divide by 3600 to find whole hours.
- **Tip 2:** Use the remainder after hours have been removed.
- **Tip 3:** Divide the remaining seconds by 60, then use `% 60` for the leftover seconds.
</details>

### M4. Digit analyser

Take a three-digit positive integer and display the sum of its digits and the reversed number.

<details>
<summary>Hints</summary>

- **Tip 1:** Use `% 10` to extract the last digit.
- **Tip 2:** Use `/ 10` to remove the last digit.
- **Tip 3:** Build the reversed number by multiplying the current result by 10 and adding the next digit.
</details>

### M5. Eligibility checker

Take a person's age and whether they have permission (true/false). Display `Eligible` if they are at least 18 or have permission.

<details>
<summary>Hints</summary>

- **Tip 1:** Store the age in an `int`.
- **Tip 2:** Store permission in a `boolean`.
- **Tip 3:** Combine the conditions using `||`.
</details>

### M6. Expression challenge

Predict and then verify the output:

```java
int a = 5;
int b = 2;

int first = a++ + 3;
int second = ++b + a;
double third = (double) a / b;

System.out.println(first);
System.out.println(second);
System.out.println(third);
```

<details>
<summary>Hints</summary>

- **Tip 1:** Write down `a` and `b` before each statement.
- **Tip 2:** In `a++`, the old value is used before incrementing.
- **Tip 3:** In `++b`, incrementing happens before the value is used.
</details>

### M7. Number breakdown

Take a non-negative integer and display the number of hundreds, tens and units in it. For example, `583` should display 5 hundreds, 8 tens and 3 units.

<details>
<summary>Hints</summary>

- **Tip 1:** Use division to remove the smaller place values.
- **Tip 2:** Use `% 10` to extract the final digit.
- **Tip 3:** Decide whether the question means place-value digits or the number of complete hundreds/tens in the whole number.
</details>

### M8. Character classifier

Take one character and check whether it is an uppercase letter, lowercase letter, digit or special character.

<details>
<summary>Hints</summary>

- **Tip 1:** Store the input as a `String`, then use `charAt(0)` for the first character.
- **Tip 2:** Use `Character.isUpperCase`, `Character.isLowerCase` and `Character.isDigit`.
- **Tip 3:** Use `else` for the remaining characters.
</details>

### M9. Salary calculation

Take a basic salary. Calculate a house allowance of 20% and a travel allowance of 10%. Display both allowances and the total salary.

<details>
<summary>Hints</summary>

- **Tip 1:** Store the basic salary in a numeric variable.
- **Tip 2:** Calculate each allowance separately.
- **Tip 3:** Add the basic salary and both allowances.
</details>

### M10. Swap and compare

Take two integers, display their values, swap them using a temporary variable, and then display which value is greater after swapping.

<details>
<summary>Hints</summary>

- **Tip 1:** Save the first value in `temp`.
- **Tip 2:** Copy the second value to the first, then `temp` to the second.
- **Tip 3:** Use `if-else` to compare the swapped values.
</details>

---

# Common Mistakes

1. **Using `=` instead of `==`:** `=` assigns a value; `==` compares primitive values.
2. **Using the wrong data type:** A decimal value such as `12.5` cannot be assigned directly to an `int`.
3. **Forgetting `f` for a float literal:** Write `float rate = 2.5f;`.
4. **Using single quotes for a String:** Write `"Hello"`, not `'Hello'`.
5. **Integer division surprises:** `5 / 2` produces `2`, not `2.5`.
6. **Reading a local variable before assigning it:** Assign a value before using the variable.
7. **Confusing `next()` and `nextLine()`:** `next()` reads one token; `nextLine()` reads a line.
8. **Ignoring operator precedence:** Use parentheses to make calculations clear.
9. **Overusing short variable names:** Names such as `totalMarks` make code easier to understand.
10. **Expecting `final` to mean the value can never be set:** A `final` local variable can be initialized once, but it cannot be reassigned afterwards.
11. **Assuming `long` fixes an earlier overflow:** The arithmetic operation itself must use a suitable type.
12. **Putting too much logic in one expression:** Break the calculation into smaller steps and print intermediate values while debugging.

---

# Answer Key

Use this section only after trying the questions. These examples show common approaches; write your own version and test it.

## Basic examples

### B1. Add two user-entered integers

```java
import java.util.Scanner;

class AddNumbers {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int a = sc.nextInt();

        System.out.print("Enter second number: ");
        int b = sc.nextInt();

        int sum = a + b;
        System.out.println("Sum = " + sum);

        sc.close();
    }
}
```

### B2. Rectangle area

```java
double length = 12.5;
double breadth = 4.0;
double area = length * breadth;

System.out.println(area); // 50.0
```

### B3. Swap two values

```java
int a = 10;
int b = 20;

int temp = a;
a = b;
b = temp;

System.out.println(a); // 20
System.out.println(b); // 10
```

### B4. Average with decimal values

```java
int a = 7;
int b = 2;

double average = (a + b) / 2.0;
System.out.println(average); // 4.5
```

## Intermediate examples

### I1. Largest of three numbers

```java
int a = 12;
int b = 25;
int c = 18;

int largest = a;

if (b > largest) {
    largest = b;
}

if (c > largest) {
    largest = c;
}

System.out.println(largest); // 25
```

### I2. Divisible by both 3 and 5

```java
int number = 30;

if (number % 3 == 0 && number % 5 == 0) {
    System.out.println("Divisible by both");
} else {
    System.out.println("Not divisible by both");
}
```

### I3. Leap year

```java
int year = 2024;

if (year % 400 == 0 || (year % 4 == 0 && year % 100 != 0)) {
    System.out.println("Leap year");
} else {
    System.out.println("Not a leap year");
}
```

## Advanced examples

### A1. Convert seconds to hours, minutes and seconds

```java
int totalSeconds = 3672;

int hours = totalSeconds / 3600;
int remainingSeconds = totalSeconds % 3600;
int minutes = remainingSeconds / 60;
int seconds = remainingSeconds % 60;

System.out.println(hours + " hours");
System.out.println(minutes + " minutes");
System.out.println(seconds + " seconds");
```

### A2. Sum the digits of a three-digit number

```java
int number = 583;

int hundreds = number / 100;
int tens = (number / 10) % 10;
int units = number % 10;

int sum = hundreds + tens + units;

System.out.println(sum); // 16
```

### A3. Character classification

```java
char ch = 'G';

if (Character.isUpperCase(ch)) {
    System.out.println("Uppercase letter");
} else if (Character.isLowerCase(ch)) {
    System.out.println("Lowercase letter");
} else if (Character.isDigit(ch)) {
    System.out.println("Digit");
} else {
    System.out.println("Other character");
}
```

## Mixed example: Shopping bill

```java
double price = 750.0;
int quantity = 3;

double total = price * quantity;
double discount = 0;

if (total >= 2000) {
    discount = total * 0.05;
}

double finalBill = total - discount;

System.out.println("Total: " + total);
System.out.println("Discount: " + discount);
System.out.println("Final bill: " + finalBill);
```

---

## Final checklist

- [ ] I can declare and initialize variables.
- [ ] I know when to use `int`, `double`, `char`, `boolean` and `String`.
- [ ] I can take input with `Scanner`.
- [ ] I can use arithmetic, comparison and logical operators.
- [ ] I understand integer division and type casting.
- [ ] I can use `if-else` and the ternary operator.
- [ ] I understand scope and `final` variables.
- [ ] I can trace prefix and postfix increment.
- [ ] I can explain my solution before writing code.
- [ ] I have solved mixed questions without opening the hints first.

**Remember:** Learn what each variable stores, how its value changes, and why the program produces its output.

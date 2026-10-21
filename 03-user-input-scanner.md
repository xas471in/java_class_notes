# User Input in Java — Class 10

## Goal
Take input from the keyboard using `Scanner`, store it in variables and use it in calculations.

## 1. Import and create a Scanner

```java
import java.util.Scanner;

class InputExample {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your age: ");
        int age = sc.nextInt();

        System.out.println("Your age is " + age);
        sc.close();
    }
}
```

- `import java.util.Scanner;` makes the Scanner class available.
- `new Scanner(System.in)` reads from keyboard input.
- `sc.nextInt()` reads an integer.
- `sc.close()` closes the Scanner after it is no longer needed.

## 2. Common Scanner methods

| Method | Reads |
|---|---|
| `nextInt()` | Integer |
| `nextLong()` | Long integer |
| `nextFloat()` | Float |
| `nextDouble()` | Double |
| `nextBoolean()` | `true` or `false` |
| `next()` | One word/token |
| `nextLine()` | A full line of text |

## 3. Taking multiple inputs

```java
Scanner sc = new Scanner(System.in);

System.out.print("Enter first number: ");
int a = sc.nextInt();

System.out.print("Enter second number: ");
int b = sc.nextInt();

System.out.println("Sum = " + (a + b));
sc.close();
```

Parentheses around `a + b` make it clear that addition should happen before joining the result to the text.

## 4. Reading a full sentence

```java
Scanner sc = new Scanner(System.in);

System.out.print("Enter your full name: ");
String name = sc.nextLine();

System.out.println("Hello, " + name);
sc.close();
```

`next()` reads only one token, while `nextLine()` reads the entire line, including spaces.

## 5. `nextLine()` after a number

`nextInt()` reads the number but leaves the line break behind. Consume that line break before reading a full line.

```java
Scanner sc = new Scanner(System.in);

System.out.print("Enter age: ");
int age = sc.nextInt();
sc.nextLine(); // Consume the remaining line break

System.out.print("Enter name: ");
String name = sc.nextLine();

System.out.println(name + " is " + age);
sc.close();
```

## Practice questions

1. Take the user's name and display a greeting.
2. Take two integers and display their sum.
3. Take three numbers and display their average.
4. Take the user's full name and age, then display both.
5. Take the price and quantity of an item and calculate the bill.
6. Take a character from the user using `next()` and `charAt(0)`.
7. Take marks in five subjects and calculate the total.
8. Take a sentence and display it inside quotation marks.
9. Take two decimal numbers and display their product.
10. Take age as input and display the age the user will be next year.

<details>
<summary>Hints</summary>

- **Tip 1:** Create one Scanner object and reuse it.
- **Tip 2:** Select the input method that matches the data type.
- **Tip 3:** Use `nextLine()` for a complete sentence and remember the leftover line break issue.
</details>

## Common mistakes

- Forgetting the Scanner import.
- Using `nextInt()` to read a sentence.
- Forgetting to consume the line break before a later `nextLine()`.
- Trying to store a decimal in an `int` without an intentional conversion.
- Forgetting that `+` can add numbers or join text, depending on the expression.

## Checklist

- [ ] I can read integers and decimals.
- [ ] I can read a full sentence.
- [ ] I understand `next()` vs `nextLine()`.
- [ ] I can use input values in calculations.

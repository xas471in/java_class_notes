# Chapter 3 — Input and Output

> **Goal:** Read information from the keyboard and display results.

## Use `Scanner`

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

## Useful methods

| Method | Reads |
|---|---|
| `nextInt()` | Integer |
| `nextLong()` | Long integer |
| `nextFloat()` | Float |
| `nextDouble()` | Double |
| `nextBoolean()` | Boolean |
| `next()` | One word |
| `nextLine()` | Full line of text |

## Read a full sentence

```java
System.out.print("Enter your full name: ");
String name = sc.nextLine();
```

After `nextInt()`, a line break may remain in the input. Consume it before reading a full line:

```java
int age = sc.nextInt();
sc.nextLine();
String name = sc.nextLine();
```

## Practice

1. Ask for a name and display a greeting.
2. Ask for two integers and display their sum.
3. Ask for a full name and age, then display both.
4. Ask for price and quantity and calculate a bill.
5. Ask for marks in five subjects and display them.
6. Read two decimal numbers and display their product.
7. Read a sentence and display it inside quotation marks.
8. Read a character using `next()` and `charAt(0)`.
9. Read a number and display its double.
10. Read a number followed by a full name without skipping the name.

<details><summary>Hints</summary>

- **Tip 1:** Match the Scanner method to the data type.
- **Tip 2:** Use `nextLine()` for sentences.
- **Tip 3:** Consume the leftover line break after numeric input when needed.
</details>

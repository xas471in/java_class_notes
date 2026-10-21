# Chapter 3: Let the User Enter Information

> **Today’s goal:** Make programs interactive by asking the user to type something.

---

## 1. Why do we need input?

A program that always uses the same numbers is not very flexible.

Instead, we can ask the user to enter values.

```text
Program: Enter your age:
                 │
                 ▼
User types:      15
                 │
                 ▼
Program: Your age is 15
```

In Java, one beginner-friendly way to read input is with `Scanner`.

---

## 2. Set up `Scanner`

```java
import java.util.Scanner;

class InputExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your age: ");
        int age = sc.nextInt();

        System.out.println("Your age is " + age);

        sc.close();
    }
}
```

**Sample run**

```text
Enter your age: 15
Your age is 15
```

What happens?

1. `Scanner sc = new Scanner(System.in);` prepares Java to read keyboard input.
2. `nextInt()` reads a whole number.
3. The value is stored in `age`.
4. The program displays the value.

---

## 3. Which input method should I use?

| Method | Example input | What it reads |
|---|---|---|
| `nextInt()` | `15` | Whole number |
| `nextDouble()` | `25.5` | Decimal number |
| `next()` | `Riya` | One word |
| `nextLine()` | `Riya Das` | A complete line |

Example:

```java
System.out.print("Enter your name: ");
String name = sc.nextLine();

System.out.print("Enter your marks: ");
int marks = sc.nextInt();

System.out.println(name + " scored " + marks);
```

---

## 4. Why can `nextLine()` sometimes skip?

After a numeric input such as `nextInt()`, the Enter key's line break may still be waiting. If you want to read a full line after it, consume that line break first.

```java
int age = sc.nextInt();
sc.nextLine(); // Consume the leftover line break

System.out.print("Enter your full name: ");
String name = sc.nextLine();
```

You do not need to memorise this immediately. Just remember it when a full line appears to be skipped.

---

## Practice time

1. Ask the user for their name and display a greeting.
2. Ask for two whole numbers and display their sum.
3. Ask for a full name and age, then display both.
4. Ask for the price and quantity of an item.
5. Ask for marks in three subjects and display them.
6. Ask for two decimal numbers and display their product.
7. Ask for a sentence and display it.
8. Ask for a number and display twice its value.
9. Read a number and then a full name; make sure the name is not skipped.

<details>
<summary>Need a hint? Open this</summary>

- **Tip 1:** Create the `Scanner` before reading input.
- **Tip 2:** Match the method to the kind of value.
- **Tip 3:** Use `nextLine()` when the input can contain spaces.
</details>

---

## Quick recap

Input lets the user provide values while the program is running. `Scanner` reads the values, and variables store them.

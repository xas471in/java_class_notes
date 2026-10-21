# Chapter 1: Your First Java Program

> **Today’s goal:** Understand what a Java program looks like and make the computer display a message.

---

## 1. What is a program?

A program is a set of instructions that tells a computer what to do.

For example, we can tell a computer to display a greeting, add two numbers, or calculate a bill.

Think of a program like a recipe: the computer follows the instructions in order.

```text
Our instructions  ──────►  Computer  ──────►  Result
"Display Hello"             runs code             Hello
```

---

## 2. Your first Java program

```java
class Hello {
    public static void main(String[] args) {
        System.out.println("Hello!");
    }
}
```

**Output**

```text
Hello!
```

Do not worry if the first line looks confusing. We will learn what each part means.

- `class Hello` gives our program a class name.
- The curly brackets `{ }` show where a block of code begins and ends.
- `main()` is where this simple Java program starts running.
- `System.out.println()` displays something on the screen.
- `"Hello!"` is the text we want to display.
- `;` marks the end of the instruction.

For now, learn the shape of the program. We will understand the pieces one by one.

---

## 3. Displaying text

```java
System.out.println("I am learning Java.");
System.out.println("This is my second line.");
```

Output:

```text
I am learning Java.
This is my second line.
```

Text must be placed inside double quotation marks: `"like this"`.

### `print()` vs `println()`

```java
System.out.print("Good ");
System.out.print("morning");
System.out.println();
System.out.println("Everyone!");
```

Output:

```text
Good morning
Everyone!
```

- `print()` continues on the same line.
- `println()` moves to the next line after displaying the value.

---

## 4. Comments: notes inside code

```java
// This is a single-line comment.

/*
   This is a multi-line comment.
   Java ignores these comments when running the program.
*/
```

Comments help us explain our code to people reading it.

---

## 5. Follow the instruction order

```java
System.out.println("First");
System.out.println("Second");
System.out.println("Third");
```

The computer follows these instructions from top to bottom.

---

## Practice time

Try these without copying the example exactly.

1. Display your name.
2. Display your name, favourite subject and hobby on separate lines.
3. Use `print()` to display `Java is fun!` on one line.
4. Display this shape:

```text
*****
*   *
*****
```

5. Write a small shop heading and display three item names.
6. Predict the output of this code before running it:

```java
System.out.print("A");
System.out.println("B");
System.out.print("C");
```

<details>
<summary>Need a hint? Open this</summary>

- **Tip 1:** Check where each statement starts and ends.
- **Tip 2:** Text goes inside double quotes.
- **Tip 3:** Remember that `print()` and `println()` behave differently.
</details>

---

## Quick recap

- A program is a set of instructions.
- Java statements usually end with `;`.
- Use double quotes for text.
- Use `print()` to stay on the same line and `println()` to move to the next line.

# Java Program Structure — Class 10

## Goal
Understand the basic structure of a Java program, the `main()` method, statements, blocks and output.

## 1. A first Java program

```java
class HelloWorld {
    public static void main(String args[]) {
        System.out.println("Hello, World!");
    }
}
```

Output:
```text
Hello, World!
```

## 2. Understanding the parts

- `class HelloWorld`: declares a class named `HelloWorld`.
- `{ }`: braces mark the beginning and end of a block.
- `public static void main(String args[])`: the main method where a simple Java application starts.
- `System.out.println()`: displays output and moves to the next line.
- `;`: ends most Java statements.
- `"Hello, World!"`: a String literal.

For now, learn the main method as a standard starting template. The words `public`, `static` and `void` have specific meanings that can be studied more deeply later.

## 3. `print()` vs `println()`

```java
System.out.print("Java ");
System.out.print("Class 10");
System.out.println();
System.out.println("Next line");
```

Output:
```text
Java Class 10
Next line
```

`print()` keeps output on the same line. `println()` moves to the next line after printing.

## 4. Comments

```java
// This is a single-line comment.

/*
 This is a multi-line comment.
 It is ignored by the compiler.
*/
```

Comments explain code and are not executed.

## 5. Case sensitivity and syntax

Java is case-sensitive: `main`, `Main`, and `MAIN` are different identifiers.

```java
System.out.println("Hi"); // Correct
// system.out.println("Hi"); // Incorrect: system has the wrong case
```

## 6. Compile-time errors vs output mistakes

- Missing semicolon: usually a compile-time error.
- Misspelled `println`: compile-time error.
- Correct program displaying an unexpected value: likely a logic error.

## Practice questions

1. Print your name, school and class on separate lines.
2. Display a three-line poem using `println()`.
3. Display three words on one line using `print()`.
4. Add comments to explain each line of a simple program.
5. Find and correct the errors in a program with a missing semicolon and incorrect capitalization.
6. Predict the output of a program mixing `print()` and `println()`.
7. Write a program that displays a simple bill with item, quantity and price on separate lines.

<details>
<summary>Hints</summary>

- **Tip 1:** Every statement that prints output uses `System.out.print` or `System.out.println`.
- **Tip 2:** Check capitalization and quotation marks.
- **Tip 3:** Trace the output one statement at a time.
</details>

## Common mistakes

1. Forgetting semicolons.
2. Mismatching opening and closing braces.
3. Using single quotes for a String.
4. Writing `system` instead of `System`.
5. Forgetting that the class name and file name must match when the class is declared `public`.

## Checklist

- [ ] I can write the basic Java program structure.
- [ ] I know the purpose of `main()`.
- [ ] I can use `print()` and `println()`.
- [ ] I can write comments and identify simple syntax errors.

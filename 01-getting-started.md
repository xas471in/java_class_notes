# Chapter 1 — Getting Started with Java

> **Goal:** Write a program, understand its structure, and display output.

## Your first program

```java
class Hello {
    public static void main(String args[]) {
        System.out.println("Hello, Java!");
    }
}
```

Output: `Hello, Java!`

- `class Hello` declares a class.
- `main()` is where a basic Java application starts.
- `{ }` mark blocks.
- `System.out.println()` displays output and moves to the next line.
- `;` ends most statements.
- Java is case-sensitive.

## `print()` and `println()`

```java
System.out.print("Good ");
System.out.print("morning");
System.out.println();
System.out.println("Java");
```

`print()` stays on the same line. `println()` moves to the next line.

## Comments

```java
// Single-line comment

/*
 Multi-line comment
*/
```

## Practice

1. Display your name, school and favourite subject on separate lines.
2. Print three words on the same line.
3. Display a simple three-line pattern.
4. Create a small bill heading with three item names.
5. Predict the output of code mixing `print()` and `println()`.
6. Find and correct missing semicolons, incorrect capitalization and mismatched braces.

<details><summary>Hints</summary>

- **Tip 1:** Check statement endings.
- **Tip 2:** Check capitalization, quotes and braces.
- **Tip 3:** Trace output one statement at a time.
</details>

## Common mistakes

- Missing semicolons or braces.
- Writing `system` instead of `System`.
- Using single quotes for a full String.

# Chapter 11 — Strings and Characters

> **Goal:** Inspect text, use String methods and solve simple text problems.

## String and char

```java
String word = "Java";
char grade = 'A';
```

## Common String methods

| Method | Purpose |
|---|---|
| `length()` | Number of UTF-16 code units |
| `charAt(i)` | Character at index `i` |
| `toUpperCase()` | Uppercase version |
| `toLowerCase()` | Lowercase version |
| `equals(s)` | Compare contents |
| `equalsIgnoreCase(s)` | Compare without case |
| `contains(s)` | Check whether text contains a sequence |
| `indexOf(ch)` | First matching index or -1 |
| `substring(a, b)` | From `a` up to but not including `b` |
| `trim()` | Remove basic leading/trailing spaces |
| `replace(a, b)` | Replace matching text |
| `split(regex)` | Split into parts |

Use `.equals()` to compare String contents; `==` compares object references.

## Count vowels

```java
String text = "Education";
int count = 0;

for (int i = 0; i < text.length(); i++) {
    char ch = Character.toLowerCase(text.charAt(i));
    if (ch == 'a' || ch == 'e' || ch == 'i' ||
        ch == 'o' || ch == 'u') {
        count++;
    }
}
System.out.println(count);
```

## Count alphabetic characters

```java
String text = "Hello World 123!";
int count = 0;

for (int i = 0; i < text.length(); i++) {
    if (Character.isLetter(text.charAt(i))) {
        count++;
    }
}
System.out.println(count); // 10
```

## Find the longest word

```java
String sentence = "Java is a powerful language";
String[] words = sentence.trim().split("\\s+");
String longest = "";

for (int i = 0; i < words.length; i++) {
    if (words[i].length() > longest.length()) {
        longest = words[i];
    }
}
System.out.println(longest); // powerful
```

Assumes a non-empty sentence; if there is a tie, this keeps the first longest word.

## Practice

1. Display the length of a sentence.
2. Display the first and last character of a non-empty String.
3. Convert text to uppercase and lowercase.
4. Compare two Strings ignoring case.
5. Count vowels and consonants.
6. Count letters, digits and spaces.
7. Count words.
8. Display the longest and shortest words.
9. Reverse a String using a loop.
10. Check whether a word is a palindrome, ignoring case.
11. Count occurrences of a chosen character.
12. Replace spaces with hyphens.
13. Count uppercase and lowercase letters.
14. Display each character with its index.

<details><summary>Hints</summary>

- **Tip 1:** Use `length()` and `charAt(i)`.
- **Tip 2:** Use methods from `Character` to classify characters.
- **Tip 3:** Split on whitespace to separate words; punctuation needs separate handling if required.
</details>

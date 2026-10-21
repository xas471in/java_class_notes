# Chapter 11: Strings — Working with Text

> **Today’s goal:** Store text and inspect it one character at a time.

---

## 1. What is a String?

A `String` stores text.

```java
String name = "Riya";
String sentence = "Java is fun to learn.";
```

Text uses double quotation marks.

A `char` stores one character:

```java
char grade = 'A';
```

---

## 2. Count characters with `length()`

```java
String word = "Java";
System.out.println(word.length()); // 4
```

Strings use `length()` with brackets. Arrays use `length` without brackets.

---

## 3. Get one character with `charAt()`

```java
String word = "Java";

System.out.println(word.charAt(0)); // J
System.out.println(word.charAt(1)); // a
```

String indexes also start at 0.

```text
Character:  J   a   v   a
Index:      0   1   2   3
```

---

## 4. Useful String methods

| Method | What it does |
|---|---|
| `length()` | Counts the characters/code units |
| `charAt(i)` | Gets the character at index `i` |
| `toUpperCase()` | Converts to uppercase |
| `toLowerCase()` | Converts to lowercase |
| `equals(text)` | Compares text contents |
| `equalsIgnoreCase(text)` | Compares contents ignoring case |
| `contains(text)` | Checks whether text is present |
| `indexOf(text)` | Finds the first matching position |
| `substring(a, b)` | Gets part of a String from `a` up to `b` |
| `replace(a, b)` | Replaces matching characters/text |
| `trim()` | Removes basic spaces at the beginning and end |

Strings do not change in place. Methods such as `toUpperCase()` return a new String.

---

## 5. Visit each character

```java
String word = "Java";

for (int i = 0; i < word.length(); i++) {
    System.out.println(word.charAt(i));
}
```

Output:

```text
J
a
v
a
```

---

## 6. Count vowels

```java
String word = "Education";
int count = 0;

for (int i = 0; i < word.length(); i++) {
    char ch = Character.toLowerCase(word.charAt(i));

    if (ch == 'a' || ch == 'e' || ch == 'i' ||
        ch == 'o' || ch == 'u') {
        count++;
    }
}

System.out.println(count);
```

---

## 7. Count alphabetic characters, not spaces

```java
String sentence = "Hello World 123!";
int count = 0;

for (int i = 0; i < sentence.length(); i++) {
    if (Character.isLetter(sentence.charAt(i))) {
        count++;
    }
}

System.out.println(count); // 10
```

`Character.isLetter()` checks whether the character is a letter. Spaces, digits and punctuation are not counted.

---

## 8. Find the longest word

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

This example assumes the sentence is not empty. If two words have the same longest length, it keeps the first one.

---

## Practice time

1. Display the length of a word.
2. Display the first and last character of a non-empty String.
3. Convert a sentence to uppercase and lowercase.
4. Compare two words without caring about uppercase/lowercase.
5. Count vowels in a sentence.
6. Count letters without counting spaces.
7. Count digits and spaces in a sentence.
8. Count the words in a sentence.
9. Find the longest word.
10. Reverse a String using a loop.
11. Check whether a word is a palindrome, ignoring case.
12. Count how many times a chosen character appears.
13. Replace spaces with hyphens.
14. Count uppercase and lowercase letters separately.

<details>
<summary>Need a hint? Open this</summary>

- **Tip 1:** Use `length()` and `charAt(i)` to inspect each character.
- **Tip 2:** Use `Character.isLetter()` and `Character.isDigit()` to classify characters.
- **Tip 3:** Split a sentence on whitespace to get its words.
</details>

---

## Quick recap

Strings store text. Use String methods to inspect, compare and transform text. When a task asks you to inspect every character, a loop is often useful.

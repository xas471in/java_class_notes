# Strings and Character Manipulation — Class 10 Java

## Goal
Use `String` methods and character checks to inspect text, count letters and words, and solve basic text problems.

## 1. What is a String?

A `String` stores text.

```java
String name = "Java";
System.out.println(name);
```

Strings use double quotes. A `char` stores one UTF-16 code unit and uses single quotes.

```java
char grade = 'A';
String word = "Array";
```

## 2. Common String methods

| Method | Purpose | Example |
|---|---|---|
| `length()` | Number of UTF-16 code units | `"Java".length()` → `4` |
| `charAt(i)` | Character at index `i` | `"Java".charAt(0)` → `'J'` |
| `toUpperCase()` | Uppercase version | `"java".toUpperCase()` → `"JAVA"` |
| `toLowerCase()` | Lowercase version | `"JAVA".toLowerCase()` → `"java"` |
| `equals(s)` | Compare text exactly | `"Hi".equals("Hi")` → `true` |
| `equalsIgnoreCase(s)` | Compare ignoring case | `"Java".equalsIgnoreCase("JAVA")` → `true` |
| `contains(s)` | Check for a sequence | `"Hello".contains("ell")` → `true` |
| `indexOf(ch)` | First matching index, or -1 | `"banana".indexOf('a')` → `1` |
| `substring(a, b)` | Text from index `a` to before `b` | `"Java".substring(1, 3)` → `"av"` |
| `trim()` | Remove leading/trailing basic spaces | `" hi ".trim()` → `"hi"` |
| `replace(a, b)` | Replace matching characters/sequences | `"banana".replace('a','o')` → `"bonono"` |
| `split(regex)` | Split into parts | `"a b".split("\\s+")` |

String indexes start at 0. The end index in `substring(start, end)` is excluded.

## 3. Comparing Strings

Use `.equals()` to compare String contents, not `==`.

```java
String a = "Java";
String b = new String("Java");

System.out.println(a.equals(b)); // true
System.out.println(a == b);      // false in this example
```

`==` checks whether references point to the same object; `.equals()` checks text content.

## 4. Visit every character

```java
String text = "Java Class";

for (int i = 0; i < text.length(); i++) {
    System.out.println(text.charAt(i));
}
```

The loop visits each character by index.

## 5. Count vowels

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

Converting to lowercase makes the check handle uppercase vowels too.

## 6. Count alphabetic characters only

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

`Character.isLetter()` ignores spaces, digits and punctuation.

## 7. Find the longest word

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

This example assumes the sentence is not empty. If two words have the same maximum length, it keeps the first one.

## Practice questions

1. Take a sentence and display its length.
2. Display the first and last character of a non-empty String.
3. Convert a sentence to uppercase and lowercase.
4. Check whether two Strings are equal, ignoring case.
5. Count vowels in a sentence.
6. Count consonant letters in a sentence.
7. Count alphabetic characters, ignoring spaces, digits and punctuation.
8. Count digits in a sentence.
9. Count spaces in a sentence.
10. Count words in a sentence.
11. Display the longest word.
12. Display the shortest word.
13. Reverse a String using a loop.
14. Check whether a word is a palindrome, ignoring case.
15. Count how many times a given character appears.
16. Replace every space with a hyphen.
17. Remove leading and trailing spaces.
18. Count uppercase and lowercase letters separately.
19. Display every character with its index.
20. Check whether a sentence contains a particular word or sequence.

<details>
<summary>Hints</summary>

- **Tip 1:** Use `length()` to control a character loop.
- **Tip 2:** Use `charAt(i)` to access each character.
- **Tip 3:** Use `Character.isLetter`, `isDigit`, `isUpperCase` and `isLowerCase` for character classification.
</details>

## Common mistakes

- Writing `length` instead of `length()` for a String. Arrays use `.length`; Strings use `.length()`.
- Using `==` to compare String contents.
- Calling `charAt(0)` on an empty String.
- Forgetting that indexes start at 0.
- Assuming `split("\\s+")` handles every punctuation rule; it splits on whitespace, not punctuation.
- Forgetting that Java Strings are immutable: methods return a new String rather than changing the original.

## Checklist

- [ ] I can use common String methods.
- [ ] I can loop through characters.
- [ ] I can count vowels and alphabetic characters.
- [ ] I can find longest and shortest words.

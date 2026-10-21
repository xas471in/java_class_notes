# Chapter 15: Mixed Practice and Mini Projects

> **Goal:** Combine topics from earlier chapters. Try each task yourself before opening its hints.

---

## A simple plan for solving a problem

```text
Understand the question
          ↓
Identify input and output
          ↓
Write the steps in plain language
          ↓
Choose variables and tools
          ↓
Write the code
          ↓
Test with a few examples
```

Do not rush straight into typing code. A clear plan makes programming easier.

---

## Challenge 1: Student marks report

Read marks for five subjects. Display the total, average, highest mark, lowest mark and Pass/Fail. A student passes only if every subject mark is at least 40.

<details>
<summary>Hints</summary>

- **Tip 1:** Store marks in an array.
- **Tip 2:** Use a loop to calculate the total, highest, lowest and pass status.
- **Tip 3:** Calculate the average after the loop.
</details>

---

## Challenge 2: Shopping bill

Read an item's price and quantity. Apply a 5% discount if the total is at least 2,000. Display the original total, discount and final amount.

<details>
<summary>Hints</summary>

- **Tip 1:** Multiply price by quantity.
- **Tip 2:** Use an `if` condition to decide whether the discount applies.
- **Tip 3:** Subtract the discount from the original total.
</details>

---

## Challenge 3: Number analyser

Read a positive integer and display its digit count, digit sum, reverse and palindrome status.

<details>
<summary>Hints</summary>

- **Tip 1:** Save the original number.
- **Tip 2:** Use `% 10` to get the last digit and `/ 10` to remove it.
- **Tip 3:** Keep separate variables for count, sum and reversed number.
</details>

---

## Challenge 4: Sentence analyser

Read a sentence and display the word count, alphabetic character count, vowel count and longest word.

<details>
<summary>Hints</summary>

- **Tip 1:** Use `charAt(i)` to inspect each character.
- **Tip 2:** Use `Character.isLetter()` and check for vowels.
- **Tip 3:** Split the sentence on whitespace to inspect words.
</details>

---

## Challenge 5: Menu calculator

Build a menu for addition, subtraction, multiplication, division and exit. Keep showing the menu until the user chooses exit.

<details>
<summary>Hints</summary>

- **Tip 1:** Put the menu inside a loop.
- **Tip 2:** Use `switch` to process the chosen option.
- **Tip 3:** Check division by zero and stop when the exit option is selected.
</details>

---

## Challenge 6: Student object

Create a `Student` class with name and marks. Use a constructor to initialize the fields and a method to return whether the student passed.

<details>
<summary>Hints</summary>

- **Tip 1:** Store name and marks as fields.
- **Tip 2:** Initialize them with a parameterized constructor.
- **Tip 3:** Return a boolean from the pass-checking method.
</details>

---

## Challenge 7: Array frequency report

Read several integers and display each distinct value with its frequency.

<details>
<summary>Hints</summary>

- **Tip 1:** Visit each array value.
- **Tip 2:** Check whether that value was already processed at an earlier index.
- **Tip 3:** Use another loop to count occurrences.
</details>

---

## Challenge 8: Pattern generator

Ask for a row count and let the user choose a triangle, inverted triangle or rectangle.

<details>
<summary>Hints</summary>

- **Tip 1:** Use `switch` for the pattern choice.
- **Tip 2:** Use nested loops for rows and columns.
- **Tip 3:** Print a newline after each row.
</details>

---

## Final checklist

- [ ] I can write a basic Java program.
- [ ] I understand variables and data types.
- [ ] I can read user input.
- [ ] I can perform calculations.
- [ ] I can use conditions and `switch`.
- [ ] I can use loops and nested loops.
- [ ] I can solve number and String problems.
- [ ] I can use arrays and methods.
- [ ] I understand classes, objects and constructors.
- [ ] I can explain my approach before writing code.

**The goal is not to memorise every answer. The goal is to understand the steps and solve a new problem independently.**

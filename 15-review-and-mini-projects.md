# Chapter 15 — Review and Mini Projects

> **Goal:** Combine concepts and practise solving problems independently.

## A good problem-solving routine

1. Read the question carefully.
2. Identify the input and expected output.
3. Write the steps in plain language.
4. Choose variables and data types.
5. Decide whether conditions, loops, arrays, Strings, methods or objects are needed.
6. Test normal and boundary values.

## Review challenges

### 1. Student marks report
Read marks for five subjects. Display total, average, highest, lowest and Pass/Fail. The student passes only if every subject mark is at least 40.

<details><summary>Hints</summary>

- **Tip 1:** Store the marks in an array.
- **Tip 2:** Use a loop to calculate total, maximum, minimum and pass status.
- **Tip 3:** Calculate the average after the loop.
</details>

### 2. Shopping bill
Read item price and quantity. Apply a 5% discount if the total is at least 2,000.

<details><summary>Hints</summary>

- **Tip 1:** Multiply price by quantity.
- **Tip 2:** Use an `if` condition for the discount.
- **Tip 3:** Subtract the discount from the original total.
</details>

### 3. Number analyser
Read a positive integer and display its digit count, digit sum, reverse and palindrome status.

<details><summary>Hints</summary>

- **Tip 1:** Save the original number.
- **Tip 2:** Use `% 10` and `/ 10`.
- **Tip 3:** Keep separate variables for count, sum and reversed number.
</details>

### 4. Sentence analyser
Read a sentence and display word count, alphabetic character count, vowel count and longest word.

<details><summary>Hints</summary>

- **Tip 1:** Use `charAt(i)` to inspect characters.
- **Tip 2:** Use `Character.isLetter()` and check vowels.
- **Tip 3:** Split on whitespace to inspect words.
</details>

### 5. Menu calculator
Build a menu for addition, subtraction, multiplication, division and exit. Keep displaying the menu until the user chooses exit.

<details><summary>Hints</summary>

- **Tip 1:** Put the menu inside a loop.
- **Tip 2:** Use `switch` to process the choice.
- **Tip 3:** Check division by zero and stop on the exit option.
</details>

### 6. Student object
Create a `Student` class with name and marks. Initialize them using a constructor and add a method that returns whether the student passed.

<details><summary>Hints</summary>

- **Tip 1:** Store name and marks as instance fields.
- **Tip 2:** Use a parameterized constructor.
- **Tip 3:** Return a boolean from the pass-checking method.
</details>

### 7. Array frequency report
Read several integers and display each distinct value with its frequency.

<details><summary>Hints</summary>

- **Tip 1:** Visit each value.
- **Tip 2:** Check whether it was processed earlier.
- **Tip 3:** Use another loop to count occurrences.
</details>

### 8. Pattern generator
Ask for a row count and let the user choose a triangle, inverted triangle or rectangle.

<details><summary>Hints</summary>

- **Tip 1:** Use `switch` for the pattern choice.
- **Tip 2:** Use nested loops for rows and columns.
- **Tip 3:** Print a newline after each row.
</details>

## Final checklist

- [ ] I can write a program from a blank file.
- [ ] I can use variables, input and output.
- [ ] I can calculate values and write conditions.
- [ ] I can use loops and nested loops.
- [ ] I can solve number and String problems.
- [ ] I can use arrays and methods.
- [ ] I understand classes, objects and constructors.
- [ ] I can explain the logic before writing code.

**The goal is not to memorise every program. The goal is to understand the steps and build a solution independently.**

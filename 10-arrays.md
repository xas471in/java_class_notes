# Java Arrays — Class 10 Learning Guide

> **Goal:** Learn arrays step by step, understand how to solve array problems, and practise without depending on ready-made answers.
>
> **How to use this guide**
> 1. Read one concept at a time.
> 2. Type and run the example yourself.
> 3. Trace the program with a small input.
> 4. Attempt the practice questions before opening any hints.
> 5. Use hints in order: **Tip 1** first, then **Tip 2** only if needed.
> 6. Write the solution in your own words. Do not just memorise code.

---

## Contents

- [Level 1 — Basics](#level-1--basic-arrays)
- [Level 2 — Intermediate](#level-2--intermediate-arrays)
- [Level 3 — Advanced](#level-3--advanced-arrays)
- [Level 4 — Mixed Practice](#level-4--mixed-practice)
- [Common Mistakes](#common-mistakes)
- [Answer Key](#answer-key)

---

# Level 1 — Basic Arrays

## 1. What is an array?

An **array** stores multiple values of the same data type under one variable name. Each value is stored at a position called an **index**.

For example, instead of creating five separate variables for marks, we can use one array:

```java
int marks[] = {78, 85, 92, 67, 80};
```

### Why use arrays?

- Store many values using one variable name.
- Access a value using its index.
- Use loops to process all values.
- Make tasks such as calculating a total or finding the largest number easier.

## 2. Declaring, creating and initializing arrays

### Declaration

```java
int numbers[];
// Also valid:
int[] numbers;
```

### Creating an array

```java
numbers = new int[5];
```

This creates space for five integers. The array's size is fixed after creation.

### Declaration and creation together

```java
int numbers[] = new int[5];
```

### Initializing with values

```java
int numbers[] = {10, 20, 30, 40, 50};
```

Java also allows:

```java
int[] numbers = new int[] {10, 20, 30, 40, 50};
```

## 3. Understanding indexes

Array indexes start at **0**, not 1.

For this array:

```java
int numbers[] = {10, 20, 30, 40, 50};
```

| Index | Value |
|---:|---:|
| 0 | 10 |
| 1 | 20 |
| 2 | 30 |
| 3 | 40 |
| 4 | 50 |

```java
System.out.println(numbers[0]); // 10
System.out.println(numbers[2]); // 30
System.out.println(numbers[4]); // 50
```

The last valid index is always `array.length - 1`.

**Important:** `numbers[5]` is invalid here because the valid indexes are 0 to 4. It causes an `ArrayIndexOutOfBoundsException`.

## 4. Changing an element

```java
int numbers[] = {10, 20, 30, 40, 50};

numbers[2] = 99;

System.out.println(numbers[2]); // 99
```

The third value changes from 30 to 99.

## 5. The `length` property

Use `arrayName.length` to get the number of elements.

```java
int numbers[] = {10, 20, 30, 40, 50};

System.out.println(numbers.length); // 5
```

`length` is a **property**, not a method. Write `numbers.length`, not `numbers.length()`.

## 6. Displaying all elements with a `for` loop

```java
class DisplayArray {
    public static void main(String args[]) {
        int numbers[] = {10, 20, 30, 40, 50};

        for (int i = 0; i < numbers.length; i++) {
            System.out.println(numbers[i]);
        }
    }
}
```

- `i = 0`: start at the first index.
- `i < numbers.length`: stop before reaching an invalid index.
- `numbers[i]`: access the current element.

## 7. Taking array input from the user

```java
import java.util.Scanner;

class ArrayInput {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        int numbers[] = new int[5];

        for (int i = 0; i < numbers.length; i++) {
            System.out.print("Enter a number: ");
            numbers[i] = sc.nextInt();
        }

        System.out.println("Array elements:");

        for (int i = 0; i < numbers.length; i++) {
            System.out.println(numbers[i]);
        }

        sc.close();
    }
}
```

The first loop takes input; the second loop displays the values.

## 8. Common array patterns

### A. Find the sum

```java
int numbers[] = {10, 20, 30, 40, 50};
int sum = 0;

for (int i = 0; i < numbers.length; i++) {
    sum = sum + numbers[i];
}

System.out.println("Sum = " + sum); // 150
```

**Pattern:** Start `sum` at 0 and add each element.

### B. Count values that match a condition

```java
int numbers[] = {12, 7, 4, 9, 20, 3};
int count = 0;

for (int i = 0; i < numbers.length; i++) {
    if (numbers[i] % 2 == 0) {
        count++;
    }
}

System.out.println("Even numbers = " + count); // 3
```

**Pattern:** Start `count` at 0 and increase it when the condition is true.

### C. Find the largest value

```java
int numbers[] = {12, 45, 7, 31, 19};
int largest = numbers[0];

for (int i = 1; i < numbers.length; i++) {
    if (numbers[i] > largest) {
        largest = numbers[i];
    }
}

System.out.println("Largest = " + largest); // 45
```

**Pattern:** Assume the first element is the largest, then compare the remaining elements.

This example assumes the array contains at least one element.

### D. Search for a value

```java
int numbers[] = {12, 45, 7, 31, 19};
int target = 31;
boolean found = false;

for (int i = 0; i < numbers.length; i++) {
    if (numbers[i] == target) {
        found = true;
        break;
    }
}

if (found) {
    System.out.println("Value found");
} else {
    System.out.println("Value not found");
}
```

`break` stops the loop once the value is found.

## 9. Basic practice questions

Try these without looking at the answer key.

1. Create an integer array containing 5 values and display all values.
2. Take 10 integers from the user and display them in the same order.
3. Take 8 integers and display them in reverse order.
4. Take 10 integers and calculate their sum.
5. Take 10 integers and calculate their average.
6. Take 10 integers and count how many are even.
7. Take 10 integers and count how many are odd.
8. Take 10 integers and count how many are positive, negative and zero.
9. Take 10 integers and display the largest number.
10. Take 10 integers and display the smallest number.
11. Take a number from the user and check whether it exists in the array.
12. Take 10 integers and display only the values greater than 50.
13. Take 10 integers and calculate the sum of all even numbers.
14. Take 10 integers and calculate the sum of all odd numbers.
15. Take a sentence from the user and count only alphabetic characters. Do not count spaces, digits or punctuation.
16. Take a sentence and display its longest word.

### Hints for selected basic questions

<details>
<summary>Question 3 — Reverse order</summary>

- **Tip 1:** The last valid index is `array.length - 1`.
- **Tip 2:** Start the loop at the last index and decrease `i`.
- **Tip 3:** Use `i >= 0` as the loop condition.
</details>

<details>
<summary>Question 5 — Average</summary>

- **Tip 1:** Calculate the sum first.
- **Tip 2:** Divide the sum by the number of elements.
- **Tip 3:** Use `double` if you want to preserve decimal values.
</details>

<details>
<summary>Question 8 — Positive, negative and zero</summary>

- **Tip 1:** Create three counters, each starting at 0.
- **Tip 2:** Use `if`, `else if` and `else`.
- **Tip 3:** A number equal to 0 is neither positive nor negative.
</details>

<details>
<summary>Question 15 — Count alphabetic characters</summary>

- **Tip 1:** Read the complete sentence using `nextLine()`.
- **Tip 2:** Visit each character using `charAt(i)`.
- **Tip 3:** `Character.isLetter(ch)` checks whether a character is a letter.
</details>

<details>
<summary>Question 16 — Longest word</summary>

- **Tip 1:** Split the sentence into words using `split("\\s+")`.
- **Tip 2:** Keep a variable named `longest`.
- **Tip 3:** Replace `longest` whenever the current word has more characters.
</details>

---

# Level 2 — Intermediate Arrays

## 1. Linear search and finding an index

Linear search checks each element one by one until the target is found or the array ends.

```java
int numbers[] = {14, 8, 25, 6, 19};
int target = 25;
int position = -1;

for (int i = 0; i < numbers.length; i++) {
    if (numbers[i] == target) {
        position = i;
        break;
    }
}

if (position != -1) {
    System.out.println("Found at index " + position);
} else {
    System.out.println("Not found");
}
```

Here, `-1` means that the target was not found. Array indexes can never be negative.

## 2. Second-largest distinct value

```java
int numbers[] = {12, 45, 7, 45, 31};
int largest = Integer.MIN_VALUE;
int secondLargest = Integer.MIN_VALUE;

for (int i = 0; i < numbers.length; i++) {
    int current = numbers[i];

    if (current > largest) {
        secondLargest = largest;
        largest = current;
    } else if (current > secondLargest && current < largest) {
        secondLargest = current;
    }
}

if (secondLargest == Integer.MIN_VALUE) {
    System.out.println("No second-largest distinct value");
} else {
    System.out.println("Second largest = " + secondLargest);
}
```

This example is useful for learning comparisons, but using `Integer.MIN_VALUE` as a marker has an edge case if that exact value is present in the array. A more robust solution should track whether the largest and second-largest values have been found using boolean variables.

**Key idea:** The second-largest *distinct* value must be smaller than the largest value.

## 3. Reverse an array in place

“In place” means changing the original array instead of creating another array.

```java
int numbers[] = {10, 20, 30, 40, 50};

int left = 0;
int right = numbers.length - 1;

while (left < right) {
    int temp = numbers[left];
    numbers[left] = numbers[right];
    numbers[right] = temp;

    left++;
    right--;
}

for (int i = 0; i < numbers.length; i++) {
    System.out.print(numbers[i] + " ");
}
// Output: 50 40 30 20 10
```

`temp` temporarily stores a value so it is not lost while swapping.

## 4. Count the frequency of a value

```java
int numbers[] = {2, 5, 2, 7, 2, 5};
int target = 2;
int count = 0;

for (int i = 0; i < numbers.length; i++) {
    if (numbers[i] == target) {
        count++;
    }
}

System.out.println(target + " appears " + count + " times.");
// Output: 2 appears 3 times.
```

## 5. Check whether an array is sorted

This checks whether the array is in ascending order.

```java
int numbers[] = {3, 8, 12, 19, 25};
boolean sorted = true;

for (int i = 0; i < numbers.length - 1; i++) {
    if (numbers[i] > numbers[i + 1]) {
        sorted = false;
        break;
    }
}

System.out.println(sorted ? "Sorted" : "Not sorted");
```

Compare each element with the element immediately after it.

## 6. Remove a value conceptually

A normal Java array has a fixed size. We cannot truly shrink it by deleting an element. One beginner-friendly approach is to copy all values except the target into a new array.

Before coding, decide what should happen if the target appears more than once: remove the first occurrence or all occurrences. These are different problems.

## 7. Intermediate practice questions

1. Find the index of a value entered by the user. Display `Not found` if it does not exist.
2. Count how many times a target number occurs.
3. Find the second-largest distinct number.
4. Find the second-smallest distinct number.
5. Reverse an array without creating another array.
6. Check whether an array is sorted in ascending order.
7. Check whether an array is sorted in descending order.
8. Copy one array into another.
9. Compare two arrays and check whether their elements are identical in the same order.
10. Count the numbers divisible by both 3 and 5.
11. Display all array elements that occur more than once.
12. Display each distinct number and its frequency.
13. Move all zeroes to the end while keeping the order of non-zero values unchanged.
14. Merge two arrays into a third array.
15. Find the difference between the largest and smallest values.
16. Rotate an array one position to the right.
17. Rotate an array one position to the left.
18. Remove the first occurrence of a value by copying the remaining values into a new array.
19. Find the common values in two arrays.
20. Find the longest word in a sentence and display its length.

### Hints for selected intermediate questions

<details>
<summary>Question 3 — Second-largest distinct number</summary>

- **Tip 1:** Track both `largest` and `secondLargest`.
- **Tip 2:** When a new largest value is found, the old largest becomes the second largest.
- **Tip 3:** Do not count a duplicate of the largest value as the second-largest distinct value.
</details>

<details>
<summary>Question 6 — Ascending order</summary>

- **Tip 1:** Compare neighbouring elements.
- **Tip 2:** If `numbers[i] > numbers[i + 1]`, the order is broken.
- **Tip 3:** You only need to inspect indexes up to `length - 2`.
</details>

<details>
<summary>Question 13 — Move zeroes to the end</summary>

- **Tip 1:** Keep a position for the next non-zero element.
- **Tip 2:** Copy non-zero values forward in their original order.
- **Tip 3:** Fill the remaining positions with zeroes.
</details>

<details>
<summary>Question 16 — Rotate right</summary>

- **Tip 1:** Save the last element before changing anything.
- **Tip 2:** Move each element one position to the right, starting from the end.
- **Tip 3:** Put the saved value at index 0.
</details>

---

# Level 3 — Advanced Arrays

These problems combine multiple array operations. Some may be beyond a particular Class 10 board's syllabus, so use them as enrichment if needed.

## 1. Bubble sort

Bubble sort repeatedly compares neighbouring values and swaps them if they are in the wrong order.

```java
int numbers[] = {5, 2, 8, 1, 3};

for (int i = 0; i < numbers.length - 1; i++) {
    for (int j = 0; j < numbers.length - 1 - i; j++) {
        if (numbers[j] > numbers[j + 1]) {
            int temp = numbers[j];
            numbers[j] = numbers[j + 1];
            numbers[j + 1] = temp;
        }
    }
}

for (int i = 0; i < numbers.length; i++) {
    System.out.print(numbers[i] + " ");
}
// Output: 1 2 3 5 8
```

After each full pass, the largest remaining unsorted value reaches its correct position at the end.

## 2. Merge two sorted arrays

Given two arrays already sorted in ascending order, create a third sorted array containing all their elements.

Example:

```text
First array:  1 4 7
Second array: 2 3 8
Merged array: 1 2 3 4 7 8
```

**Approach:**
1. Keep one index for each input array.
2. Compare the current values.
3. Copy the smaller value into the result array.
4. Move the index of the array you copied from.
5. Copy any remaining values after one array ends.

## 3. Two-dimensional arrays

A two-dimensional array stores data in rows and columns, like a table.

```java
int marks[][] = {
    {80, 75, 90},
    {65, 88, 72}
};

System.out.println(marks[0][0]); // 80
System.out.println(marks[1][2]); // 72
```

The first index represents the row; the second represents the column.

### Display a 2D array

```java
int numbers[][] = {
    {1, 2, 3},
    {4, 5, 6}
};

for (int i = 0; i < numbers.length; i++) {
    for (int j = 0; j < numbers[i].length; j++) {
        System.out.print(numbers[i][j] + " ");
    }
    System.out.println();
}
```

The outer loop visits each row. The inner loop visits each value in that row.

## 4. Advanced practice questions

1. Sort an array in ascending order using bubble sort.
2. Sort an array in descending order.
3. Find the third-largest distinct number.
4. Merge two sorted arrays into one sorted array.
5. Find the missing number from values that should contain every integer from 1 to `n`, with exactly one missing.
6. Find all pairs of elements whose sum equals a target.
7. Find the element that appears most frequently.
8. Rotate an array by `k` positions.
9. Separate even and odd numbers while preserving their original relative order.
10. Find the intersection of two arrays without displaying duplicates.
11. Add two matrices of the same dimensions.
12. Find the sum of each row in a 2D array.
13. Find the sum of each column in a 2D array.
14. Find the largest element in a 2D array.
15. Find the sum of the main diagonal of a square matrix.
16. Check whether a square matrix is an identity matrix.

### Hints for selected advanced questions

<details>
<summary>Question 5 — Missing number</summary>

- **Tip 1:** The expected values are from 1 through `n`.
- **Tip 2:** Calculate the expected sum using `n * (n + 1) / 2`.
- **Tip 3:** Subtract the actual array sum from the expected sum. This approach assumes exactly one number is missing and no values are duplicated.
</details>

<details>
<summary>Question 6 — Pairs with a target sum</summary>

- **Tip 1:** Use one loop to choose the first element.
- **Tip 2:** Use a second loop starting at `i + 1` to choose the second element.
- **Tip 3:** Check whether `numbers[i] + numbers[j] == target`.
</details>

<details>
<summary>Question 11 — Add two matrices</summary>

- **Tip 1:** Both matrices must have the same number of rows and columns.
- **Tip 2:** Add values at matching row and column indexes.
- **Tip 3:** Store the result in a third 2D array.
</details>

---

# Level 4 — Mixed Practice

**Rules for this section**

- Try to solve each question without looking at a solution.
- You may use arrays, loops, `if-else`, `String` methods and `Scanner`.
- Write down your approach before coding.
- Use the hints only when stuck.
- Check edge cases, such as repeated values, negative numbers, empty input and equal-length words.

## Mixed questions

### M1. Marks report

Take marks for 10 students. Display the total, average, highest mark, lowest mark and number of students who passed. Assume the pass mark is 40.

<details>
<summary>Hints</summary>

- **Tip 1:** Store all marks in an array.
- **Tip 2:** Use one loop to calculate the total, maximum, minimum and pass count.
- **Tip 3:** Calculate the average after the loop.
</details>

### M2. Reverse only the output

Take 8 integers and display them in reverse order without changing the original array.

<details>
<summary>Hints</summary>

- **Tip 1:** No second array is required.
- **Tip 2:** Start at `array.length - 1`.
- **Tip 3:** Decrease the index until it reaches 0.
</details>

### M3. Unique values

Take 10 integers and display each distinct value only once.

<details>
<summary>Hints</summary>

- **Tip 1:** For each value, check whether it appeared earlier.
- **Tip 2:** Compare the current value with indexes before the current index.
- **Tip 3:** Print it only if no earlier matching value exists.
</details>

### M4. Word statistics

Take a sentence and display the number of words, the longest word and the shortest word.

<details>
<summary>Hints</summary>

- **Tip 1:** Split the sentence into words using whitespace.
- **Tip 2:** Start both longest and shortest with the first word.
- **Tip 3:** Compare each word's length with both stored words.
</details>

### M5. Move negative numbers

Take an integer array and move all negative numbers to the beginning while keeping the relative order of the negative values and non-negative values unchanged.

<details>
<summary>Hints</summary>

- **Tip 1:** Think about creating a second array.
- **Tip 2:** Copy negative values first, in their original order.
- **Tip 3:** Copy zero and positive values afterwards.
</details>

### M6. Target pairs

Take an array and a target number. Display every pair of different indexes whose values add up to the target.

<details>
<summary>Hints</summary>

- **Tip 1:** Use two loops.
- **Tip 2:** Start the inner loop at `i + 1` so a pair is not repeated in reverse order.
- **Tip 3:** Print the pair whenever the sum equals the target.
</details>

### M7. Rotate by `k`

Take an array and a positive integer `k`. Rotate the array to the right by `k` positions.

<details>
<summary>Hints</summary>

- **Tip 1:** Reduce unnecessary rotations with `k = k % array.length`.
- **Tip 2:** One simple solution uses a temporary array.
- **Tip 3:** Test cases where `k` is 0, equal to the array length, and greater than the array length. Handle an empty array before using `% array.length`.
</details>

### M8. Matrix row totals

Take a 3 × 3 matrix and display the sum of each row and the sum of each column.

<details>
<summary>Hints</summary>

- **Tip 1:** Use nested loops to read the matrix.
- **Tip 2:** For row totals, keep one sum for each row.
- **Tip 3:** For column totals, keep one sum for each column.
</details>

### M9. Frequency report

Take 10 integers and display the frequency of each distinct number exactly once.

<details>
<summary>Hints</summary>

- **Tip 1:** Visit each element.
- **Tip 2:** Before counting, check whether the value was already processed at an earlier index.
- **Tip 3:** Count its occurrences with another loop and print the result once.
</details>

### M10. Alphabet count and longest word

Take a sentence from the user. Count only alphabetic characters, ignoring spaces, digits and punctuation. Then display the longest word.

<details>
<summary>Hints</summary>

- **Tip 1:** Use `Character.isLetter()` for counting alphabetic characters.
- **Tip 2:** Use `split("\\s+")` to separate words.
- **Tip 3:** Keep the alphabet count and longest-word search as two separate steps.
</details>

---

# Common Mistakes

1. **Starting at index 1:** This skips the first element. Start at 0 unless there is a specific reason not to.
2. **Using `i <= array.length`:** This eventually accesses an invalid index. Use `i < array.length`.
3. **Writing `array.length()`:** Arrays use the property `array.length`.
4. **Forgetting to initialize a sum or counter:** Usually start these variables at 0.
5. **Setting the largest value to 0:** This fails if every array value is negative. Start with the first element when the array is not empty.
6. **Confusing an index with a value:** `i` is the index; `array[i]` is the value.
7. **Using `next()` for a sentence:** `next()` reads one token. Use `nextLine()` for a complete line.
8. **Assuming an array can shrink:** Java arrays have a fixed length. Create a new array if you need a different size.
9. **Not testing edge cases:** Test duplicates, negative values, zero, one-element arrays and targets that are not found.
10. **Copying code without tracing it:** Test a small example and follow each variable's value line by line.

---

# Answer Key

Use this section only after attempting the practice questions. Answers are short reference solutions or approaches, not a replacement for understanding the code.

## Basic examples

### B1. Sum of an array

```java
int[] a = {10, 20, 30, 40};
int sum = 0;

for (int i = 0; i < a.length; i++) {
    sum += a[i];
}

System.out.println(sum); // 100
```

### B2. Count even numbers

```java
int[] a = {2, 7, 8, 11, 14};
int count = 0;

for (int i = 0; i < a.length; i++) {
    if (a[i] % 2 == 0) {
        count++;
    }
}

System.out.println(count); // 3
```

### B3. Count alphabetic characters in a sentence

```java
String str = "Java Class 10!";
int count = 0;

for (int i = 0; i < str.length(); i++) {
    if (Character.isLetter(str.charAt(i))) {
        count++;
    }
}

System.out.println(count); // 9
```

### B4. Longest word in a sentence

```java
String str = "Java is a powerful language";
String[] words = str.trim().split("\\s+");
String longest = "";

for (int i = 0; i < words.length; i++) {
    if (words[i].length() > longest.length()) {
        longest = words[i];
    }
}

System.out.println(longest); // powerful
```

For empty input, add a check before processing the words. This simple example assumes a non-empty sentence.

## Intermediate examples

### I1. Check if an array is sorted

```java
int[] a = {2, 4, 6, 8};
boolean sorted = true;

for (int i = 0; i < a.length - 1; i++) {
    if (a[i] > a[i + 1]) {
        sorted = false;
        break;
    }
}

System.out.println(sorted);
```

### I2. Copy an array

```java
int[] a = {4, 8, 12};
int[] copy = new int[a.length];

for (int i = 0; i < a.length; i++) {
    copy[i] = a[i];
}
```

### I3. Find common values (simple approach)

```java
int[] a = {2, 4, 6, 8};
int[] b = {1, 4, 8, 10};

for (int i = 0; i < a.length; i++) {
    for (int j = 0; j < b.length; j++) {
        if (a[i] == b[j]) {
            System.out.println(a[i]);
            break;
        }
    }
}
```

This prints common values for arrays without duplicate values. Extra checks are needed to avoid duplicate output if the input arrays contain duplicates.

## Advanced example: add two 2D arrays

```java
int[][] a = {
    {1, 2},
    {3, 4}
};

int[][] b = {
    {5, 6},
    {7, 8}
};

int[][] result = new int[2][2];

for (int i = 0; i < a.length; i++) {
    for (int j = 0; j < a[i].length; j++) {
        result[i][j] = a[i][j] + b[i][j];
        System.out.print(result[i][j] + " ");
    }
    System.out.println();
}
```

Output:

```text
6 8
10 12
```

---

## Final checklist

Before moving to the next Java topic, make sure you can:

- [ ] Declare, create and initialize an array.
- [ ] Explain why indexes start at 0.
- [ ] Use `array.length` correctly.
- [ ] Take input into an array with `Scanner`.
- [ ] Traverse an array using a loop.
- [ ] Calculate sums, counts, minimums and maximums.
- [ ] Search for a value.
- [ ] Reverse and sort an array.
- [ ] Explain your logic before writing code.
- [ ] Solve at least a few mixed questions without hints.

**Remember:** Understanding the approach matters more than memorising a program.

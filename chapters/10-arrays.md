# Chapter 10: Arrays — Keeping Many Values Together

> **Today’s goal:** Store several values of the same type in one variable and access them by position.

---

## 1. Why do we need an array?

Imagine storing five students' marks.

Without an array, we might create five separate variables:

```java
int mark1 = 70;
int mark2 = 85;
int mark3 = 92;
int mark4 = 64;
int mark5 = 78;
```

That gets messy when there are many values.

An array lets us keep related values together.

```text
marks ──►  ┌────┬────┬────┬────┬────┐
           │ 70 │ 85 │ 92 │ 64 │ 78 │
           └────┴────┴────┴────┴────┘
Index:       0    1    2    3    4
```

Each box is called an **element**. Its position number is called an **index**.

---

## 2. Create an array

```java
int[] marks = {70, 85, 92, 64, 78};
```

This creates an integer array with five elements.

To display one value:

```java
System.out.println(marks[0]); // 70
System.out.println(marks[2]); // 92
```

**Important:** Java array indexes start at `0`, not `1`.

For an array of 5 elements, the valid indexes are `0, 1, 2, 3, 4`.

---

## 3. Change an element

```java
int[] marks = {70, 85, 92};

marks[1] = 90;

System.out.println(marks[1]); // 90
```

The value at index 1 changes from 85 to 90.

---

## 4. Create an array with a fixed size

```java
int[] numbers = new int[5];
```

This creates space for five integers. Java fills a new `int` array with zeros.

We can fill the elements one by one:

```java
numbers[0] = 10;
numbers[1] = 20;
numbers[2] = 30;
numbers[3] = 40;
numbers[4] = 50;
```

An array's size cannot be changed after it has been created.

---

## 5. Use a loop to visit every element

```java
int[] marks = {70, 85, 92, 64, 78};

for (int i = 0; i < marks.length; i++) {
    System.out.println(marks[i]);
}
```

`marks.length` tells us how many elements are in the array.

Why does the loop use `i < marks.length`? For five elements, the indexes are 0 through 4. The condition stops before index 5.

---

## 6. Find the total

```java
int[] numbers = {10, 20, 30};
int sum = 0;

for (int i = 0; i < numbers.length; i++) {
    sum = sum + numbers[i];
}

System.out.println(sum); // 60
```

The variable `sum` starts at 0, and each array value is added to it.

---

## 7. Find the largest value

```java
int[] numbers = {12, 45, 8, 32, 19};
int largest = numbers[0];

for (int i = 1; i < numbers.length; i++) {
    if (numbers[i] > largest) {
        largest = numbers[i];
    }
}

System.out.println(largest); // 45
```

Start by treating the first value as the largest. Then compare every other value against it.

---

## 8. Search for a value

```java
int[] numbers = {12, 45, 8, 32, 19};
int target = 8;
boolean found = false;

for (int i = 0; i < numbers.length; i++) {
    if (numbers[i] == target) {
        found = true;
        break;
    }
}

if (found) {
    System.out.println("Found");
} else {
    System.out.println("Not found");
}
```

This is called a **linear search**: check the values one by one.

---

## Practice time

### First steps

1. Create an array of five numbers and display the first element.
2. Display the third element.
3. Change the second element and display it.
4. Display every element using a loop.
5. Display how many elements the array contains.

### Getting comfortable

6. Find the sum of all elements.
7. Find the average of the elements.
8. Count how many values are greater than 50.
9. Find the largest value.
10. Find the smallest value.
11. Search for a number and display whether it exists.
12. Count how many times a chosen number appears.

### A little more practice

13. Display the array in reverse order.
14. Count even and odd values.
15. Copy the values into a second array.
16. Find the second-largest value, assuming the array has at least two distinct values.
17. Display only values greater than the average.
18. Read five marks from the user and display their total and average.

<details>
<summary>Need a hint? Open this</summary>

- **Tip 1:** Use `array.length` to know how many elements there are.
- **Tip 2:** For a total, start `sum` at `0`.
- **Tip 3:** For a largest or smallest value, start with the first element instead of guessing a number.
- **Tip 4:** Check the indexes carefully. The last valid index is `length - 1`.
</details>

---

## Common mistakes

- Using index 1 to mean the first element.
- Writing `i <= array.length`, which tries to access one position too far.
- Forgetting to initialize a total variable to 0.
- Trying to store a `String` in an `int[]`.

## Quick recap

An array stores several values of one type. Use an index to access a value and a loop to process all the values.

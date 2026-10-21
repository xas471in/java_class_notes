# Chapter 6 — Switch and Menu-Driven Programs

> **Goal:** Select from a list of clear choices.

## Basic `switch`

```java
int day = 3;

switch (day) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");
        break;
    default:
        System.out.println("Invalid day");
}
```

`break` exits the switch. `default` handles choices that do not match a case.

## Menu calculator

```java
switch (choice) {
    case 1:
        System.out.println(a + b);
        break;
    case 2:
        System.out.println(a - b);
        break;
    case 3:
        System.out.println(a * b);
        break;
    case 4:
        if (b != 0) {
            System.out.println(a / b);
        } else {
            System.out.println("Cannot divide by zero");
        }
        break;
    default:
        System.out.println("Invalid choice");
}
```

Use `switch` for discrete choices. Use `if-else` for ranges and complex conditions.

## Practice

1. Enter a number from 1 to 7 and display the weekday.
2. Enter a month number and display its name.
3. Build a calculator menu.
4. Create a menu to calculate square, rectangle or circle area.
5. Create a unit-conversion menu.
6. Use letters as menu choices.
7. Create a menu for square, cube or square root.
8. Create a food-order menu and calculate the bill.
9. Display a description based on a menu choice.
10. Handle invalid choices.

<details><summary>Hints</summary>

- **Tip 1:** Display options before asking for a choice.
- **Tip 2:** Use `break` in each case.
- **Tip 3:** Include `default` and handle invalid calculations.
</details>

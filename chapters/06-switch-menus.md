# Chapter 6: Choosing from a Menu with `switch`

> **Today’s goal:** Use `switch` when a program offers several separate choices.

---

## 1. When is `switch` useful?

Imagine a menu:

```text
1. Add
2. Subtract
3. Multiply
4. Divide

Enter your choice: 3
```

A `switch` statement lets us write what should happen for each choice.

---

## 2. A small example

```java
int day = 2;

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

Output:

```text
Tuesday
```

- `case` means “when the value matches this choice”.
- `break` exits the `switch`.
- `default` runs when no case matches.

---

## 3. A simple menu program

```java
import java.util.Scanner;

class Menu {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("1. Say Hello");
        System.out.println("2. Say Goodbye");
        System.out.print("Choose 1 or 2: ");

        int choice = sc.nextInt();

        switch (choice) {
            case 1:
                System.out.println("Hello!");
                break;
            case 2:
                System.out.println("Goodbye!");
                break;
            default:
                System.out.println("Please choose 1 or 2.");
        }

        sc.close();
    }
}
```

---

## 4. `if-else` or `switch`?

Use `if-else` for ranges, such as marks greater than 80.

Use `switch` for separate choices, such as menu option 1, 2 or 3.

---

## Practice time

1. Enter a number from 1 to 7 and display the weekday.
2. Enter a month number and display the month name.
3. Create a menu that adds, subtracts, multiplies or divides two numbers.
4. Create a menu to calculate the area of a square or rectangle.
5. Create a menu for square, cube or square root.
6. Use `A`, `B` and `C` as menu choices.
7. Create a simple food menu and calculate the bill.
8. Display a message based on the user's menu choice.
9. Display a helpful message for an invalid choice.

<details>
<summary>Need a hint? Open this</summary>

- **Tip 1:** Display the menu before reading the choice.
- **Tip 2:** Give each case a clear action.
- **Tip 3:** Include `break` and a `default` case.
</details>

---

## Quick recap

A menu makes a program easier to use. `switch` connects each choice with the action that should happen.

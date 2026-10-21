# Switch Case and Menu-Driven Programs — Class 10 Java

## Goal
Use `switch` to choose between several options and build simple menu-driven programs.

## 1. Basic `switch`

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

`break` exits the switch. Without it, execution can continue into later case labels (fall-through). `default` handles values that do not match any case.

## 2. Menu-driven calculator

```java
import java.util.Scanner;

class CalculatorMenu {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);

        System.out.println("1. Add");
        System.out.println("2. Subtract");
        System.out.println("3. Multiply");
        System.out.println("4. Divide");
        System.out.print("Choose an option: ");
        int choice = sc.nextInt();

        System.out.print("Enter first number: ");
        double a = sc.nextDouble();

        System.out.print("Enter second number: ");
        double b = sc.nextDouble();

        switch (choice) {
            case 1:
                System.out.println("Result = " + (a + b));
                break;
            case 2:
                System.out.println("Result = " + (a - b));
                break;
            case 3:
                System.out.println("Result = " + (a * b));
                break;
            case 4:
                if (b != 0) {
                    System.out.println("Result = " + (a / b));
                } else {
                    System.out.println("Cannot divide by zero");
                }
                break;
            default:
                System.out.println("Invalid choice");
        }

        sc.close();
    }
}
```

## 3. `switch` vs `if-else`

Use `switch` when selecting among clear discrete choices, such as menu option 1, 2, 3 or 4. Use `if-else` for ranges and complex conditions, such as `marks >= 80`.

## Practice questions

1. Enter a number from 1 to 7 and display the day of the week.
2. Enter a month number and display the month's name.
3. Build a calculator menu for addition, subtraction, multiplication and division.
4. Create a menu to calculate the area of a square, rectangle or circle.
5. Create a menu to convert kilometres to metres or metres to centimetres.
6. Enter a character for a basic menu: `A` for greeting, `B` for farewell, otherwise invalid choice.
7. Create a menu that checks whether a number is even or odd, or positive or negative.
8. Create a menu for finding the square or cube of a number.
9. Create a menu for displaying a grade description.
10. Build a simple food-order menu with prices and calculate the bill.

<details>
<summary>Hints</summary>

- **Tip 1:** Display the options before asking for the choice.
- **Tip 2:** Read the choice into an integer or character variable.
- **Tip 3:** Include `break` in each case and a `default` branch.
</details>

## Common mistakes

- Forgetting `break`.
- Forgetting `default`.
- Using `switch` for ranges such as `marks >= 40`.
- Forgetting to check division by zero.
- Not handling an invalid menu choice.

## Checklist

- [ ] I can write a `switch` statement.
- [ ] I understand `case`, `break` and `default`.
- [ ] I can create a menu-driven program.

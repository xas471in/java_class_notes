# Chapter 12 — Methods and Reusable Code

> **Goal:** Break a program into named tasks that can be reused.

## A simple method

```java
class Greeting {
    static void sayHello() {
        System.out.println("Hello!");
    }

    public static void main(String args[]) {
        sayHello();
        sayHello();
    }
}
```

## Parameters and arguments

```java
static void greet(String name) {
    System.out.println("Hello, " + name);
}
```

`name` is a parameter. A value supplied when calling the method is an argument.

## Return a value

```java
static int add(int a, int b) {
    return a + b;
}
```

A method's return type must match the value returned. `void` means the method does not return a value.

## Reusable calculation

```java
static double rectangleArea(double length, double breadth) {
    return length * breadth;
}
```

## Method overloading

Methods can share a name if their parameter lists differ.

```java
static int add(int a, int b) {
    return a + b;
}

static int add(int a, int b, int c) {
    return a + b + c;
}
```

Changing only the return type does not create a valid overload.

## Practice

1. Write a method that displays your name.
2. Display the square of a number using a method.
3. Return the sum of two integers.
4. Return the larger of two numbers.
5. Return whether a number is even.
6. Return the area of a rectangle.
7. Convert Celsius to Fahrenheit using a method.
8. Return the sum of digits.
9. Check whether a number is prime.
10. Return factorial.
11. Count vowels in a String.
12. Overload `add()` for two and three integers.
13. Return Pass or Fail based on marks.
14. Return the average of three numbers as a `double`.
15. Return the reverse of a String.

<details><summary>Hints</summary>

- **Tip 1:** Decide whether to print a result or return it.
- **Tip 2:** Choose a return type that matches the result.
- **Tip 3:** Keep the calculation in the method and call it from `main()`.
</details>

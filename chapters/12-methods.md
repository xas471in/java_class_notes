# Chapter 12: Methods — Give a Task Its Own Name

> **Today’s goal:** Put instructions into reusable blocks so you do not need to write the same code again.

---

## 1. Imagine a reusable machine

A method is like a small machine. You give it information, it performs a task, and it may give you a result.

```text
Input values ──► Method does a task ──► Result
```

---

## 2. A method that displays a message

```java
class Greeting {
    static void sayHello() {
        System.out.println("Hello!");
    }

    public static void main(String[] args) {
        sayHello();
        sayHello();
    }
}
```

Output:

```text
Hello!
Hello!
```

We wrote the instructions once and called the method twice.

---

## 3. Give a method information

```java
static void greet(String name) {
    System.out.println("Hello, " + name);
}
```

Call it like this:

```java
greet("Riya");
greet("Aman");
```

`name` is a parameter: it receives the value passed to the method.

---

## 4. Return an answer

A method can calculate something and send the answer back using `return`.

```java
static int add(int a, int b) {
    return a + b;
}
```

Use it like this:

```java
int answer = add(10, 20);
System.out.println(answer); // 30
```

The word `int` says the method returns an integer. `void` means it does not return a value.

---

## 5. A method for a calculation

```java
static double rectangleArea(double length, double breadth) {
    return length * breadth;
}
```

Now the area formula can be reused whenever needed.

---

## Practice time

1. Write a method that displays your name.
2. Write a method that displays the square of a number.
3. Return the sum of two integers.
4. Return the larger of two numbers.
5. Return whether a number is even.
6. Return the area of a rectangle.
7. Convert Celsius to Fahrenheit using a method.
8. Return the sum of a number's digits.
9. Check whether a number is prime using a method.
10. Return the factorial of a number.
11. Count vowels in a String using a method.
12. Return the average of three numbers.
13. Return whether marks are enough to pass.
14. Create two `add()` methods: one for two numbers and one for three.

<details>
<summary>Need a hint? Open this</summary>

- **Tip 1:** Decide whether the method should print a result or return it.
- **Tip 2:** Choose a return type that matches the answer.
- **Tip 3:** Call the method from `main()` to use it.
</details>

---

## Quick recap

Methods divide a program into smaller tasks. They make code easier to read, test and reuse.

# Methods (Functions) in Java — Class 10

## Goal
Understand methods, parameters, arguments, return types and how methods help avoid repeating code.

## 1. What is a method?

A method is a named block of code that performs a task. It can be called whenever that task is needed.

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

Output:
```text
Hello!
Hello!
```

`static` allows this example to call the method directly from `main()` without creating an object. Object methods will be covered later.

## 2. Method with parameters

Parameters are variables listed in the method declaration. Arguments are the actual values passed when calling it.

```java
static void greet(String name) {
    System.out.println("Hello, " + name);
}

public static void main(String args[]) {
    greet("Riya");
    greet("Aman");
}
```

`name` is a parameter. `"Riya"` and `"Aman"` are arguments.

## 3. Method with a return value

A method can return a result using `return`.

```java
static int add(int a, int b) {
    return a + b;
}

public static void main(String args[]) {
    int result = add(10, 20);
    System.out.println(result); // 30
}
```

The return type is `int`, so the method must return an integer value on every valid path.

## 4. `void` methods

A `void` method does not return a value.

```java
static void displaySquare(int number) {
    System.out.println(number * number);
}
```

## 5. Return types

Common return types include `int`, `double`, `boolean`, `char`, `String` and `void`.

```java
static boolean isEven(int number) {
    return number % 2 == 0;
}
```

## 6. Reusing methods

```java
static double rectangleArea(double length, double breadth) {
    return length * breadth;
}
```

Call it with different arguments rather than rewriting the formula repeatedly.

## 7. Method overloading (introductory)

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

## Practice questions

1. Write a `void` method that displays your name.
2. Write a method that takes an integer and displays its square.
3. Write a method that returns the sum of two integers.
4. Write a method that returns the larger of two numbers.
5. Write a method that checks whether a number is even.
6. Write a method that returns the area of a rectangle.
7. Write a method that converts Celsius to Fahrenheit.
8. Write a method that returns the sum of digits of a positive integer.
9. Write a method that checks whether a number is prime.
10. Write a method that returns the factorial of a non-negative integer.
11. Write a method that counts vowels in a String.
12. Overload an `add` method for two and three integers.
13. Write a method that takes marks and returns Pass or Fail as a String.
14. Write a method that takes three numbers and returns their average as a `double`.
15. Write a method that returns the reverse of a String.

<details>
<summary>Hints</summary>

- **Tip 1:** Decide whether the method needs to print a result or return it.
- **Tip 2:** Choose a return type that matches the value.
- **Tip 3:** Keep the calculation inside the method and call it from `main()`.
</details>

## Common mistakes

- Calling a method with the wrong number or type of arguments.
- Declaring a non-void method without returning a value.
- Trying to use a returned value from a `void` method.
- Expecting a local variable inside a method to be directly available in another method.
- Thinking that changing only the return type overloads a method.

## Checklist

- [ ] I can declare and call a method.
- [ ] I understand parameters and arguments.
- [ ] I can return a value.
- [ ] I can reuse methods to keep code organised.

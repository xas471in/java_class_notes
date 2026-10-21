# Classes and Objects — Class 10 Java

## Goal
Understand classes as blueprints and objects as instances with data and behaviour.

## 1. What is a class?

A class defines the fields (data) and methods (behaviour) that its objects can have.

## 2. What is an object?

An object is an instance of a class. It can hold its own field values and use the class's methods.

```java
class Student {
    String name;
    int age;

    void display() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

class Main {
    public static void main(String args[]) {
        Student s1 = new Student();
        s1.name = "Riya";
        s1.age = 15;
        s1.display();
    }
}
```

## 3. Understanding object creation

```java
Student s1 = new Student();
```

- `Student` is the class type.
- `s1` is a reference variable.
- `new Student()` creates a new object and calls its constructor.

## 4. Instance variables vs local variables

```java
class Example {
    int number; // Instance variable: belongs to each object

    void show() {
        int temporary = 5; // Local variable: belongs to this method call
        System.out.println(number + temporary);
    }
}
```

Instance variables receive default values if not explicitly initialized. Local variables must be assigned before they are read.

## 5. Multiple objects

```java
Student s1 = new Student();
s1.name = "Riya";
s1.age = 15;

Student s2 = new Student();
s2.name = "Aman";
s2.age = 16;

s1.display();
s2.display();
```

Each object has its own instance fields.

## 6. Fields and methods

- Fields represent the data or state of an object.
- Methods represent actions or behaviour.
- Access an instance field or method using the reference and dot operator, such as `s1.name` or `s1.display()`.

## 7. Encapsulation (intro)

A common design is to make fields `private` and expose methods to read or update them. This protects data from arbitrary changes. Getter and setter methods can be introduced after the basic class/object idea is clear.

## Practice questions

1. Create a `Student` class with name, age and marks, then display the values.
2. Create two `Student` objects with different data.
3. Create a `Book` class with title, author and price.
4. Create a `Rectangle` class with length, breadth and a method that returns area.
5. Create a `Circle` class with radius and a method that returns area.
6. Create an `Employee` class with name and salary.
7. Create a `BankAccount` class with account holder and balance, and a method to display the balance.
8. Create a `Car` class with brand and speed and a method to display its details.
9. Explain the difference between a class and an object using a real-world example.
10. Create a `Student` object and change one field after creation.
11. Add a method that returns whether a student's marks are passing.
12. Create a `Book` object and calculate a discounted price using a method.

<details>
<summary>Hints</summary>

- **Tip 1:** Put fields and methods inside the class.
- **Tip 2:** Use `new ClassName()` to create an object.
- **Tip 3:** Use the dot operator to access public fields and methods in these introductory examples.
</details>

## Common mistakes

- Forgetting to create an object before accessing an instance member.
- Confusing the class name with an object reference.
- Declaring local variables outside the block where they are needed.
- Assuming two objects share the same instance field values.
- Putting `main()` in a class that cannot access the intended members without an object or appropriate static declaration.

## Checklist

- [ ] I can explain class vs object.
- [ ] I can create objects with `new`.
- [ ] I can define instance variables and methods.
- [ ] I understand that separate objects have separate instance fields.

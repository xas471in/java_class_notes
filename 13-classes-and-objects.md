# Chapter 13 — Classes and Objects

> **Goal:** Learn the basics of object-oriented programming with familiar examples.

## Class and object

A class is a blueprint. An object is an instance of that class.

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

## Creating an object

`Student s1 = new Student();`

- `Student` is the type.
- `s1` is a reference variable.
- `new Student()` creates the object.

## Multiple objects

Each object has its own instance field values.

```java
Student s1 = new Student();
s1.name = "Riya";

Student s2 = new Student();
s2.name = "Aman";
```

## Fields and methods

- Fields store object data.
- Methods define behaviour.
- Use the dot operator, such as `s1.name` and `s1.display()`.

## Practice

1. Create a `Student` class with name, age and marks.
2. Create two students with different details.
3. Create a `Book` class with title, author and price.
4. Create a `Rectangle` class with an area method.
5. Create a `Circle` class with an area method.
6. Create an `Employee` class with name and salary.
7. Create a `Car` class with brand and speed.
8. Explain class vs object with a real-world example.
9. Add a method to check whether a student's marks pass.
10. Create a book object and calculate a discounted price.

<details><summary>Hints</summary>

- **Tip 1:** Put fields and methods inside the class.
- **Tip 2:** Create objects with `new ClassName()`.
- **Tip 3:** Use the dot operator to access members.
</details>

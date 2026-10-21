# Chapter 14 — Constructors and `this`

> **Goal:** Initialize objects when created and understand `this`.

## What is a constructor?

A constructor runs when an object is created. Its name matches the class name and it has no return type.

```java
class Student {
    String name;
    int age;

    Student() {
        name = "Unknown";
        age = 0;
    }
}
```

If no constructor is declared, Java may provide a compiler-generated default constructor. Once you declare a constructor, Java does not automatically add that default constructor.

## Parameterized constructor

```java
class Student {
    String name;
    int age;

    Student(String studentName, int studentAge) {
        name = studentName;
        age = studentAge;
    }
}
```

## The `this` keyword

`this` refers to the current object. It is useful when parameters have the same names as fields.

```java
class Student {
    String name;
    int age;

    Student(String name, int age) {
        this.name = name;
        this.age = age;
    }
}
```

`this.name` is the object's field; `name` on the right is the parameter.

## Constructor overloading

```java
class Book {
    String title;
    double price;

    Book() {
        title = "Untitled";
        price = 0;
    }

    Book(String title, double price) {
        this.title = title;
        this.price = price;
    }
}
```

## Practice

1. Create a class with a no-argument constructor.
2. Create a parameterized constructor for name and age.
3. Use `this` with same-named fields and parameters.
4. Initialize a Book's title and price using a constructor.
5. Create a Rectangle constructor for length and breadth.
6. Add two constructors to a Circle class.
7. Create an Employee constructor.
8. Explain constructor vs method.
9. Explain default constructor vs programmer-written no-argument constructor.
10. Fix a constructor where `name = name;` fails to update the field.

<details><summary>Hints</summary>

- **Tip 1:** A constructor has the class name and no return type.
- **Tip 2:** Use parameters to pass data when creating an object.
- **Tip 3:** Use `this.fieldName = parameterName` when names are the same.
</details>

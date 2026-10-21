# Chapter 14: Constructors and `this`

> **Today’s goal:** Give an object its starting values when it is created.

---

## 1. Why use a constructor?

Without a constructor, we might create an object and then assign its fields one by one.

```java
Student s1 = new Student();
s1.name = "Riya";
s1.age = 15;
```

A constructor lets us provide the starting values at the moment the object is created.

---

## 2. A parameterized constructor

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

Create a student like this:

```java
Student s1 = new Student("Riya", 15);
Student s2 = new Student("Aman", 16);
```

The constructor runs when `new Student(...)` creates the object.

Remember:
- A constructor has the same name as the class.
- It has no return type.
- Its job is often to set starting values.

---

## 3. What does `this` mean?

Sometimes a constructor parameter has the same name as a field.

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

`this.name` means the field belonging to the current object. `name` by itself refers to the parameter.

---

## 4. A no-argument constructor

```java
class Book {
    String title;

    Book() {
        title = "Untitled";
    }
}
```

This constructor does not need any values when the object is created:

```java
Book b1 = new Book();
```

If you write no constructor at all, Java may provide a default constructor. Once you write your own constructor, Java does not automatically add that default constructor.

---

## Practice time

1. Create a `Student` class with a constructor for name and age.
2. Create two Student objects with different values.
3. Use `this` when the parameters and fields have the same names.
4. Create a `Book` constructor for title and price.
5. Create a `Rectangle` constructor for length and breadth.
6. Create an `Employee` constructor for name and salary.
7. Write a no-argument constructor that sets a default title.
8. Explain how a constructor differs from a normal method.

<details>
<summary>Need a hint? Open this</summary>

- **Tip 1:** Constructor name = class name.
- **Tip 2:** Do not write `void` before a constructor.
- **Tip 3:** Use `this.field = parameter` when both names are the same.
</details>

---

## Quick recap

Constructors help set up new objects. The keyword `this` helps us refer to the current object's fields.

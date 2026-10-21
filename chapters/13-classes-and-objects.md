# Chapter 13: Classes and Objects

> **Today’s goal:** Group related information and actions into a class, then create objects from it.

---

## 1. A real-world example

A student has information such as a name and age. A student can also perform actions, such as displaying their details.

A **class** describes what a student object will contain. An **object** is one actual student created from that class.

```text
Class: Student
 ├── Data: name, age
 └── Action: display()

       creates
          │
          ▼
Object: s1
 name = "Riya"
 age  = 15
```

---

## 2. Create a class

```java
class Student {
    String name;
    int age;

    void display() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}
```

The class describes the fields and method. It does not display anything until we create an object and call the method.

---

## 3. Create an object

```java
class Main {
    public static void main(String[] args) {
        Student s1 = new Student();

        s1.name = "Riya";
        s1.age = 15;

        s1.display();
    }
}
```

Output:

```text
Name: Riya
Age: 15
```

- `new Student()` creates a Student object.
- `s1` refers to that object.
- The dot `.` lets us access a field or method.

---

## 4. Create more than one object

```java
Student s1 = new Student();
s1.name = "Riya";
s1.age = 15;

Student s2 = new Student();
s2.name = "Aman";
s2.age = 16;
```

Each object has its own `name` and `age`.

---

## Practice time

1. Create a `Student` class with name, age and marks.
2. Create two Student objects with different details.
3. Create a `Book` class with title, author and price.
4. Create a `Rectangle` class with a method to return its area.
5. Create a `Circle` class with an area method.
6. Create an `Employee` class with name and salary.
7. Create a `Car` class with brand and speed.
8. Add a method that checks whether a student's marks meet the pass mark.
9. Explain the difference between a class and an object in your own words.

<details>
<summary>Need a hint? Open this</summary>

- **Tip 1:** Put fields and methods inside the class.
- **Tip 2:** Use `new ClassName()` to create an object.
- **Tip 3:** Use the dot operator to access its fields and methods.
</details>

---

## Quick recap

A class is a blueprint. An object is a specific instance created from that blueprint.

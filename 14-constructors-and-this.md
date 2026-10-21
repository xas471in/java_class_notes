# Constructors and the `this` Keyword — Class 10 Java

## Goal
Learn how constructors initialize objects, compare default/no-argument and parameterized constructors, and understand `this`.

## 1. What is a constructor?

A constructor is a special class member called when an object is created. It initializes the new object.

- Its name must match the class name.
- It has no return type—not even `void`.
- It is called when `new` creates an object.

## 2. No-argument constructor

```java
class Student {
    String name;
    int age;

    Student() {
        name = "Unknown";
        age = 0;
    }

    void display() {
        System.out.println(name + " " + age);
    }
}

class Main {
    public static void main(String args[]) {
        Student s1 = new Student();
        s1.display();
    }
}
```

This constructor takes no arguments and initializes the fields with the values chosen in the constructor.

**Terminology note:** If no constructor is declared at all, Java can provide a default constructor. A programmer-written `Student()` is a no-argument constructor, not the compiler-provided default constructor.

## 3. Parameterized constructor

```java
class Student {
    String name;
    int age;

    Student(String studentName, int studentAge) {
        name = studentName;
        age = studentAge;
    }

    void display() {
        System.out.println(name + " " + age);
    }
}

class Main {
    public static void main(String args[]) {
        Student s1 = new Student("Riya", 15);
        Student s2 = new Student("Aman", 16);

        s1.display();
        s2.display();
    }
}
```

Arguments are passed into the constructor to initialize each object differently.

## 4. The `this` keyword

`this` refers to the current object. It is often used when a parameter has the same name as an instance variable.

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

- `this.name` means the object's instance variable.
- `name` on the right side means the constructor parameter.
- `this.age` means the object's instance variable.
- `age` on the right side means the parameter.

## 5. Variable shadowing

A parameter or local variable can have the same name as an instance variable. The local name shadows the field within that scope.

```java
class Box {
    int size;

    Box(int size) {
        this.size = size;
    }
}
```

Without `this`, `size = size;` would assign the parameter to itself and leave the instance field unchanged.

## 6. Constructor overloading

A class can have multiple constructors with different parameter lists.

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

Java chooses the constructor that matches the arguments supplied to `new Book(...)`.

## Practice questions

1. Create a `Student` class with a no-argument constructor.
2. Create a `Student` class with a parameterized constructor for name and age.
3. Use `this` to assign parameters to same-named instance variables.
4. Create a `Book` class with title and price and initialize them using a constructor.
5. Create a `Rectangle` class whose constructor takes length and breadth.
6. Add two constructors to a `Circle` class: one with a default radius and one with a supplied radius.
7. Create an `Employee` class with name and salary and display the data.
8. Explain the difference between a constructor and a method.
9. Explain the difference between a compiler-provided default constructor and a programmer-written no-argument constructor.
10. Create two objects with different constructor arguments and show that their fields differ.
11. Overload a `Box` constructor to accept one value for all dimensions or three separate dimensions.
12. Identify and fix a program where `name = name;` fails to set the instance field.

<details>
<summary>Hints</summary>

- **Tip 1:** A constructor has the same name as the class and no return type.
- **Tip 2:** Use parameters to provide values when the object is created.
- **Tip 3:** Use `this.fieldName = parameterName` when the names are the same.
</details>

## Common mistakes

- Giving a constructor a return type such as `void`.
- Naming the constructor differently from the class.
- Assuming a default constructor is still supplied after declaring another constructor. It is not.
- Forgetting `this` when a parameter shadows an instance field.
- Trying to return a value from a constructor.

## Checklist

- [ ] I can write a no-argument constructor.
- [ ] I can write a parameterized constructor.
- [ ] I understand `this`.
- [ ] I can overload constructors.

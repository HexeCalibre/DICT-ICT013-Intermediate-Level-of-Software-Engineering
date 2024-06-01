# Overview

Welcome to the Intermediate Software Engineering course!

This week, we will discuss the pointers to check in your projects such as comments, naming, and formatting. We will also discuss how you can apply design patterns in your code structure.

At the end of this week, you will be able to improve the readability of your code and the code structure by applying design patterns.

---

## Software Design Patterns

programming language independent strategies general reusable solution for the common problems

### The Gang of Four

The Gang of Four (GoF) Design Patterns, introduced in the book “Design Patterns: Elements of Reusable Object-Oriented Software,” authored by Erich Gamma, Richard Helm, Ralph Johnson, and John Vlissides, provide a catalog of proven solutions to common design problems in software development. The GoF Design Patterns encourage best practices, code reusability, and the separation of concerns, aiding in the development of robust and scalable applications.

[To read more about GoF, click this link](https://www.geeksforgeeks.org/gang-of-four-gof-design-patterns/)

### Types of Design Patterns

- **Creational:**
  - Concerned with the way in which objects are created
  - Reduce complexities and instability by creating objects
  - Used when a decision must be made at the time of instantiation of a class
  - **Types of Creational Design Pattern:**
    - Singleton
    - Factory Method
    - Abstact Factory
    - Builder
  - **When to use Singleton Pattern**
    - define a class that has only one instance
    - provides a global point of access
    - Resources that are expensive to create
    - For classes which provides access to configuration settings
```java
public class Singleton {
    private Singleton (){}

    private statc class SingletonMolder {
        public static final Singleton instance = new Singleton();
    }

    public static Singleton getInstance(){
        return SingletonMolder.instance;
    }
}
```
> **Note:** If you implement Singleton Design Pattern, make sure you understand the runtime implications. Also Create Diagrams.
>
> A solution to solve some problems
> It is the same for all the design patterns.
- Structural
- Behavioral

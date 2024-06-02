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

---

## Types of Design Patterns

### Creational:
- Concerned with the way in which objects are created
- Reduce complexities and instability by creating objects
- Used when a decision must be made at the time of instantiation of a class

#### Types of Creational Design Pattern:
- Singleton
- Factory Method
- Abstact Factory
- Builder

##### When to use Singleton Pattern?
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

--- 
### Structural
- Assemble objects and classes into larger structures
- Identifying a simple way to realize relationships between entities

#### Types of Structural Design Pattern:
- Adapter
- Bridge
- Tree
  
##### When to use Adapter Pattern?
- incompatible interfaces
```java
interface Bird
{
    public void fiy();

    public void makeSound();
}

class Sparrow implements Bird {
    @Override
    public void fiy() {
        System.out.println("Flying");
    }

    @Override
    public void makeSound() {
        System.out.println("Chirp Chirp");
    }
}

interface ToyDuck {
    public void squeak();
}

class PlasticToyDuck implements ToyDuck {
    public void squeak() {
        System.out.println("Squeak");
    }
}

class BirdAdapter implements ToyDuck {
    Bird bird;

    public BirdAdapter(Bird bird) {
        this.bird = bird;
    }

    @Override
    public void squeak() {
        bird.makeSound();
    }
}

class Main
{
    public static void main (String args[])
    {
        Sparrow sparrow = new Sparrow();
        // Wrap a bird in a birdAdapter so that it
        // behaves like toy duck

        // toy duck behaving like a bird
        System.out.println("BirdAdapter...");
        birdAdapter.squeak();
    }
}
```

### Behavioral
- Identify common communication patterns between objects

#### Types of Creational Design Pattern:
- Chain of Responsibility
- Command
- Iterator
- Memento
- Mediator
- Observer

##### When to use Chain of Responsibility Pattern?
- Pattern consists of a source of command objects and a series of processing objects
- handy for decoupling a sender and receiver of a command
- picking a processing strategy at processing-time
- To implement a common interface
- To delegate on to the next one if appropriate
- standardize what are already accepted as best practices
- a well-factored implementation

```java
interface ChainOfResponsibility {
    void perform();
}

class LoggingChain {
    private ChainOfResponsibility delegate;

    public void perform() {
        System.out.println("Starting chain");
        // validate input parameters
        // before delegate
        delegate.perform();
        System.out.println("Ending chain");
    }
}
```
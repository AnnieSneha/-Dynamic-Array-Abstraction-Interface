# -Dynamic-Array-Abstraction-Interface

### Abstraction

1. **Abstract Class**: An abstract class is a class that cannot be instantiated on its own and may contain abstract methods (methods without a body) as well as concrete methods (methods with a body). It provides a base for subclasses to extend and implement the abstract methods.

2. **Interface**: An interface is a reference type in Java, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types. Interfaces cannot contain instance fields. The methods in interfaces are abstract by default. Interfaces are used to achieve complete abstraction and multiple inheritance.

### Multiple Inheritance Using Interfaces

Java does not support multiple inheritance with classes to avoid the complexity and ambiguity of inheriting from multiple classes (the "diamond problem"). However, Java allows a class to implement multiple interfaces, which is a form of multiple inheritance.

Here’s an example to illustrate abstraction and multiple inheritance using interfaces:

```java
// Define an interface for flying behavior
interface Flyable {
    void fly();
}

// Define an interface for swimming behavior
interface Swimmable {
    void swim();
}

// Implementing both interfaces in the class Duck
class Duck implements Flyable, Swimmable {
    @Override
    public void fly() {
        System.out.println("The duck flies in the sky.");
    }

    @Override
    public void swim() {
        System.out.println("The duck swims in the water.");
    }
}

// Main class to test the implementation
public class Main {
    public static void main(String[] args) {
        Duck duck = new Duck();
        duck.fly();   // Output: The duck flies in the sky.
        duck.swim();  // Output: The duck swims in the water.
    }
}
```


- **Interfaces `Flyable` and `Swimmable`**: Both interfaces define a contract with abstract methods `fly()` and `swim()`, respectively.

- **Class `Duck`**: This class implements both `Flyable` and `Swimmable` interfaces. It provides concrete implementations for the `fly()` and `swim()` methods.

- **Multiple Inheritance**: The `Duck` class inherits behavior from both interfaces, achieving multiple inheritance.

By using interfaces, Java allows you to create classes that have behaviors from multiple sources, promoting a flexible and modular design.

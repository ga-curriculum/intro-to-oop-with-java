<h1>
  <span class="headline">Intro to OOP with Java</span>
  <span class="subhead">OOP with Java</span>
</h1>

**Learning objective:** By the end of this lesson, you'll be able to describe how Classes are used to implement object-oriented programming principles of encapsulation, abstraction, inheritance and polymorphism in Java.

## An introduction to classes in Java
In the real-world, if we want to create an object like a clock, we first create a blueprint or a schematic on a paper. This blueprint describes the positions, names and workings of:
- All the other objects that going to be a part of the clock, and their characteristics (gears, springs, clock hands, their shapes and material, etc.)
- All the tasks that can be done by the clock (both visible tasks like moving hands and invisible tasks like rotating of gears)
- All the interfaces provided to interact with it (a crown, for users to move the hands and set a time)

This blueprint, along with all the required materials, if given to a clockmaker, an object called a clock gets made.

In objected-oriented programming languages like Java, a **class** is the blueprint for creating an object. It defines the members (variables and methods) of an object. Classes are thematically grouped together as **Java Packages**.

```
Java Package
  (contains) Java Class
    (contains) Class members
```

## Defining a class
Syntax to define a class: 
```java
public class MyClass {
    // statement block containing variable and method definitions
}
```
- The optional access modifier `public` means that `MyClass` can be instantiated into an object by code inside any class contained in to any package. When not used (default), it means that `MyClass` can be instantiated into an object only by code inside a class contained in the same package. Default and `public` are the only possible access modifiers for a class.
- `class` keyword declares that `MyClass` is a class entity.


## Implementing encapsulation in Java
Java classes implement encapsulation using the following rules:
1. All the members an object, created from this class, needs to be endowed with must be declared and described within the statement block of the class.
2. The accessibility of all the members contained in an object created from this class, must be declared using the following access modifier keywords:
    - `private` : Private members can be accessessed/used by code only within the same class. When objects are created from this class, naturally private members will not be accessible by objects created from other classes.
    - `protected` : Protected members can be accessessed/used only by code within the same class, within a class existing in the same package or within a child class that is inherited from our current class. 
    - `public` : Public members can be accessessed/used by code inside the any class.
    - default : When none of the above three access modifiers are used while defining a member inside a class, such members can be accessed/used by code within the same class or within a class existing in the same package.

Demonstration:
```java
class Account {
    private double balance; // Private data

    // Public method to access private data
    public double getBalance() {
        return balance;
    }
    // Public method to manipulate private data
    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
        }
    }
}
```

## Implementing abstraction in Java
By proper usage of access modifiers, abstraction is automatically implemented. In the above example, the variable `balance` is a private variable whereas the method `deposit` which updates the value of `balance` is a public method. Still, any other object can increase the `balance` value by 100, by making a method call as `<objectName>.deposit(100)`. 

The calling object need not worry about all the tasks that the `deposit` method needs to perform and all the variables it needs to manipulate to perform those tasks.

## Implementing inheritance in Java
In Java, the `extends` keyword is used to indicate inheritance between classes. It allows a **child** class ( **subclass** in Java terminology) to inherit fields and methods from a **parent** class (**superclass** in Java terminology). The only things that needs to be coded in subclass are the additional members that need to be added on top of the existing superclass members. Inheritance promotes code reuse and modularity. 

Syntax:
```java
class ParentClass {
    // Fields and methods
}

class ChildClass extends ParentClass {
    // Additional fields and methods for the subclass
}
```

## Implementing polymorphism in Java
Polymorphism allows the same method or operator to behave differently based on the context. Polymorphism can be implemented in Java using two techniques called **method overloading** and **method overriding**.

### Method overloading
Method overloading occurs when two or more methods in the same class have the **same name** but **different parameter lists** (number, type, or order of parameters).

Example:
```java
class Calculator {
    int add(int a, int b) { // Overloaded method
        return a + b;
    }
    double add(double a, double b) {
        return a + b;
    }
}
```

### Method overriding
Method overriding occurs when a subclass provides a specific implementation of a method that is already defined in its superclass. The overridden method in the subclass must have the **same name, parameters, and return type** as the method in the superclass.

Example:
```java
class Vehicle {
    void move() {
        System.out.println("Vehicle is moving");
    }
}
class Car extends Vehicle {
    @Override
    void move() {
        System.out.println("Car is driving");
    }
}
public class Main {
    public static void main(String[] args) {
        Vehicle v1 = new Vehicle()
        Vehicle v2 = new Car();
        v1.move(); // Calls Vehicle's move() method
        v2.move(); // Calls Car's move() method
    }
}
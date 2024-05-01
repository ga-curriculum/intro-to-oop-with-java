# ![[tktk Module Name] - tktk Microlesson Name](./assets/classes-and-modifiers.png)

**Learning objective:** By the end of this lesson, students will be able to explain how classes and objects factor into object-oriented programming.

## Classes and Modifiers (10 min)

Before object-oriented programming came along, programming languages like C sported a feature called `struct` — a way of defining a common format to allocate blocks of consistent data types.
 
For example:

```java
struct Person { 
    double birthdate;
    int id; 
    char name[50];
} 
```

That would basically allow you to carve out memory for all of the structure's variables (e.g., `birthdate`, `id`, `name`) simply by assigning a new `struct`.

Now that we have data as a `struct`, why not add **functionality** to that structure (e.g., derive a person's age given today's date) and include that functionality inside the `struct` itself? That's exactly what a **class** is — a data structure with functions or methods.

> In our example of deriving a person's age given today's date, we might create a method called `getCurrentAge()` or something similar.

### Defining a Class

We've already seen several examples of classes. They all conform to this common pattern:

```java
public class MyClass {
    // guts of the class
}
```

In this example, `public` refers to the class visibility. Top-level classes can only be `public` or default (unspecified). "Top level" means they're not inner classes, which we'll define later in this lesson.

`public` classes can be referenced by any other class, and this is the most common class visibility. A file may contain **no more than one** `public` class. The rule is that every top-level `public` Java class must reside in a file that exactly matches the file name (minus the `.java` file type). 

#### Default Classes

Default classes don't specify an access modifier. For example:

```java
class MyDefaultClass {}
```

They can be accessed in the current file, as well as by other classes in the same package. For this reason, the default visibility level is called "package" or "package-private."

Package and public are the only access levels available for top-level classes. But as we'll see, inner classes can also be `protected` or `private`.

#### Access Levels

The access levels — going from most to least restrictive — are:

```
private --> package --> protected --> public
```

`private`, `protected`, and `public` are all **access modifiers**, which means you specifically add them in so you can change the access (or protection) level away from the default we described above.

This nifty table from [Oracle's docs on access control](https://docs.oracle.com/javase/tutorial/java/javaOO/accesscontrol.html) shows what's unique about each level:

![](https://res.cloudinary.com/briezh/image/upload/v1560810976/Screen_Shot_2019-06-17_at_3.35.38_PM_fq9ffm.png)

----

## Conclusion (5 min)

Object-oriented programming is the practice of using classes and objects to make code modular (encapsulated) and often reusable. A class can be thought of as a blueprint for a building or a pattern for a dress. There's one blueprint, but you can build many buildings with it. There's one dress pattern, but you can manufacture many dresses with it.

> **Knowledge Check**: Can you define each of the four OOP pillars?
> - Abstraction
> - Polymorphism
> - Inheritance
> - Encapsulation
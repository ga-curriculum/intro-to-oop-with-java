# ![[tktk Module Name] - tktk Microlesson Name](./assets/four-principles-of-oop.png)

**Learning objective:** By the end of this lesson, students will be able to cefine the four principles of object-oriented programming.

## Opening (5 min)

**Object-oriented programming** (OOP) is a concept that was first introduced in the 1960s with the advent of the Simula programming language and became popular some 25 years later with C++.

Whereas earlier languages were **procedural** in nature, object-oriented programming introduced the concept of **objects** — compartments of data and functionality that could easily retain and modify their own instance data.

-----

## The Four Principles of OOP (10 min)

The four pillars of object-oriented programming are:

* Abstraction
* Polymorphism
* Inheritance
* Encapsulation

> Why are they ordered like that? Because it spells "A PIE." If you like pie and acronyms, this might help you remember these four concepts!

### Abstraction

The idea behind abstraction is that the average person doesn't need to know the inner workings of something in order to use it successfully. For example, you don't have to be a mechanic to drive a car.

### Encapsulation

Encapsulation is related to abstraction but goes a step further. Not only does the average user not need to have access to the inner workings of something in order to use it, if they do have access, it may actually be harmful.

You could technically start your car with a screwdriver or directly with electricity, but you really shouldn't — you might hurt yourself or damage your car. Likewise, your users don't always need direct access to sensitive parts of your code.

![](https://res.cloudinary.com/briezh/image/upload/v1560812857/bike-brakes_pvfblg.jpg)

> Image credit goes to [this article](https://dev.to/charanrajgolla/beginners-guide---object-oriented-programming), which we highly recommend reading if this course feels a bit too fast paced.

### Inheritance

Inheritance allows classes to "inherit" code from one another. The base class is called the **parent** and the inheritor or beneficiary class is called the **child**. It's just one more way of keeping our code shorter and simpler.

The most frequent use of inheritance is for deriving classes using existing classes, which provides reusability. The existing classes remain unchanged. By promoting reusability in our code, the development time of software is reduced.

### Polymorphism

Polymorphism simply means "many forms." It refers to the fact that a method could have multiple implementations, either differing between a parent and a child class (method overriding) or depending on the type and number of arguments (method overloading).
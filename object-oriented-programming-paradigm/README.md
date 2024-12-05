<h1>
  <span class="headline">Intro to OOP with Java</span>
  <span class="subhead">Object-Oriented Programming Paradigm</span>
</h1>

**Learning objective:** By the end of this lesson, you'll be able to describe the object-oriented programming paradigm

## Why OOP emerged
In the early days of computing, programming was mostly **procedural**. Instructions were written sequentially, with data and logic closely intertwined. While effective for small programs, this method became increasingly unwieldy as software systems grew in size and complexity. Imagine trying to debug or find the root cause of an error in a hospital management system that has more than a million statements of code in a single, massive procedural codebase. Imagine making a change in one line of the code and it results in failure of lot of downsteam statements might fail, and there being no way to predict that because of the size and complexity of the program. Programmers needed a way to organize and simplify their work while still capturing the nuances of real-world problems.

## The Object-Oriented paradigm
The origins of OOP can be traced to the idea of modeling real-world entities in software. Think of a complex system like a human society. It consisits of a large number of individuals, each of them uniquely identifiable by a combination of visible and invisible traits and labels ('states` in programming parlance) and all of them capable of performing acts and exchanging information with each other. With these characteristics, they can work together to bring to life a complex, purpose-oriented and functional entity like a military or a corporation or government.

What if we can think of computer programming like that? We may be able to build some of the most complex computing applications (So many of which exist, in the present day, as testament to the power of OOP).

Object-orient paradigm is a way of designing and writing computer programs by thinking of any software requirement as a problem to solve by a organising the interactions between a number of self-contained entities, called **Objects**, in the most effient and effective way. These objects possess:

- **Properties**: Data values that describe what they are.
- **Methods**: labelled actions that descibe what they can do.

When a task needs to be accomplished, all it takes is identifying the most appropriate object, using its properties, passing the required data to it, and instructing it to perform one of it's method that can accomplish the task. Programming an entire application is, then, viewed as the task of orchestrating such interactions between objects towards a larger purpose. 

## The four pillars of OOP
How can we tell if a programming language is object-oriented or procedural? The answer is that OOP languages demonstrate all the four following characteristics by design, whereas procedural languages do not. Lets look at each of them with a real-world analogy.

### Encapsulation
 In object-oriented programming paradigm, it translates to the restrictions placed by the rules of the language to make data (constants and variables) and behaviours (methods, procedures, subroutines), invisible and inaccessible as independent programming entities. The Data and behaviour definitions are always **encapsulated** (grouped) inside an **object**. They belong to that particular object only and it is the prerogative of this object to make it accessible to other objects. As a real-world analogy think of you wanting to build a table. You will need a carpenter to perform the carpentry tasks. The carpenter has a name, a qualification and a set of carpentry-specific skills. It would be absurd to imagine a set of skills, without a person, building a table. 

### Abstraction
Objects do not expose their internal programmatic complexity of properties and methods to other objects. Instead, they are made visible and accessible to other Objects as simple entities with just interfaces for interactions. Objects also view other objects as what they are and what can they do for me, and not as entities possessing complex programming logics inside them. As a real-world analogy, a driver and an automobile interact with each other using simple techniques to go from point A to point B. They do not expose their internal complexities. Neither do they care about the other's. Both of them interact with each other only using simple points of interactions. It makes the relationship less complicated for both of them.

### Inheritance
Inheritance is the capability of the language to create two objects having this hierarchical relationship called **parent-child**. A child object will have all the characteristics of a parent (properties and methods) and, can have some more unique characteristics of their own. This is called inheritance. This parent-child relationship can continue enlessly to for the objects to become more and more evolved. This is just like the biological parent-child relationship in real-life among organisms.

### Polymorphism
Polymorphism comes from the Greek words _poly_ (meaning "many") and _morph_ (meaning "forms"). In object-oriented programming paradigm, it is the capability of a language that allows the object's interfaces to change their behaviour according to the context where they are used. It practical implementation, an objects can perform different tasks and/or provide different outputs based on how the call to that method is made. As a real-world analogy lets think of an object called electrical switch. They can be turned on and turned off. However, they can be made equally capable of switching a light bulb or a fan or a television depending on their placement, and making no change to the structure or functionality of the switch.

## Thinking in an Object-Oriented way
We need not struggle hard to think in an object-oriented way. Its the way the natural way the world works. We know how to do it instinctively. However, as programmers, we need to unlearn the procedural way of thinking that we've learnt from working with early and procedural languages like C, COBOL, Pascal, etc.

|Feature|Procedural paradigm|Object-Oriented paradigm|
|:---|:---|:---|
|**Data handling**| Data and logic are individual entities capable of existing independently.| Data and logic are always encapsulated into a single entity and that entity is represented as an object.|
|**Code reuse**| Reusable at the level of functions.|Reusable at the level of objects through inheritance and polymorphism.|
|**Point of view**| A computer program is a simple sequence of procedures and processes manipulating data values to achieve a purpose.| A computer program is an orchestrated set of interactions between objects to achieve a purpose. There's no limit to the complexity of such orchestration.|

Alan Kay, who was a computer scientist in the 1970s who considered a visionary for championing and popularizing the OOP paradigm said his inspiration came from biology and his fascination with cells as self-contained units of life. He saw objects in programming as analogous to cells — independent yet capable of communicating with one another to form complex systems. He created a language, called Smalltalk, that embodied the four pillars of OOP. Smalltalk’s groundbreaking design principles influenced the development of modern OOP languages like Java, C++, and Python.
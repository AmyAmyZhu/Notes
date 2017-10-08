# Introduction to Objects

### The progress of abstraction

program : a collection of statements (recall compiler)

OOP: 
- using computer as an expressive medium
- represent elements ("objects") in the problem space
- characteristics:
  1. Everything is an object
  2. A program is a bunch of objects telling each other what to by sending messages
  3. Each object has its own memory made up of other objects
  4. Every object has a type
  5. All objects of a particular type can receive the same messages
 
### An object has an interface

keyword __class__: abstract date types(ADT), the type of variables

interface: each object can satisfy only certain requests

Unified Modeling Language(UML): includes data members and methods

### An object provides services

High cohesion(recall cs136), means the designing of objects should focus on the same functionality or goals.

Low coupling: the dependency of each classes should be low. A bad example is A requires B, B requires C.

### The hidden implementation

access specifiers keywords: __public, private, protected

package access: classes can access the members of other classes in the same package, but outside of the package those same members appear to be private

### Reusing the implementation

composition: "has-a" relationship, for example, "a car has an engine"

aggregation: composition happens dynamically(has the entire reference of another object), also "has-a". It is used more often than composition.

### Inheritance

override: having two methods with the same method name and parameters (i.e., method signature). One of the methods is in the parent class and the other is in the child class.

overload: when two or more methods in one class have the same method name but different parameters.

"is-a" vs "islike-a"

### Interchangeable objects with polymorphism

early binding: compile time binding(find the address of functions firstly)

late/dynamic binding: runtime binding(after compile, express the statement and find the function, recall cs444)

C++ keyword __virtual__ means make a method to have the flexibility of latebinding

upcasting: casting up to find the parent class methods, safe

downcasting: casting down to find the children class methods, dangerous, need to handle exceptions

### The singly rooted hierarchy

garbage collector

### Containers

List: 
  - ArrayList: randomly accessing is constant-time; Insert an element is expensive
  - LinkedList: randomly accessing is expensive; Insert an element is constant-time

Map, Set

Parameterized types (generics): a class that the compiler can automatically customize to work with particular types

```
ArrayList<Shape> shapes = new ArrayList<Shape>();
```

### Object creation & lifetime

1. place the objects in the stack, maximum runtime speed but restrictive
2. place the objects in the heap dynamically

Java uses dynamic meomory allocation: __new__ operator

C++ must determine programmatically when to destroy the object, which can lead to memory leaks; Java provides garbage collector

### Exception handling: dealing with errors

An exception is an object that is "thrown" from the site of the error and can be "caught" by an appropriate exception handler

### Java and the Internet

#### client/server computing

Problems:
- desginer "balances" the layout of data into tables for optimal use
- ensure one client's new data doesn't walk over another client's new data
- built, debugged, and installed client software
- small delay can be critical

#### Client-side programming

HTML: text-entry boxes, check boxes, radio boxes, lists and dropdown lists and button

cgi-bin: an action to run a program located on the server in a directory

#### Scripting languages

can solve 80% pof the client-side programming problems

#### Java

Applet: a mini-program that will run only under a Web browser. When it is activated, it executes a program.

JVM (java virtual machine): the software platform on which Java programs execute
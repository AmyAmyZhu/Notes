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

## Reusing the implementation

composition: "has-a" relationship, for example, "a car has an engine"

aggregation: composition happens dynamically(has the entire reference of another object), also "has-a". It is used more often than composition.

### Inheritance

override: having two methods with the same method name and parameters (i.e., method signature). One of the methods is in the parent class and the other is in the child class.

overload: when two or more methods in one class have the same method name but different parameters.

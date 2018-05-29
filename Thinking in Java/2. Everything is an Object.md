# Everything is an Object

### You manipulate objects with references

Reference not connect to an object:

```
String s;
```
A safe initilazition for reference:

```
String s = "abcd";
String s = new String("abcd");
```

### You must create all the objects

keyword __new__: make a new object

#### Where storage lives

five different places to store data:
1. Registers: fastest, inside the prcessor; limited and no direct control
2. The stack: RAM, direct support from the processor via its stack pointer, fast; limit on the flexibility
3. The heap: RAM, great flexibility; more time to allocate and clean up
4. Constant storage: program code and ROM (embedded system)
5. Non-RAM storage: streamed object & persistent objects; lightwegiht persistence like JDBC

#### Special case: primitive types

an "automatic" variable is created that is not a reference, it holds the value directly and it's placed on the stack

High-precision numbers:
- __BigInteger__: arbitrary-precision integers; can accurately represent integral values of any size without losing any information during operations. 
- __BigDecimal__: arbitrary-precision fixed-point numbers

#### Arrays in Java

C/C++: blocks of memory

Java: create an array of references; keyword __null__ (not point to an object, the problem will be reported at run time)

### You never need to destroy an object

#### Scoping

scope is determined by the placement of curly braces {}

#### Scope of objects

memory leak: a programmer forgets to release memory

### Creating new data types: __class__

```
class AtypeName { /* Class body goes here */}
AtypeName a = new AtypeName();
```

#### Fields and methods

fields: data members; an object of any type that you can talk to via its reference/primitive type

default values not apply to local variables

### Methods, arguments, and return values

methods: member functions; it contains name, arguments, return type and the body
```
ReturnType methodName( /* Argument list */ ) {
  /* Method body */
}
objectName.methodName(arg1, arg2, arg3);
```

### Building a Java program

#### Name visibility

To avoid name clashing:
- C++ introduced __namespaces__ keyword
- Java use domain name to guaranttee uniqueness

#### Using other components

__import__ keyword: tells the compiler to bring in a package
```
import java.util.ArrayList;
```

#### The __static__ keyword

__static__ keyword: not tied to any particular object instance of that class 
```
class Incrementable {
  static void increment() {StaticTest.i++; }
}
// call it directly through its class
Incrementable.increment();
// or call through an object
Incrementable sf = new Incrementable();
sf.increment();

```

### Comments and embedded documentation

#### Comment documentation

Javadoc: to look for special comment tags

doclets: Javadoc handlers

#### Syntax

Standalone doc tags: commands that start with an '@' and are placed at the beginning of a comment line

Inline doc tags: appear anywhere with a Javadoc, start with an '@' but are surrounded by curly braces

Javadoc process comment documentation for only __public__ and __protected__ members

### Coding style

Code Conventions for the Java Programming Language: to capitalize the first letter of a class name
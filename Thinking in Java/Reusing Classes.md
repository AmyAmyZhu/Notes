# Reusing Classes

composition: simply create objects of your existing class inside the new class

inheritance: creates a new class as a type of an existing class

### Composition syntax

to make the references initialized:
1. at the point the objects are defined
2. in the constructor for that class
3. lazy initialization: right before you actually need to use the object
4. use instance initialization

### Inheritance syntax

__extends__ keyword: followed by the name of the base class; automatically get all the fields and methods in the base class

### Delegation

place a member object in the class you're building(composition), but at the same time you expose all methods from the member object in your new class(inheritance)

### Combining composition and inheritance

#### Guaranteeing proper cleanup

__try__ keyword: indicates that the block is follows is a _guarded region_, which means that it is given special treatment

__finally__ keyword: always executed

```
try {
    // Code and exception handling...
} finally {
    x.dispose();
}
```

#### Name hiding

redefining a method that is overloaded several times in the derived class wil _not_ hide any of the base-class versions(unlike C++)

### Choosing composition vs. inheritance

Composition is generally used: embed an object so that you can use it to implement features in your new class; has-a relationship

Inheritance: is-a relationship; the new class is a type of the existing class

### protected

__protected__: this is __private__ as far as the class user is concerned, but available to anyone who inherits from this class or anyone else in the same __package__

### Upcasting

Upcasting: casting a subtype to a supertype, upward to the inheritance tree; safe

!"Do I need upcast?": if yes, then necessary to use inheritance

### The final keyword

__final__ keyword: this cannot be changed

want to prevent changes for two reasons:
1. design
2. efficiency

#### final data

a constance is usedful for two reasons:
1. it can be a compile-time constant that won't ever change
2. it can be  a value initialized at run time that you don't want changed

__final__ primitives: compile-time constant

__final__ && __static__ field: one piece of storage that cannot be changed

__final__ object references: it can never be changed to point to another object; however, the object itself can be modified

blank finals: fields that are declared as __final__ but are not given an initialization value; must be initalized before it is used —— perform assignments to __finals__ either with an expression at the point of definition of the field or in every constructor

__final__ arguments: inside the method you cannot change what the argument reference point to

#### final methods

two reasons for __final__ methods:
1. put a "lock" on the method to prevent any inheriting class from changing its meaning(cannot be overriden)
2. efficiency; inline calls

any __private__ methods in a class are implicitly __final__

#### final classses

__final__ class: don't want to inherit from this class or allow anyone else to do so

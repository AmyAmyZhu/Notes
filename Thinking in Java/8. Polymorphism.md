# Polymorphism

changes in your code don't cause damage to parts of the program that should not be affected

polymorphism is an important technique for the programmer to "separate the things that change from the things that stay the same"

### The twist

#### Method-call binding

binding: connect a method call to a method

early binding: binding is performed before the program is run

late binding: the binding occurs at run time, based on the type of object; dynamic binding/runtime binding

all method binding in Java uses late binding unless the method is __static__ or __final__(__private__ methods are implicitly __final__)

#### Extensibility

extensible: can add new functionality by inheriting new data types from the common base class

### Constructors and polymorphism

#### Order of constructor calls

order of constructor calls for a complex object:
1. the storage allocated for the object is initialized to binary zero before anything else happens
2. the base-class constructor is called
3. member initializers are called in the order of declaration
4. the body of the derived-class constructor is called

#### Inheritance and cleanup

when override __dispose()__ in an inherited class, it's important to remember to call the base-class version of __dispose()__

the order of disposal should be the reverse of the order of initialization

#### Behavior of polymorphic methods inside constructors

a good guideline for constructors is, "Do as little as possible to set the object into a good state, and if you can possibly avoid it, don't call any other methods in this class"

The only safe methods to call inside a constructor are those that are __final__ in the base class

### Covariant return types

covariant return types: an overridden method in a derived class can return a type derived class can return a type derived from the type returned by the base-class method

### Designing with inheritance

#### Substitution vs. extension

pure substitution: derived class objects can be perfectly substituted for the base class, and you never need to know any extra information about the subclasses when you're using them

"is-like-a" relationship: the derived class is like the base class —— it has the same fundamental interface —— but it has other features that require additional methods to implement

#### Downcasting and runtime type information

downcast: to retrieve the type information, to move back down the inheritancy hierarchy; unsafe

every cast is checked in Java -> downcast call RTTI (runtime type identification) -> __ClassCastException__
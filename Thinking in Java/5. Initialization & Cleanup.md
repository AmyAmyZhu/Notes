# Initialization & Cleanup

### Guaranteed initialization with the constructor

constructor: a special method automatically called when an object is created; the name of the constructor must match the name of the class exactly

default constructor: a constructor that takes no arguments

### Method overloading

allow the same method name to be used with different argument types

#### Distinguishing overloaded methods

each overloaded method must take a unique list of argument types

#### overloading with primitives

a primitive can be automatically promoted from a smaller type to a larger one

#### overloading on return values

not use return value to distinguish since calling a method for its sie effect

### Defalut constructors

if you define any constructors, the compiler with not synthesize one for you

### The this keyword

__this__ keyword: can be used only inside a non-__static__ method -- produces the reference to the object that the method has been called for

__this__ keyword is used only for those special cases in which you need to expicitly use the reference to the current object

#### Calling constructors from constructors

In a constructor, the __this__ keyword makes an explicit call to the constructor that matches that argument list

#### The meaning of static

__static__ callback: no __this__ for that particular method

cannot call non-__static__ methods from inside __static__ methods

### Cleanup: finalization and garbage collection

garbage collector: release memory allocated with __new__

what if the object allocated "special" memory without using __new__?

__finalize()__: when garbage collector is ready to release the storage, first call __finalize()__; it perform cleanup at the time of garrbage collection

Notes:
1. your objects might not get garbage collected
2. Garbage collection is not destruction 
3. Garbage collection is only about memory

#### What is finalize() for?

native methods: a way to call non-Java code from Java

after C/C++ uses __malloc()__, call __free()__ to release the storage

#### The termination condition

termination condition: use finalize() to detect an object that hasn't been properly cleaned up

__System.gc()__ is used to force finalization

#### How a garbage collector works

reference counting: each object contains a reference counter, and every time a reference is attached to that object, the reference count is increased

！need more reading...

### Constructor initialization

#### static data inilalization

The order of initialization is __static__ first, if they haven't already been initialized by a previous object creation, and then the non-__static__ objects

#### Explicit static initialization

```
public class Spoon {
    static int i;
    static {
        i = 47;
    }
}
```
is executed only once: the first time make an object or that class or the first time access a __static__ member of that class

### Non-static instance initialization

instance initialization: initialize non-__static__ variables for each object

it is executed before constructors

```
public class Mugs {
    Mug mug1;
    Mug mug2;
    {
        mug1 = new Mug(1);
        mug2 = new Mug(2);
    }
}
```

### Array initialization

length of array: array.length

covert array to string: Arrays.toString();

### Enumerated types

```
public enum Spiciness {
    NOT, MILD, MIDIUM, HOT, FLAMING
}
```
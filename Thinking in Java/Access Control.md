# Access Control

refactoring: rewrites working code in order to make it more readable, understandable, and maintainable

access specifiers: allow the library creator to say what is available to the client programmer

the levels of access control from "most access" to "least access": __public__, __protected__, package access, __private__

### package: the library unit

a package contains a group of classes, organized together under a single _namespace_

compilation unit: must have a name ending in __.java__, and inside the compilation unit there can be a __public__ class that must have the same name as the file

```
import java.util.ArrayList;
import java.util.*;
```

#### Creating unique package names

collecting the package files into a single subdirectory sloves two problems:
1. creating unique package names
2. finding those classes that might be buried in a directory structure

#### Using imports to change behavior

conditional compilation: Java is missing that feature from C; allows you to change a witch and get different behavior without changing any other code

Java can change packages imported in order to switch to debug mode

### Java access specifiers

#### Package access

package access: default access

only way to grand access to a member is to:
1. Make the member __public__
2. Give the member package access by leaving off any access specifier, and put the other classes in the same package
3. an inherited class can access a __protected__ member as well as a __public__ member
4. provide "accessor/mutator" methods that read and change the value

### Interface and implementation

Access control is referred to as implementation hiding

encapsulation: wrap data and methods within classes in combination with implementation hiding

the reasons why access control put boundaries within a data type:
1. to establish what the client programmers can and can't use
2. to sparate the interface from the implementation

### Class access

set of constraints:
1. there can be only one __public__ class per compilation unit (file)
2. The name of the __public__ class must exactly match the name of the file containint the compilation unit, including capitalization
3. It is possible to have a compilation unit with no __public__ class at all

two choices for class access:
1. package access
2. __public__
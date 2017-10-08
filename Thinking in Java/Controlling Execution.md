# Controlling Execution

### ture and false

==, !=

### if-else

```
if(Boolean-expression)
statement
else
statement
```

### Iteration

___while__, __do-while__, __for__

### Foreach synatx

```
for(float x : f) {}
```

### return

unconditional braching: __return__, __break__, __continue__

two purpose of __return__:
1. specifies what value a method will return
2. causes the current method to exit, returning that value 

### break and continue

__break__: quits the loop without executing the rest of the statements in the loop
__continue__: stops the execution of the current iteration and goes back to the beginning of the loop to begin the next iteration

### The infamous "goto"

__goto__: a jump at the source-code level

Java has no __goto__
```
label1:
outer-iteration {
    inner-iteration {
        //...
        break;
        //...
        continue;
        //...
        continue label1;
        //...
        break label1;
    }
}
```

rules:
1. a plain __continue__ goes to the top of the innermost loop and continues
2. a labeled __continue__ goes to the label and reenters the loop right after that label
3. a __break__ "drops out of the bottom" of the loop
4. a labeled __break__ drops out of the bottom of the end of the loop denoted by the label

### switch

__switch__: slection statement
```
switch(integral-selector) {
    case integral-value1 : statement; break;
    case integral-value2 : statement; break;
    case integral-value3 : statement; break;
    //...
    defalut: statement;
}
```
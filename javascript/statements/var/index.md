---
title: 'var'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/z16cackw(v=vs.94).aspx)'
compatibility:
  feature: var
  topic: javascript
readiness: 'Ready to Use'
summary: 'Declares a variable.'
tags:
  - JS_Basic
uri: javascript/statements/var

---
## Summary

Declares a variable.

## Syntax

    var variable = value;

**variable**
:   The name of the variable being declared.

**value**
:   The initial value assigned to the variable.

## Examples

The following examples illustrate the use of the var statement.

``` js
var index;
var name = 'Thomas Jefferson';
var answer = 42,
    counter,
    numpages = 10;
var array = [];
```

## Remarks

Use the `var` statement to declare variables. You can assign values to the variables when you declare them or later in your script.

A variable is declared the first time it appears in your script.

You can declare a variable without using the `var` keyword and assign a value to it. This is known as an implicit declaration, and it is not recommended. An implicit declaration gives the variable global scope. When you declare a variable at the procedure level, though, you typically do not want it to have global scope, because that means other scripts could overwrite it causing your script to break.. To avoid giving the variable global scope, you must use the `var` keyword in your variable declaration.

If you do not initialize your variable in the `var` statement, it is automatically assigned [the JavaScript value `undefined`](/javascript/undefined).

## See also

### Other articles

-   [function Statement](/javascript/statements/function)
-   [new Operator](/javascript/operators/new)
-   [Array Object](/javascript/Array)


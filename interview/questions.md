### Primitive vs non-primitive:

1. Primitive - String, Number, bigInteger, Undefined, Null, Symbol
2. Non-Promotive: Means can store multiple values/Complex values - Object, Array

### Hoisting

     This means that irrespective of where the variables and functions are declared, they are moved on top of the scope. The scope can be both local and global.

Example 1:
```javascript
hoistedVariable = 3;
console.log(hoistedVariable); // outputs 3 even when the variable is declared after it is initialized	
var hoistedVariable;
```
Example 2:
```javascript
hoistedFunction();  // Outputs " Hello world! " even when the function is declared after calling

function hoistedFunction(){ 
  console.log(" Hello world! ");
}
```

## Debugger:
The debugger for the browser must be activated in order to debug the code. 
Built-in debuggers may be switched on and off, requiring the user to report faults. 
The remaining section of the code should stop execution before moving on to the next line while debugging.

## Difference between “ == “ and “ === “ operators.

```javascript
var x = 2;
var y = "2";
(x == y)  // Returns true since the value of both x and y is the same
(x === y) // Returns false since the typeof x is "number" and typeof y is "string"
```

## difference b/w var and let:
- var is used long before from begining
- let introduced 2015
- let is scoped
- var is function scope
- let and const not hoisted

## Implicit Type Coercion in javascript.
Implicit type coercion in javascript is the automatic conversion of value from one data type to another. It takes place when the operands of an expression are of different data types.

String coercion
String coercion takes place while using the ‘ + ‘ operator. When a number is added to a string, the number type is always converted to the string type.

Example 1:
```javascript
var x = 3;
var y = "3";
x + y // Returns "33"
```
Example 2:
```javascript
var x = 24;
var y = "Hello";
x + y   // Returns "24Hello";
```
Note - ‘ + ‘ operator when used to add two numbers, outputs a number. The same ‘ + ‘ operator when used to add two strings, outputs the concatenated string:
```javascript
var name = "Vivek";
var surname = " Bisht";
name + surname     // Returns "Vivek Bisht"
```
Note - Type coercion also takes place when using the ‘ - ‘ operator, but the difference while using ‘ - ‘ operator is that, a string is converted to a number and then subtraction takes place.
```javascript
var x = 3;
Var y = "3";
x - y    //Returns 0 since the variable y (string type) is converted to a number type
```

OR ( | | ) operator - If the first value is truthy, then the first value is returned. Otherwise, always the second value gets returned.

AND ( && ) operator - If both the values are truthy, always the second value is returned. If the first value is falsy then the first value is returned or if the second value is falsy then the second value is returned.

Example:
```javascript
var x = 220;
var y = "Hello";
var z = undefined;
        
x | | y    // Returns 220 since the first value is truthy
        
x | | z   // Returns 220 since the first value is truthy
        
x && y    // Returns "Hello" since both the values are truthy
        
y && z   // Returns undefined since the second value is falsy
        
if( x && y ){ 
  console.log("Code runs" ); // This block runs because x && y returns "Hello" (Truthy)
}   
        
if( x || z ){
  console.log("Code runs");  // This block runs because x || y returns 220(Truthy)
}

```

## Is javascript a statically typed or a dynamically typed language?
<img width="665" height="347" alt="image" src="https://github.com/user-attachments/assets/4881a1ed-7e45-4e26-a0d4-1b9810ecda26" />

## NaN:
Not a Number -->
```javascript
isNaN("Hello")  // Returns true
isNaN(345)   // Returns false
isNaN('1')  // Returns false, since '1' is converted to Number type which results in 0 ( a number) 
isNaN(true) // Returns false, since true converted to Number type results in 1 ( a number)
isNaN(false) // Returns false
isNaN(undefined) // Returns true
```

## Explain passed by value and passed by reference.
```javascript
var y = #8454; // y pointing to address of the value 234

var z = y; 
     
var z = #5411; // z pointing to a completely new address of the value 234
     
// Changing the value of y
y = 23;
console.log(z);  // Returns 234, since z points to a new address in the memory so changes in y will not effect z
```
## What is an Immediately Invoked Function in JavaScript?
(function(){ 
  // Do something;
})();

## javascript strict-mode?

In 'Strict mode,' however, all forms of errors, including silent errors, will be thrown. As a result, debugging becomes a lot simpler.  Thus programmer's chances of making an error are lowered.

Characteristics of strict mode in javascript

- Duplicate arguments are not allowed by developers.
- In strict mode, you won't be able to use the JavaScript keyword as a parameter or function name.
- The 'use strict' keyword is used to define strict mode at the start of the script. Strict mode is supported by all browsers.
- Engineers will not be allowed to create global variables in 'Strict Mode

## 

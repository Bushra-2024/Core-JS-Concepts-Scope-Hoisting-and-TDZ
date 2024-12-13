# Core-JS-Concepts-Scope-Hoisting-and-TDZ
### JavaScript Scope  
Scope defines where variables are accessible in your code. JavaScript has three main types of scope:  

## Before you start reading about types first look at the picture, then read the information here. You'll have a better understanding.

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*I5kTkljF6GIVc56lVccjAw.png">

1. **Global Scope**  
   - Variables declared outside any function or block.  
   - Accessible from anywhere in the program.
     Example :
     ```
     let name = "xyz"
     function changeName() {
     name = "abc"               
     }
     changeName();
     console.log(name);             // abc
     ```
     In the above example, we assign the global “name” variable a new value in function changeName() and it will override the existing value of the variable.

2. **Local Scope**  
   - Variables declared inside a specific function or block.  
   - Further divided into:  
     - **Function Scope**: Whenever you create a new function, a new scope is created. Each function has its own scope, therefore when you declare a `variable` in a function, you can 
      access this variable only within that function and its nested(inner) functions. You cannot access this variable outside of the function.
     - **Block Scope**: we can declare local scope in block statements like for loop, if statement etc. Variables declared with `let` or `const` are limited to the block `{}` where they 
     are defined.  

3. **Module Scope**  
   - Variables declared inside a module are only accessible within that module unless exported.  
   - Helps prevent global namespace pollution in modular code.  



# Hoisting in JavaScript

Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their containing scope during the compile phase before code execution. This means that variables and functions can be used before they are declared, but the behavior depends on how they are declared.

## Variable Hoisting

When a variable is declared using `var`, it is hoisted to the top of its scope, but only its declaration, not its assignment. This means that if you try to use the variable before it’s initialized, its value will be `undefined`.

Example:

```javascript
console.log(x); // undefined
var x = 5;
console.log(x); // 5
```
## Function Hoisting


Function declarations are hoisted completely, meaning the entire function (including its body) is moved to the top of its scope. This allows you to call the function before its actual declaration in the code.

```
 hello(); // "Hello, world!"
function hello() {
    console.log("Hello, world!");
}
```

# Temporal Dead Zone (TDZ) in JavaScript

The Temporal Dead Zone (TDZ) refers to the period between the creation of a variable (due to `let` or `const` hoisting) and the actual declaration in the code. During this time, the variable is in an uninitialized state and cannot be accessed, resulting in a `ReferenceError` if attempted.

## What is the TDZ?

When you declare a variable using `let` or `const`, it is hoisted to the top of its block scope, but it cannot be accessed until the execution reaches the line where the variable is declared and initialized. Accessing it before this point leads to a `ReferenceError` because the variable is in the "dead zone."

### Example of TDZ with `let`:

```javascript
console.log(x); 
let x = 5;

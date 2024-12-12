# Core-JS-Concepts-Scope-Hoisting-and-TDZ
### JavaScript Scope  
Scope defines where variables are accessible in your code. JavaScript has three main types of scope:  

1. **Global Scope**  
   - Variables declared outside any function or block.  
   - Accessible from anywhere in the program.  

2. **Local Scope**  
   - Variables declared inside a specific function or block.  
   - Further divided into:  
     - **Function Scope**: Variables declared with `var` inside a function are accessible only within that function.  
     - **Block Scope**: Variables declared with `let` or `const` are limited to the block `{}` where they are defined.  

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

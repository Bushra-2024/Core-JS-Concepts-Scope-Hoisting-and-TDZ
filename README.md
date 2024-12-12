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


### Understanding JavaScript Scope with Examples  

Scope in JavaScript defines the visibility and accessibility of variables. The following illustrates the three main types of scope:  

![JavaScript Scope Schema](https://soshace.com/wp-content/uploads/2023/04/scope-schema-879.png)  

---

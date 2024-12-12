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


<img src="https://images.ctfassets.net/pzhspng2mvip/1d5LNFu1ftEWvcMipQd1GN/0e857b697ae5145af31467e30749586a/2-scope-chain.png">

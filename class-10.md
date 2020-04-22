# Ch 10 JavaScript Book - Error Handling and Debugging (pg. 450-486)
- Every code has bugs at first!
- It is important to understand the order of execution in the script to better pinpoint exactly where a problem might be occuring
- JS interpreter uses 3 execution contexts
    1. Global Context -> deals w/ global scope
    1. Function context -> deals w/ local scope
    1. Eval context -> not covered in this book

- The stack refers to the order of operations when the code gets to a statement that requires data from another function (454-455)
- Function declarations (also known as named functions) can be accessed anywhere in the code
    - ex. function area (width, height) {
        return width * height
    }
- Function expressions (or anonymous functions) work a little differently in that they cannot be called before the interpreter has discovered it (so why would you use this format?)
    - ex. var area = function (width, height){
        return width * height;
    };
- So each time a script enters a new execution context, 2 phases occur 
    1. Prepare - new scope is created, variables, functions, and arguments are created
    1. Execute - now it can assign value to variables. Reference functions and run their code, execute statements.
- Children can get info from parents but parents can NOT get info from children
- If a statement generates an error, it throws an EXCEPTION
- 7 types of errors (error objects):
    1. Syntax error
    1. Eval error
    1. reference error
    1. URI error
    1. type error
    1. range error
    1. error (general)
- Using breakpoints in the console can help... you can manually insert a breakpoint in javascript w/ the debugger; line
- If you know your code might fail, use 'try,' 'catch,' and 'finally.'
- You can throw an error into your code on purpose fore some strange reason...
    - ex. throw new error('message');
- Practical debugging tips
    - Try another browser
    - add numbers
    - strip it back
    - explaining the code
    - search aka GOOGLE!
    - code playgrounds
    - Validation tools (like jslint!)
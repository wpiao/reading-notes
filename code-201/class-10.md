# Read: 10 - JS Debugging - 2/9/2021  

- Execution contexts  
  1. Global context - only one global context in any page
  2. Function context - each function has its own function context
  3. Eval context
- Variable scope  
  1. Global scope - can be used anywhere
  2. Function-level scope - can only be used within the function
- The stack - when a statement needs data from another function, it stacks the new function on top of the current task
- Execution context
  1. Prepare - new scope, variables, functions, and arguments are created. The value of the this keyword is determined.
  2. Execute - assign values to variables, reference functions and run their code, execute statements.
- Error Objects - help you find where your mistakes are and browsers have tools to help you read them.
- How to deal with errors
  1. Debug the script to fix errors
  2. Handle errors gracefully
- A debugging workflow
  1. Where is the problem?
      1. Look at the error message
      2. Check how far the script is running
      3. Use breakpoints where things are going wrong
  2. What exactly is the problem?
      1. When you have set breakpoints, you can see if the variables around them have the values you would expect them to. If not, look earlier in the script.
      2. Break down / break out parts of the code to test smaller pieces of the functionality.
      3. Check the number of parameters for a function, or the number of items in an array.
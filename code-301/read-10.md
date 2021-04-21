# Read: 10 - In memory storage - 4/20/2021

## JavaScript Call Stack

The JavaScript engine (which is found in a hosting environment like the browser), is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.
The call stack is primarily used for function invocation (call). A call stack is a data structure that uses that Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call). The call stack is synchronous. In Asynchronous JavaScript, we have a callback function, an event loop, and a task queue.

Summary:

1. It is single-threaded. Meaning it can only do one thing at a time.
2. Code execution is synchronous.
3. A function invocation creates a stack frame that occupies a temporary memory.
4. It works as a LIFO - Last In, First Out data structure.

## JS Error message

1. Type of error messages
   - Reference errors
   - Syntax errors
   - Range errors
   - Type errors
2. Tools to avoid runtime errors
   - quokka to evaluate your code as you type
   - eslint to make sure your style guide is consistent and it will grab you an error or two along the way
   - TypeScript

## References

[JavaScript errors reference on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)

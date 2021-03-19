# Journal-06 - 1/27/2021

I learned JS object literals and Document Object Model (DOM). We went over creating objects, adding properties or methods to an object, and DOM manipulations. Lab-06 went very well and I didn't have any difficulties when I did it.

## Key takeaways

1. JS Object literals

   - Create an object - `const seattle = {name: 'seattle'}; // key-value pair`
   - Access property:
     - Dot notation - `seattle.name`
     - Square bracket notation - `seattle['name']`
   - Add property - `seattle.state = 'WA'`

2. DOM manipulation

   - Get the target element - `let targetElement = document.getElementById(<id name as string>);`
   - Create the required element - `let requiredElement = document.createElement(<element name as string>);`
   - Give it content - `requiredElement.textContent = <some contents>;`
   - Append to the DOM, append to its parent or directly to the DOM - `targetElement.appendChild(requiredElement);`

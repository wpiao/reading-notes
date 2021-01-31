# Journal-07 - 1/30/2021  

I learned JS constructor function in this lab. I refactored the previous lab code by using it and make my code DRY. One thing need to know about the constructor function is the keyword `this` doesn't refer to the constructor itself, it refers to the object/instance that is created by it. This lab went very well, I didn't have any difficulties and I don't have any questions at this time. 

## Key takeaways  

1. JS constructor function  
  - Example:
    ```javascript
    // Define Student constructor
    const Student = function (name, gender) {
      this.name = name;
      this.gender = gender;
      this.greetings = function () {
        console.log('Hello World');
      };
    };

    // Create an instance by using keyword new 
    const wenhao = new Student('wenhao', 'male');

    // Use prototype to add a property to a constructor
    Student.prototype.anotherGreetings = function () {
      console.log(`Greetings from ${this.name}!`);
    } ;
    ```
  - The first letter of the constructor name should be capitalized
  - Use keyword `new` when calling it
  - Use `prototype` to add a property to a constructor

2. DOM manipulation
   - Get the target element - `let targetElement = document.getElementById(<id name as string>);`
   - Create the required element - `let requiredElement = document.createElement(<element name as string>);`
   - Give it content - `requiredElement.textContent = <some contents>;`
   - Append to the DOM, append to its parent or directly to the DOM - `targetElement.appendChild(requiredElement);`
# Read: 06 - JS Object Literals; The DOM

## JS Object Literals

- JS objects group together a set of variables and functions
- Variables become known as properties in an object
- Functions become known as methods in an object
- JS objects store key-value pairs
- Example:
  ```JavaScript
  const hotel = {
    name: 'Hilton', // property
    rooms: 50, // property
    greetings: function () { // method
      console.log('Hello, World!');
    },
  };
  ```
- Accessing an object
  1. Dot notation - e.g. `hotel.name`
  2. Square brackets - e.g. `hotel['name']`
  3. These two methods are interchangeable in most cases, but sometimes we can only use the square-bracket to access an object.

## The Document Object Model - DOM

- The DOM Specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.
- DOM tree - a model of a web page - stores in the memory - made of objects
- document node - represents the entire page
- Common used DOM queries:
  1. `getElementById(<id value>)` - return one element
  2. `getElementsByClassName(<class name>)` - return Nodelists - similar to arrays
  3. `getElementsByTagName(<tag name>)` - return all elements that have the specified tag name
  4. `querySelector()` - return the first matching element
  5. `querySelectorAll()` - return all matching elements
  6. `parentNode, previousSibling/nextSibling, firstChild/lastChild` - traversing between element nodes

# ES6 Classes - 3/20/2021   

## Constructor function - Prototypal Inheritance  
```javascript
// when methods or properties are attached to object's prototype they become available for use on that object and its descendants, but NOT DIRECTLY ATTACHED to them.
function Animal(name) {
  this.name = name;
}

Animal.prototype.walk = function() { // all animals (Animal instances) can walk
  // code block for implementing the walk function
}

// Bird can do all the things animals can do plus things only Bird can do
function Bird(name) {
  Animal.call(this, name); // I can do all the things animals can do!
}

Bird.prototype.fly = function() { // all birds (Bird instances) can fly
  // code block for implementing the fly function
}

// A new Bird instance
const parrot = new Bird('parrot');
parrot.fly();  // comes with Bird constructor
parrot.walk(); // inherited from Animal constructor
```

## ES6 Classes - more like Java class syntax
```javascript
class Animal {
  constructor(name) {
    this.name = name; // instance variable or field
  }

  // business method
  walk() { // all animals (Animal instances) can walk
    // code block for implementing the walk function
  }
}

class Bird extends Animal { // Bird IS-A Animal, so all birds can do all things animals can
  fly() { // all birds (Bird instances) can fly
    // code block for implementing the fly function
  }
}

// A new Bird instance
const parrot = new Bird('parrot');
parrot.walk(); // from Animal class
parrot.fly();  // from Bird class
```

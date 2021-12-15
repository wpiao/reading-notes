# Read: 04 - Classes and Objects and Recursion - 12/14/2021

## Classes and Objects

- Class is a blueprint/template to create a object
- Object is an instantiation of a class. It gets its variable and functions from a class
- Example:

  ```python
  class Myclass:
    variable = "blah" # instance variable

    def function(self):
      print("This is a message inside the class.")

  # instantiation
  myclass_1 = Myclass()
  myclass_2 = Myclass()
  ```

## Recursion

Recursive function will continue to call itself and repeat its behavior until some condition is met to return a result. All recursive functions share a common structure made up of two parts: base case and recursive case.

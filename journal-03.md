# Journal-03 - 1/16/2021

I learned CSS box model, array, and loop today. An element in HTML is displayed as a box in the web browser. Each box can have a margin, padding, and border. Padding and border are inside of the box, but borer is outside of the box. Block elements such as `<div>, <header>, <main>, <footer>` take the whole width of the window and each block stacks on top of each other. Inline elements such as `<strong>, <span>` are displayed in a line and each element is left or right to each other.<br/>
An Array in JS is a collection of things (could be any data type or mixed) and it is zero-index based. It stores collections of data in a chunk of the memory. Accessing data is very fast since it looks up its index, however, searching data is not efficient if the array is very big because it needs to iterate over its elements from the beginning until it finds it.<br/>
There are two common ways to use loops in JS - For Loop and While Loop. Both loops run code block until the condition is false. Loop is very helpful when you need to iterate over the elements of an array.

## Key findings in Lab-03

1. `prompt()` returns user inputs as string even though user inputs are number.
2. use `break` in the loop when you want to get out of loop immediately so that you don't have to go through rest of the iterations.
3. falsy values in JS - `0, NaN, null, undefined, ''`.

## Summary

### CSS Box Model

- margin - outside of the box
- padding, border - inside of the box
- block elements - take the whole width of the window, each block stack on each other
- inline elements - placed in one line, left to right
- example:
  ```css
  body {
    margin: auto; /* place the element in the center */
    box-sizing: border-box; /* use to include border in box width */
  }
  ```

### JS: Array and Loop

- array - A data structure, a collection of things, zero-index based
  - create an array - `let arrayOne = [1, 2, 3]`
  - access an element - `arrayOne[<index>]`
  - assign a value (5) to an array at index x - `arrayOne[x] = 5`
  - array method length - number of elements in the array
- For loop - Instantiation, conditional statement, increment or decrement
- While loop - if conditional is true then run the code block
- JS falsy values - 0, '', null, undefined, NaN

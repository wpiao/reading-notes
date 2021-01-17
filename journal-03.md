# Journal-03 - 1/16/2021

## CSS Box Model

- margin - outside of the box
- padding, border - inside of the box
- block elements - take the whole width of the window, each block stack on each other
- inline elements - placed in one line, left to right

```css
body {
  margin: auto; /* place the element in the center */
  box-sizing: border-box; /* use to include border in box width */
}
```

## JS: Array and Loop

- array - A data structure, a collection of things, zero-index based
  - create an array - `let arrayOne = [1, 2, 3]`
  - access an element - `arrayOne[<index>]`
  - assign a value (5) to an array at index x - `arrayOne[x] = 5`
  - array method length - number of elements in the array
- For loop - Instantiation, conditional statement, increment or decrement
- While loop - if conditional is true then run the code block
- JS falsy values - 0, '', null, undefined, NaN

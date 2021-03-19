# Reading: 04 - HTML Links, JS Functions, and Intro to CSS Layout - 01/19/2021

## HTML Links

1. Linking to other sites - `<a href="<url>">Other sites</a>`
2. Linking to other pages on the same site = `<a href="<file path>">Other pages</a>`
3. Relative URLs - a shorthand way of telling the browser where to find the files
4. Email links - `<a href="mailto:<email address>">Email me</a>`
5. Opening links in a new window - use `target="_blank"` attribute
6. Linking to a specific part of the same page - use id for href attribute

## CSS Layout

1. Block-level boxes - start on a new line
2. Inline boxes - flow between surrounding text
3. Five positioning schemes - Normal flow, Relative positioning, Absolute positioning, Fixed positioning, and Floating elements
4. Normal flow - browser default, `position: static;`
5. Relative positioning - moves an element in relation to its default position in normal flow, `position: relative;`
6. Absolute positioning - taken out of the normal flow and no longer affects the position of other elements, `position: absolute;`
7. Fixed positioning - positions the element in relation to the browser window, `position: fixed;`
8. z-index - controls which element sits on top when there are overlapping elements. The higher the number the closer that element is to the front.

## JS Functions

1. Function - a series of statements that perform a task helps organize the code. It can be used anytime by calling it.
2. Function declaration and calling a function

```JavaScript
// function declaration
function getArea (width, height) {
  return width * height;
}
// call a function
let area = getArea(3, 5);
```

3. Local variables vs Global variables

- Local variables - cannot be accessed outside of the local scope
- Global variables - can be accessed from anywhere after defined; has potential naming conflicts

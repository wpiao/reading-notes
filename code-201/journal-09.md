# Journal-09 - 2/6/2021 

In lab-09, I created a basic form with 4 inputs and one button. I added an event listener and an event handler to this form so that when users submit the form it will add a row of data in the table and the table footer row will be updated accordingly. When a new row of data is inserted into the table, I have to remove the current table footer row and re-render the footer row. Otherwise, there would be more than one footer row rendered. I don't have any questions about this lab at this time. 

## Key takeaways  

- Event Handling
  - Event: Fired or Raised
  - Code: Triggered
  - Event Types: click, submit, hover/mouseover, on page load, etc.
  - Event Listener: code that is going to trigger when an event is FIRED
  - Bind: bind or tether an event listener to the event
  - Event handler: code that runs in response to the event
- DOM level 2 event handlers
  ```javascript
  element.addEventListener('event', functionName); // format
  myContainer.addEventListener('click', handleClick); // example
  ```
- Event bubbling - this is what we rely on often - we can "listen" in the "main" element and "hear" when the article was clicked
- Callback function: function entered as a parameter of another function/method
- Helper function: a function called inside of a function
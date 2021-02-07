# Journal-09 - 2/6/2021 

Event Handling:

Event: Fired or Raised
Code: Triggered
Event Types:
click - (clicking on boxes ex)
submit - (when a form button clicked)
hover/mouseover
on page load
Event Listener: code that is going to trigger when an event is FIRED
Bind: bind or tether an event listener to the event
Event handler: code that runs in response to event

- DOM level 2 event handlers - Our way - Do this
```javascript
element.addEventListener('event', functionName);

example: myContainer.addEventListener('click', handleClick);
// welcome to Asynchronous code! asynchronous code: code that runs out of order
```

Event bubbling - this is what we rely on foten - we can "listen" in the "main" element and "hear" when the article was clicked

- callback function: function entered as a parameter of Another function/method
- helper function: a function called inside of a function
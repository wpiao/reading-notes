# Read: 09 - Forms and JS Events - 2/6/2021  

## Forms  

- Form usage - Adding text, making choices, submitting forms  
- Form workflow:
  1. Sent user inputs to the server upon clicking submit button.
  2. The server processes the information and may store the information in a database.
  3. The server creates a new page to send back to the browser based on the information received.
- `<form>` - should always carry the action attribute and will usually have a method and id attribute too
- `<input>` - the value of the type attribute determines what kind of input they will be creating
- input type - text, password, radio, checkbox, file, submit, img, date, url, email, search

## JS Events  
- Event handling  
  1. Select the element nodes you want the script to respond to.
  2. Indicate which event on the selected nodes will trigger the response.  
  3. Start the code you want to run when the event occurs.
- Three ways to bind an event to an element 
  1. HTML Event Handlers  - Do Not Use  
  2. Traditional DOM Event Handlers 
  3. DOM Level 2 Event Listeners
# Journal-13 - 2/20/2021  

I learned local storage today. The use of local storage is to store data permanently so that when uses refresh or reset the page, the data still exists. In this lab, I implemented data persistence for the views and votes so that the app can keep track of aggregate number of views and votes. 

- Steps to use local storage  
  1. `Stringify` the data - `JSON.stringify(<some data>);`
  2. Set to local storage - `localStorage.setItem(<key>, <value>);` 
- Steps to retrieve the data from local storage 
  1. Get the target data by key - `localStorage.getItem(<key>);`
  2. Parse the target date - `JSON.parse(<target data>);`

## References 
[Local Storage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage)
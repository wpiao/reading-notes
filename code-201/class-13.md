# Read: 13 - Local Storage - 2/20/2021  

For native applications, the operating system typically provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state. If your native client application needs local storage beyond key/value pairs, you can embed your own database, invent your own file format, or any number of other solutions. 

## Check for HTML5 Storage  
```javascript
function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
}
```

## Using HTML5 Storage  
```javascript
let foo = localStorage.getItem('bar');
localStorage.setItem('bar', foo);

// removing the value for a given named key
interface Storage {
  deleter void removeItem(in DOMString key);
  void clear();
};

// get the total number of values in the storage area
interface Storage {
  readonly attribute unsigned long length;
  getter DOMString key(in unsigned long index);
};
```

## Tracking changes to the HTML5 storage area 
```javascript
if (window.addEventListener) {
  window.addEventListener("storage", handle_storage, false);
} else {
  window.attachEvent("onstorage", handle_storage);
};
```
# Read: 03 - Passing Functions as Props - 3/27/2021 

## Lifting State Up
**Single Source of Truth**-There should be a single "source of truth" for any data that changes in a React application. Usually, the state is first added to the component that needs it for rendering. Then, if other components also need it, you can lift it up to their closest common ancestor. Instead of trying to sync the state between different components, you should rely on the top-down data flow.   

## Lists and Keys   
Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity. Key must only be unique among siblings.   

Example:    
```JavaScript
function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    <ListItem key={number.toString()}
              value={number} />
  );
  return (
    <ul>
      {listItems}
    </ul>
  );
}
```

## References 
[React Lists and Keys](https://reactjs.org/docs/lists-and-keys.html)
[React Lifting State Up](https://reactjs.org/docs/lifting-state-up.html)
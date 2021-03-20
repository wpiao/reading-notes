# Read: 01 - Introduction to React and Components - 3/20/2021 

## What is React? 
React is declarative, efficient, and flexible JavaScript library for building user interfaces. It lets you compose complex UIs from small and isolated pieces of code called "components".    

## JSX  
JSX is a syntax extension to JavaScript and it allows us to write JavaScript with HTML tags. It comes with the full power of JavaScript and it produces React "element".
```JSX
const element = <h1>Hello, world!</h1>;
```

## React sample code  
```JavaScript
// React component
class ShoppingList extends React.Component {
  render() {
    return (
      <div className="shopping-list">
        <h1>Shopping List for {this.props.name}</h1>
        <ul>
          <li>Instagram</li>
          <li>WhatsApp</li>
          <li>Oculus</li>
        </ul>
      </div>
    );
  }
}

// render the component
ReactDOM.render(
  ShoppingList, document.getElementById('root') // render the React component under the element that id is root
);
```

## Resources  
[React Official Docs](https://reactjs.org/tutorial/tutorial.html)

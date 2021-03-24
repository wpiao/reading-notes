# Read: 02 - React State and Props - 3/23/2021  

## State and Lifecycle  
State is similar to props, but it is private and fully controlled by the component and we can use state in a class component.   

```JavaScript
// class component with a state
class Clock extends React.Component {
  constructor(props) {
    super(props);
    this.state = {date: new Date()}; // state
  }

  render() {
    return (
      <div>
        <h1>Hello, world!</h1>
        <h2>It is {this.state.date.toLocaleTimeString()}.</h2>
      </div>
    );
  }
}

// Lifecycle methods
componentDidMount() {...} // it runs after the component output has been rendered to the DOM.

componentWillUnmount() {...} // If the component is ever removed from the DOM, use it.

// correct way to modify a state
this.setState(...);
```

## Handling Events  
```JavaScript
// Recommend use arrow functions inside of class component to aviod binding issues.
class LoggingButton extends React.Component {
  // This syntax ensures `this` is bound within handleClick.
  handleClick = () => { // use arrow function instead of regular funciton
    console.log('this is:', this);
  }

  render() {
    return (
      <button onClick={this.handleClick}>
        Click me
      </button>
    );
  }
}
```

## Conditional Rendering
```JavaScript
function Greeting(props) {
  const isLoggedIn = props.isLoggedIn;
  if (isLoggedIn) { // can change it using setState
    return <UserGreeting />;
  }
  return <GuestGreeting />;
}
```

## Resources
- [State and Lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)
- [Handling Events](https://reactjs.org/docs/handling-events.html)
- [Conditional Rendering](https://reactjs.org/docs/conditional-rendering.html)

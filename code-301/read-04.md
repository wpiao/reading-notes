# Read: 04 - React and Forms - 3/30/2021    

## React Forms  
1. Controlled Components  
In HTML, form elements such as `<input>, <textarea>, and <select>` typically maintain their own state and update it based on user input. In React, mutable state is typically kepy in the state property of components, and only updated with `setState()`. We can combine the two by making the React state be the "single source of truth". Then the React component that renders a form also controls what happens in that form on subsequent user input.    

```JavaScript
// Example: Controlled component
class Form extends React.Component {
  super(props);
  this.state = {value: ''};
}

handleChange = e => {
  this.setState({
    value: e.target.value
  });
}

render() {
  return (
    <form>
      <input type="text" value={this.state.value} onChange={this.handleChange} />
    </form>
  );
}
```

2. Handling Multiple Inputs   
When you need to handle multiple `input` elements, you can add a `name` attribute to each element and let the handler function choose what to do based on the value of `event.target.name`.   

```JavaScript
this.setState({
  [name]: value
});
```

## References   
[React Forms](https://reactjs.org/docs/forms.html)
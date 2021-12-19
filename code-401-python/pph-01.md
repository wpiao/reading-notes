# Partner Power Hour 1 - Class VS Function components in React - 12/18/2021

**Presenter**: Said Hayani

Today's partner power hour presenter was Said Hayani. He was talking about `Class VS Function components in React`. I used `React` before and it is a great and powerful front-end library for web development. It's been a while since I used `React` last time, so this PPH was a great refresh for me. I personally prefer function component because of its simple syntax and use of hooks.

Example:

```javascript
// class component
// import libraries
import React from 'react';

// class component
class App extends React.Component {
  constructor(props) {
    super(props);
    this.state = {};
  }
  async componentDidMount() {
    // fetch data
    // data manipulations with response
  }
  render() {
    return <div>Hello, World</div>;
  }
}

export default App;
```

```javascript
// function component
import React from 'react';

const Myfunction = () => {
  return <div>Hello world</div>;
};
```

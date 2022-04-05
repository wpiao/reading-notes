# Read:37 - React.js and Next.js - 04/05/2022

[Next.js tutorial](https://nextjs.org/learn/basics/create-nextjs-app)  
React's problems:

- Code has to be bundled using a bundler like webpack and transformed using a compiler like Babel.
- You need to do production optimizations such as code splitting.
- You might want to statically pre-render some pages for performance and SEO. You might also want to use server-side rendering or client-side rendering.
- You might have to write some server-side code to connect your React app to your data store.

Next.js: The React Framework

- An intuitive page-based routing system (with support for dynamic routes)
- Pre-rendering, both static generation (SSG) and server-side rendering (SSR) are supported on a per-page basis
- Automatic code splitting for faster page loads
- Client-side routing with optimized prefetching
- Built-in CSS and Sass support, and support for any CSS-in-JS library
- Development environment with Fast Refresh support
  A- PI routes to build API endpoints with Serverless Functions
- Fully extendable

Next.js - The React Framework

- quick spin-up next.js app
  1. `npx create-next-app nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/master/basics/learn-starter"`
  2. `cd nextjs-blog`
  3. `npm run dev`

```javascript
// ES6
// Destructing
var obj = { a: 1, b: 2, c: 3 };
let { a, b, c } = obj;

// Spread syntax
let arr1 = [1, 2, 3];
let arr2 = ['a', 'b', 'c'];
let arr3 = [...arr1, ...arr2];

console.log(arr3); // [1, 2, 3, "a", "b", "c"]

// ES6 classes
class Func {
  constructor(a, b) {
    this.a = a;
    this.b = b;
  }

  getSum() {
    return this.a + this.b;
  }
}

let x = new Func(3, 4);

// import and export
// export.js
let func = (a) => a + a;
let obj = {};
let x = 0;

export { func, obj, x };
// import.js
import { func, obj, x } from './export.js';

console.log(func(3), obj, x);

// React
// class component
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
// function component
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

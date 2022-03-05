# Partner Power Hour 6 - Loops - 03/05/2022

**Presenter**: Kassie Bradshaw

Kassie is a recent code fellows python graduate and she was demonstrating different `Loops` in the javascript.

```javascript
// for...in loops => get the properties
cosnt myObject = {
  school: "codefellows",
  activity: "pph",
  time: "noonish"
}

for (let item in myObject) {
  console.log(item)
}

// for...of loops => can iterate all iterable object, cannot use on object(key, value pair)
for (let item of myObject) {
  console.log(item)
}
```

# Read: 05 - Putting it all together - 4/3/2021   

## Thinking in React  

1. Start With A Mock - JSON data

2. Break The UI Into A Component Hierarchy  
Identity the components and its subcomponents in the mock and give them all names.

3. Build A Static Version in React  
Build a version that takes data model and renders the UI but has no interactivity. It's best to decouple these processes because building a static version requires a lot of typing and no thinking, and adding interactivity requires a lot of thinking and not a lot of typing.

4. Identify The Minimal (but complete) Representation Of UI State 
Figure out the absolute minimal representation of the state the application needs and compute everything else you need on-demand. The key here is DRY.    

5. Identify Where Your State Should Live    
Identify which component mutates, or owns, this state. React is all about one-way data flow down the component hierarchy. It may not be immediately clear which component should own what state.

  - Identify every component that renders something based on that state.
  - Find a common owner component (a single component above all the components that need the state in the hierarchy).
  - Either the common owner or another component higher up in the hierarchy should own the state.
  - If you can't find a component where it makes sense to own the state, create a new component solely for holding the state add add it somewhere in the hierarchy above the common owner component.

6. Add Inverse Data Flow  
Support data flowing the other way.

## Resources    
[Thinking in React](https://reactjs.org/docs/thinking-in-react.html)

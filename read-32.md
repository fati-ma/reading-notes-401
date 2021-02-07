# Readings: Custom Hooks
## Read: 32 - Class 32

### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-32.md).

# Review, Research, and Discussion

## 1. What does a component’s lifecycle refer to?
The time between mounting and unmounting a component.

## 2. Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect
Prevents the recreation of a function

## 3. Why are functional components preferred over class components?
Functional components are just standard JS functions.

## 4. What is wrong with the following code?
```
import React, {useState, useEffect} from 'react';

function MyComponent(props) {
  const [count, setCount] = useState(0);

  function changeCount(e) {
    setCount(e.target.value);
  }

  let renderedItems = []

  for (let i = 0; i < count; i++) {
    useEffect( () => {
      console.log('component mount/update');
    }, [count]);

    renderedItems.push(<div key={i}>Item</div>);
  }

  return (<div>
     <input type='number' value={count} onChange={changeCount}/>
      {renderedItems}
    </div>);
}
```
Answer: Hooks should not be used inside of a loop


# Vocabulary Terms

**state hook** `useState(<initial state>)` used to create a state variable

**effect hook** Allows you to perform side effects, tells react to do something after the render

**reducer hook** Returns the current state paired with a dispatch method


# Preparation Materials
Authoring

- [custom hooks - all you need to know](https://www.telerik.com/kendo-react-ui/react-hooks-guide/#toc-custom-react-hooks)
   - `useEffect` tells react to do something after the render is complete and after every update
   - `useEffect(()=>{document.title = 'You clicked ${count} times'});`
   - Custom hooks are prefixed with the word `use`, normal function but follows the rules of creating a Hook
   
- [async hooks](https://dev.to/vinodchauhan7/react-hooks-with-async-await-1n9g)
   - Offers an example of how to code a fetch request to google books
   - Cannot use `async` keyword with `useEffect` will create race condition
   
- [useReducer Hook](https://reactjs.org/docs/hooks-reference.html#usereducer)
   - Reducer takes in `(state, action)` and returns current state and a dispatch method
   - Preferable when complex state logic or multiple sub-values or when state depends on previous
   
- [react custom hooks](https://reactjs.org/docs/hooks-custom.html)
   - When you want to share logic between two hooks, extract to a third hook
   - name must start with use
   - state inside custom hooks is isolated

Hooks Lists/Collections

- [use hooks](https://usehooks.com/)
- [hooks list](https://github.com/rehooks/awesome-react-hooks)
- [10 essential react hooks](https://blog.bitsrc.io/10-react-custom-hooks-you-should-have-in-your-toolbox-aa27d3f5564d?gi=342012325546)

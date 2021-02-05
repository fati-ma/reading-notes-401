# Readings: Hooks API
## Read: 31 - Class-31
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-31.md).


# Review, Research, and Discussion

## 1. Why do we not need more .html pages in a multi-page React app?
Single page websites cannot always represent complete information

## 2. If we wanted a component to show up on every page, where would we put it and why?
   - Outside the `<BrowserRouter/>`
   - Inside the `<BrowserRouter />`, outside a `<Route />`
   - Inside a `<Route />`
   
## 3. What does props.children contain?
Whatever we include in between the opening and closing tags


# Vocabulary Terms

**Composition** Combining multiple components to achieve a particular goal

**Children / Child Components** Allows you to pass components as data to other components

**Hash Routing** A URL that has a unique application endpoint /app/ controlled by one single back-end action and multiple hashtags managed by JavaScript that define the SPA routes

**Link Routing** The primary way to allow users to navigate around your application


# Preparation Materials

## [making sense of hooks](https://medium.com/@dan_abramov/making-sense-of-react-hooks-fdbde8803889)
- Hooks let you always use functions rather than a mix of functions classes, higher-order components, and render props
- Adding hooks does not introduce any breaking changes
- Hooks don't share state they share stateful logic
- Hooks are a vision of the future of React at FB

## [the state hook](https://reactjs.org/docs/hooks-state.html)
- `import React, { useState } from 'react';`
- Calling useState declares a state variable that does not disappear after the function exits
- useState returns the current state and a function that updates it

## [hooks api](https://reactjs.org/docs/hooks-overview.html)
- Hooks don't work inside classes, but they can replace the need for classes
- Hooks are functions that let you hook into React state and lifecycle features
- `useEffect` runs your effect function after flushing changes to the DOM, runs after every render
- Rules of Hooks
   - Only call hooks at the top level, don't call hooks inside loops, conditions, or nested functions
   - Only call hooks from React function components
   
## [hooks api reference](https://reactjs.org/docs/hooks-reference.html)
- "Bailing out of a state update" if you update a state hook to the same value as the current state, will not render children or firing effects

## [effects hook](https://reactjs.org/docs/hooks-effect.html)
- Effect Hook allows you to perform side effects in function components
- Can pass a second argument to the useEffect() as an array that will prevent unnecessary re-renders

# Readings: Redux - Asynchronous Actions
## Read: 38 - Class 38

### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-38.md).


# Review, Research, and Discussion

## 1. How granular should your reducers be?
In most cases it will probably be beneficial to have a unique reducer for each action so that it be reused in other processes

## 2. Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched
this is probably a con because it would be difficult to make independent changes if necessary

## 3. Name a strategy for preventing the above
eparate out the actions so each calls a specific reducer


# Vocabulary Terms

**store** the top level storage of all state in Redux

**combined reducers** a single reducer that takes in two or more other reducers and returns a single function



# Preparation Materials

## [dan abramov on suspense]()
## [async actions](https://redux.js.org/tutorials/fundamentals/part-6-async-logic)
- Redux middleware enables writing logic with side effects
- Redux `Thunk` middleware allows us to write functions that get `dispatch` and `getState` as arguments
- `$npm install redux-thunk`
- `import thunkMiddleware from 'redux-thunk'`
- `const composedEnhancer = composeWithDevTools(applyMiddleware(thunkMiddleware))`

## [thunk middleware](https://github.com/reduxjs/redux-thunk)
- Allows you to write action creators that return a function instead of an action
- Can be used to delay dispatch or conditionally dispatch
- "The term originated as a humorous past-tense version of 'think'."
- `import { createStore, applyMiddleware } from 'redux';`
## [redux thunk](https://www.digitalocean.com/community/tutorials/redux-redux-thunk)

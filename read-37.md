# Readings: Redux - Combined Redux
## Read: 37 - Class 37

### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-37.md).


# Review, Research, and Discussion

## 1. Why choose Redux instead of the Context API for global state?
Context appears to be the better option when dealing the static data like theme selection while Redux is often better for storing global state data that is more dynamic.
Also Context is used on the level of the component while Redux on the level of the whole lab, right?

## 2. What is the purpose of a reducer?
A function that determines the changes to an applications state, uses the action to determine the change

## 3. What does an action contain?
Actions are the only way to updated data in the store. Must include a type and can pass a payload containing data

## 4. Why do we need to copy the state in a reducer?
Data in the store is immutable, so to make changes a copy must be made in the reducer so that it can be changed


# Vocabulary Terms

**immutable state** state that cannot be changed

**time travel in redux** Redux dev tools records dispatched actions and the state of the Redux, possible to travel back in time to view previous app state without reloading

**action creator** The means by which state is changed in a Redux store

**reducer** Function that determines changes to an application's state

**dispatch** a method on Redux store that is the only way to update the state. Call store.dispatch() and pass in an action object


# Preparation Materials

## [Multiple Reducers Example](https://www.youtube.com/watch?v=gBER4Or86hE)
- `import {combineReducers, createStore } from 'redux';`
- Example reducer: `const userReducer = (state={}, action) => { return state };`
- Example combineReducer example: `const reducers = combineReducers({user: userReducer, tweets: tweetReducer})`

## [Redux Docs: Using Combined Reducers](https://redux.js.org/recipes/structuring-reducers/using-combinereducers/)
- Takes an object of reducer functions and returns a new reducer function
- `createStore` function takes `preloadedState` as a second argument

## [Redux Docs: Combined Reducer Syntax](https://redux.js.org/api/combinereducers/)
- Reducers passed to `combineReducers` must satisfy the following:
   - any action that is not recognized, must return state that was given as first argument
   - must never return undefined
   - if `state` given to it is undefined, must return initial state for the specific reducer

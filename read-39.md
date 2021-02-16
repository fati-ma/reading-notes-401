# Readings: Redux - Additional Topics
## Read: 39 - Class 39

### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-39.md).



# Review, Research, and Discussion

## 1. What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?
Create an initial state that is immutable.

## 2. When using a thunk/async action that dispatches the actual action, which do you export from your reducer?
A function


# Vocabulary Terms

**middleware** code that extends the functionality of redux

**thunk** provides the ability to write actions that return a function, useful for handling side effects and asynchronous actions


# Preparation Materials

## [Redux Toolkit (RTK)](https://redux-toolkit.js.org/)
- `configureStore()` provides simplified config options, combine slice reducers, adds Redux middleware, includes Redux-thunk
- `createReducer()` supply a lookup table of action types to case reducer functions, uses `immer` library to let you write simpler immutable updates
- `createAction()` generates an action creator function for the given action type string
- `createSlice()` accepts an object of reducer functions, a slice name, and an initial state value, creates a slice reducer with corresponding action creators and action types
- `createAsyncThunk` accepts an action type string and a function that returns a promise, generates a thunk that dispatches action based on promise
- `createEntityAdaptor` generates set of reusable reducers adn selectors to manage normalized data in the store
- `createSelector` utility from `Reselect` library re-exported for ease of use
- `npm install @reduxjs/toolkit`

## [Tutorial](https://redux-toolkit.js.org/tutorials/intermediate-tutorial)
- "slice reducer" describes a reducer function responsible for updating a single key/value state
- `createSlice` and `createReducer` wrap function with `produce` from `Immer` library. Can write code that mutates code inside reducer and Immer will return a correct immutably updated result
- `ducks` pattern: "put all action creators and reducers in one file, do named exports of the action creators, and default export of reducer function"    
    
#### Alternative State Managers

- [MobX](https://mobx.js.org/getting-started.html)
- [HookState](https://hookstate.js.org/)

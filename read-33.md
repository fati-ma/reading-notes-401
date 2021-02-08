# Readings: Context API
## Read: 33 - Class 33

### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-33.md).


# Review, Research, and Discussion

## 1. Describe use cases for useMemo() and useReducer()
`useMemo()` will only recompute memoized value if one of the dependencies has changed. `useReducer()` is similar to `useState()` but works better for complex state logic or if the new state depends on the previous

## 2. Why do custom hooks need the use prefix?
So that it is clear to react if a function needs to maintain all of the hook rules.

## 3. What do custom hooks usually do?
Allow for the reuse of stateful logic.

## 4. Using any list of custom hooks, research and name one that you think will be useful in your applications
`useEffect()` is a good way to have something happen after a render or every render

## 5. Describe how a hook that fetches API data might work.
`useFetch()` is a quick way to set up a fetch and provide state for isLoading


# Vocabulary Terms

**reducer** used to manage state in an application


# Preparation Materials

## [context api](https://reactjs.org/docs/context.html)
- Context allows info to be passed between components without props
- Use case: when components at different levels all need access to the same info
- Use minimally, context makes some hooks less reusable

## [hooks and context example](https://medium.com/swlh/snackbars-in-react-an-exercise-in-hooks-and-context-299b43fd2a2b)

## [react context links](https://github.com/diegohaz/awesome-react-context)

# Readings: Props and State
## Read: 27 - Class 27
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-27.md).


# Review, Research, and Discussion

## 1. Does a deployed React application require a server?
A server is not explicitly required for deploying a React app.

## 2. Why do we prefer to test a React application at the behavior rather than the unit level?
Unit testing is good for confirming that an algorithm will always produce the desired result, but React apps are created to generate a user experience and it is more crucial that each state is rendered correctly at the correct time.

## 3. What does `npm run build` do?
This command creates a build directory that houses a production build of the app.

## 4. Describe the actual composition / architecture of a React application
- Title & Favicon: Browser tab label and thumbnail
- Router: Provides navigation through the DOM
- Material UI & Robot Font: Allows the use of prebuilt customizable components
- Backend Connectivity: Defines how the app interfaces with outside resources
- Redux & Thunk: Provisions the app level state, thunk works with redux to handle side effects like outside resource fetching
- Multi-Environment Setup: Defining dynamic configuration parameters via env variables
- Internationalization: `react-i18next` is a library that provides tools for multilingual support
- Unit testing: Jest works well for testing React apps
- Deployment: Must deploy the final /build directory


# Vocabulary Terms

**BDD** Behavior Driven Development, develope based on user behavior, combines test driven development with the business side to create a common understanding between devs, PMs, and other disciplines.

**Acceptance Tests** Determining whether design requirements have been achieved

**mounting** rendering an item to the DOM for the first time

**build** compiles the code



# Preparation Materials

- [setState explained](https://css-tricks.com/understanding-react-setstate/) 
- [handling events](https://reactjs.org/docs/handling-events.html)

- React events are named with camelCase
- Simple example: `<button on Click={activateLasers}> Activate Lasers </button>`
- returning default does not prevent default behavior in React, must use e.preventDefault();

- [forms](https://reactjs.org/docs/forms.html)
- [state and lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)

- **mounting** - rendering an item to the DOM for the first time
- **unmounting** - when an DOM element is removed
- "lifecycle methods" - methods that occur on mounting or unmounting
- `componentDidMount()` runs after a component output is rendered to the DOM
- `componentWillUnmount()` teardown an unused element
- Incorrect: `this.state.comment = 'Hello';`
- Correct: `this.setState({comment: 'Hello'});`

- [components and props](https://reactjs.org/docs/components-and-props.html)

- Components allow the UI to be split in to independent, reuseable pieces, similar to JS functions
- Simplest form: function Welcome(props) {return <h1>Hello, {props.name}</h1>}
- props = properties
- ES6 class: class Welcome extends React.Component { render () { return <h1>Hello, {this.props.name}</h1>; }}
- Always capitalize component names
- All React components must act like pure functions regarding their props

- [React Testing Library](https://testing-library.com/docs/dom-testing-library/react-testing-library)

- AAA pattern Arrange (set up the test), Act (trigger the necessary event), Assert (compare the expected outcome)
- `jest-dom` library that adds declarative matchers to jest for use with React
   - To install: $ `npm i @testing-library/jest-dom`
   - Import the package to extend the Jest matchers: `import "@testing-library/jest-dom/extend-expect"

- [RTL Testing Example](https://thomlom.dev/beginner-guide-testing-react-apps/)

### Bookmark
- [Roles Reference](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques#roles)

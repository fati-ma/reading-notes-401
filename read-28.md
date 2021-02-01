# Readings: Component Composition
## Read: 28 - Class 28
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-28.md).


# Review, Research, and Discussion

## 1. Can a parent component access the state of a child component?
Yes, by using a call back function.

## 2. What can be passed along in a prop variable?
Any and all kinds of data

## 3. How can a child component “know” the state of another component?
using React Hooks


# Vocabulary Terms

**component props** Properties of components, data that is passed into a component

**component state** this.state, provides the current snapshot of a component

**application state** current snapshot of the entire application


# Preparation Materials

## - [react basics recap](https://www.freecodecamp.org/news/these-are-the-concepts-you-should-know-in-react-js-after-you-learn-the-basics-ee1d2f4b8030/)
- Life cycle of a component: Mounting, Updating, Unmounting
- Higher-order component function that takes a component and returns a new component
- Hooks aim to replace classes

## - [props.children](https://codeburst.io/a-quick-intro-to-reacts-props-children-cb3d2fce4891?gi=7b962f28fc89)
- `this.props.children` is used to display whatever you include between the opening and closing tags when invoking a component"

## - [composition vs inheritance](https://reactjs.org/docs/composition-vs-inheritance.html)
- Some components do not know their children ahead of time
- A more specific component can render a generic component and configure it with props
- Facebook has not found a use case for component inheritance hierarchies

## - [react testing library api example(https://testing-library.com/docs/react-testing-library/example-intro/)


#### Bookmark
- [react-if component](https://www.npmjs.com/package/react-if)
- [react-testing-library-async](https://testing-library.com/docs/dom-testing-library/api-async/)

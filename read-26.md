# Readings: Component Based UI
## Read: 26 - Class 26
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-26.md).

# Review, Research, and Discussion

## 1. Name 5 JS UI frameworks (other than React)
Angular
jQuery
Bootstrap
Sencha Ext JS
Vue

## 2. What’s the difference between a framework and a library?
A library contains a methods that can be implemented to accomplish a task where as a framework is a group of libraries we use to create our program within its structure.


# Vocabulary Terms

**Rendering** Parsing HTML elements and converting them to DOM nodes

**Templates** A structural scaffold for rendering variable content to the DOM

**State** Object where property values are stored for a component


# Preparation Materials

## - [react hello world](https://reactjs.org/docs/hello-world.html)

React is an open-source, front end, JavaScript library for building user interfaces or UI components. It is maintained by Facebook and a community of individual developers and companies. React can be used as a base in the development of single-page or mobile applications.

```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

## - [introducing JSX](https://reactjs.org/docs/introducing-jsx.html)

JSX is a syntax extension to JavaScript.

- Tag syntax that looks something like this:
```
const element = <h1>Hello, world!</h1>;
```

- You can embed extentions in JSX such as variables. You can put any valid JavaScript expression inside the curly braces in JSX.

-instead of separating technologies by putting markup and logic in separate files, we can separate concerns with loosely coupled components that contain both.

-JSX is an expression too (regular JS function) after compilation.

-Prevents injection attacks so it's safe to embed user input

## - [rendering elements](https://reactjs.org/docs/rendering-elements.html)

- The smallest building block of a React app

- Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like.

- To render something in an html div somewhere, you pass both the react element and the root DOM, like this:
  ```
  const element = <h1>Hello, world</h1>;
  ReactDOM.render(element, document.getElementById('root'));
  ```
  
- React elements are immutable and can't be changed, so the only way to update an item is to re-render it completely.

- React only updates what's necessary - compares previous with new desired DOM state and updates only what's changed

### Bokkmark
- [sass cheatsheet](https://devhints.io/sass)
- [react cheatsheet](https://devhints.io/react)
- [another react cheatsheet](https://reactcheatsheet.com/)

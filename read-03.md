# Readings: Data Modeling, NoSQL
## Read: 03 - Class 03

### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-03.md).

### For this class, I will provide answers for the following questions:

1. Name 3 advantages to Test Driven Development
2. In what case would you need to use beforeEach() or afterEach() in a test suite?
3. What is one downside of Test Driven Development
4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?
5. Name a use case for a static method
6. Write an example of a Higher Order function and describe the use case it solves



## 3 advantages to Test Driven Development

1. Writing the tests first requires you to really consider what do you want from the code.
2. TDD creates a detailed specification.
3. TDD reduces the time spent on rework.


## Using `beforeEach()` or `afterEach()` in a test suite?

The behavior I am noticing is that beforeEach and afterEach are run before/after every, it blocks in the current context and all nested contexts.


## Aownside of Test Driven Development

Big-time investment. For the simple case, you lose about 20% of the actual implementation, but for complicated cases, you lose much more.


## Tprimary difference between ES6 Classes and Constructor/Prototype Classes

The most important difference between class- and prototype-based inheritance is that a class defines a type that can be instantiated at runtime, whereas a prototype is itself an object instance.


## A use case for a static method

Static methods, like many other features introduced in ES6, are meant to provide class-specific methods for object-oriented programming in Javascript. Static methods in Javascript are similar to class methods in Ruby. To declare a static method, simply prefix a method declaration with the word static inside the class declaration.

```
class Foo(){
   static methodName(){
      console.log("bar")
   }
}
```


## Example of a Higher Order function and the use case it solves
Higher-order functions allow us to abstract over actions, not just values. They come in several forms. For example, we can have functions that create new functions.

```
function greaterThan(n) {
  return m => m > n;
}
let greaterThan10 = greaterThan(10);
console.log(greaterThan10(11));
// → true
```

functions that change other functions

```
function noisy(f) {
  return (...args) => {
    console.log("calling with", args);
    let result = f(...args);
    console.log("called with", args, ", returned", result);
    return result;
  };
}
noisy(Math.min)(3, 2, 1);
// → calling with [3, 2, 1]
// → called with [3, 2, 1] , returned 1
```


## Terms

- functional programming - programming that goes somewhat linearly by applying functions.
- object-oriented programming (OOP) - programming that utilizes classes, inheritance, methods... etc to model the world after "objects" that have verbs for us to use.
- class - something we create an object of - a model.
- super - the class that this one extends. we use it to call the class this one is based on's constructor, for example.
- this - the current object in which this operation is happening
- Test Driven Development (TDD) - again? development that starts with writing the test before writing the code, write enough code to make the test pass, then continue on.
- Jest - a module that allows us to run tests to do CI
- Continuous Integration (CI) - a strategy that allows us to run tests every time there's a code check in, it enables continuous deployment as well.
- REST - representational state transfer - allows us a set of verbs to perform CRUD operations over http.
- Data Model - the base properties and methods for an object we will want to use. in a way sort of the template of an object.

# Readings: Application State with Redux
## Read: 36 - Class 36

### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-36.md).


# Review, Research, and Discussion

## 1. What are the advantages of storing tokens in “Cookies” vs “Local Storage”
It is better to store tokens in cookies because cookies are less susceptible to XSS attacks.

## 2. Explain 3rd party cookies.
3rd party cookies are placed on a client by a creator other than the site that installs them, primarily used for tracking, advertisement targeting, and analysis

## 3. How do pixel tags work?
Pixel tags work like any other tag and are served just like other images, but they are intended to be invisible to the user. The image is served by an advertiser who then gains access to reading and recording the user cookies


# Vocabulary Terms

**cookies** piece of information stored on client computer

**authorization** Process by which a client proves their identity and is granted access or privileges

**access control** Limiting which clients can access which parts of a site

**conditional rendering** Rendering certain parts of a page or site depending on a client or current state


# Preparation Materials

## [Dan Abramov Redux Tutorials](https://egghead.io/courses/getting-started-with-redux)

- Everything that changes in an app is stored in a single object

- Action allows for changes to Redux

- State is redundant

- Redux functions must be pure

- Function must take in previous state and return the new state


### Bookmark

[worlds easiest guide to redux](https://www.freecodecamp.org/news/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6/)

[testing reducers](https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1)

[Redux Docs](https://redux.js.org/)

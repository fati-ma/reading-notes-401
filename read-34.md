# Readings: Login and Auth
## Read: 34 - Class 34

### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-34.md).


# Review, Research, and Discussion

## 1. Why is the Context API useful?
Useful when some data needs to be accessible by many components at different levels.

## 2. Can a component outside of a provider get its context?
Yes, it is possible to access context outside of a provider.

## 3. What are some common use cases for using the Context API?
Where data or state is needed by all or most components such as page themes

## 4. Describe “Context Hell”
Many nested layers of components passing context down


# Vocabulary Terms

**global state** A higher order component that stores state that is needed by many other components

**global context** Top level object that will contain all of the context for all consumers

**provider** Context object that shares props with all consumers, consumers will rerender when every provider prop changes

**consumer** Subscribes to a provider and rerenders whenever the provider props change



# Preparation Materials

## [what is role based access control?](https://digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more)
- RBAC (Role Based Access Control)
- Limits network access to only those who need access and provides access to only what is needed by job role
- Benefits
   - Reduces administrative work and IT support
   - Maximizing operational efficiency
   - Improves compliance regarding the safeguarding of sensitive data

## [react-cookies component](https://www.npmjs.com/package/react-cookies)
- Documentation for NPM package react-cookies `npm i react-cookies --save`

## [react-cookie library](https://www.npmjs.com/package/react-cookie)
- Documentation for NPM package React-Cookie
- `npm i react-cookie`



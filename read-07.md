# Readings: Express
## Read: 07 - Class-07
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-07.md).


# Review, Research, and Discussion

## 1. What’s the difference between PUT and PATCH?
PUT updates the entire resource, and PATCH can update parts of it 

## 2. Provide links to 3 services or tools that allow you to “mock” an API for development like json-server
Jest which we use for testing, Mirage js and Cypress

## 3. Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?
Swagger allows you to describe your api's structure in a way that machines can read them, building an interactive api documentation. APIDoc creates a documentation from API annotations in the source code. For apidocs.js we have to modify documentation for each affected method/endpoint when we make code changes. swagger uses plain json which is easy to read for 3rd party apps or services. 
200 - success 400 - bad request 403 - forbidden 404 - resource not found 500 - internal server error

## 4. Compare and contrast SOAP and ReST
SOAP is more rigid than rest but gives us better standardization. REST is more flexible. SOAP is language, platform and transport independent while REST requires http. SOAP works well in distributed enterprise environments whereas REST assumes direct point-to-point communication. SOAP is standardized, has built-in error handling and some automation with certain languages. REST is easier to use, easier to learn, more flexible, and doesn't require an expensive tool to interact with the web service. REST is more efficient as it doesn't always use XML for smaller message formats. REST is fast as it doesn't require extensive processing. REST is more consistent with other web technologies in design philosophy.


# Vocabulary Terms

**SOAP** : Simple Object Access Protocol is a messaging protocol specification for exchanging structured information in the implementation of web services in computer networks. Its purpose is to provide extensibility, neutrality, verbosity and independence.

**ReST Verbs**: specify an action to be performed on a specific resource or a collection of resources.

**CRUD Verbs**: The primary or most-commonly-used HTTP verbs (or methods, as they are properly called) are POST, GET, PUT, PATCH, and DELETE. These correspond to create, read, update, and delete (or CRUD) operations, respectively.

**Swagger** : Swagger allows you to describe the structure of your APIs so that machines can read them. The ability of APIs to describe their own structure is the root of all awesomeness in Swagger


# Preparation Materials

## [express middleware explained](https://www.youtube.com/watch?v=9HOem0amlyg)

## [using express middleware](https://expressjs.com/en/guide/using-middleware.html)

## [express middleware](https://www.tutorialspoint.com/expressjs/expressjs_middleware.htm)


Express is a routing and middleware web framework that has minimal functionality of its own: An Express application is essentially a series of middleware function calls.

Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named next.

Middleware functions can perform the following tasks:
  - Execute any code.
  - Make changes to the request and the response objects.
  - End the request-response cycle.
  - Call the next middleware function in the stack.

Types of middleware:
  - Application-level middleware
  - Router-level middleware
  - Error-handling middleware
  - Built-in middleware
  - Third-party middleware



## [using express routing](https://expressjs.com/en/guide/routing.html)

Routing refers to how an application’s endpoints (URIs) respond to client requests. A route method is derived from one of the HTTP methods, and is attached to an instance of the express class.

example of routes that are defined for the GET and the POST methods to the root of the app.

```
// GET method route
app.get('/', function (req, res) {
  res.send('GET request to the homepage')
})
```
```
// POST method route
app.post('/', function (req, res) {
  res.send('POST request to the homepage')
})
```

**Route paths**
Route paths, in combination with a request method, define the endpoints at which requests can be made. Route paths can be strings, string patterns, or regular expressions.

The characters `?, +, *, and ()` are subsets of their regular expression counterparts. The hyphen (-) and the dot (.) are interpreted literally by string-based paths.

examples of route paths based on strings

```
app.get('/', function (req, res) {
  res.send('root')
})
```
```
app.get('/about', function (req, res) {
  res.send('about')
})
```
```
app.get('/random.text', function (req, res) {
  res.send('random.text')
})
```
```
app.get('/ab*cd', function (req, res) {
  res.send('ab*cd')
})
```
```
app.get('/ab(cd)?e', function (req, res) {
  res.send('ab(cd)?e')
})
```

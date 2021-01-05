# Readings: API Server
## Read: 09 - Class-09
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-09.md).


# Review, Research, and Discussion

## 1. How does route prefixing work with an external routing module?
inside `server.js` we use: 
```
let externalRoutes = require('./routes/externalRoutes');
app.use('/externalRoutes', externalRoutes);
```

## 2. When routing, what’s the difference between `app.get(‘/data/:id’)` and `app.get(‘/data/:name’)`?
The diffrence is in the request pararms [req.params], as the params is an object here have 2 property one for the id and the other for the name.

## 3. Explain how Express handles routing conflicts?
Routes are processed by Express in order

## 4. What are the ways that a browser can send “data” or request variables to an HTTP server?
Using HTML tag form and pass the method of the request, path and the data if needed.


# Vocabulary Terms

**Routing** : How an application’s endpoints (URIs) respond to client requests.

**Route Prefixing** : Is a concept to make the route function that receive same prefix of different requests.

**Request “Body”** : Property for request object comes with post,put,patch,delete method, here doesn't appears on the url

**Request “Query”** : Property for request object comes with get method, here we send data in the url.

**Request “Params”** : Property for request object comes with all method method t have placeholder in the url to send data on it.


# Preparation Materials

## 1. [express router.param() middleware](https://expressjs.com/en/4x/api.html#router.param)

`router.param(name, callback)`
Adds callback triggers to route parameters, where name is the name of the parameter and callback is the callback function. Although name is technically optional, using this method without it is deprecated starting with Express v4.11.0 (see below).

The parameters of the callback function are:

- req, the request object.
- res, the response object.
- next, indicating the next middleware function.
- The value of the name parameter.
- The name of the parameter.

Param callback functions are local to the router on which they are defined. They are not inherited by mounted apps or routers. Hence, param callbacks defined on `router` will be triggered only by route parameters defined on `router` routes.

A param callback will be called only once in a request-response cycle, even if the parameter is matched in multiple routes.


## 2. [mongoose middleware](https://mongoosejs.com/docs/middleware.html)

Middleware (also called pre and post hooks) are functions which are passed control during execution of asynchronous functions. Middleware is specified on the schema level and is useful for writing plugins.
Mongoose has 4 types of middleware: document middleware, model middleware, aggregate middleware, and query middleware.

Pre middleware functions are executed one after another, when each middleware calls next.

Middleware are useful for atomizing model logic. Here are some other ideas:

- complex validation
- removing dependent documents (removing a user removes all their blogposts)
- asynchronous defaults
- asynchronous tasks that a certain action triggers
- Errors in Pre Hooks


## 3. [mongoose sub-documents](https://mongoosejs.com/docs/subdocs.html)

Subdocuments are similar to normal documents. Nested schemas can have middleware, custom validation logic, virtuals, and any other feature top-level schemas can use. The major difference is that subdocuments are not saved individually, they are saved whenever their top-level parent document is saved.

Subdocuments are documents embedded in other documents. In Mongoose, this means you can nest schemas in other schemas. Mongoose has two distinct notions of subdocuments: arrays of subdocuments and single nested subdocuments.
Aside from code reuse, one important reason to use subdocuments is to create a path where there would otherwise not be one to allow for validation over a group of fields (e.g. dateRange.fromDate <= dateRange.toDate).

Subdocuments have `save` and `validate` middleware just like top-level documents. Calling save() on the parent document triggers the save() middleware for all its subdocuments, and the same for validate() middleware.


## 4. [mongoose virtual joins](http://mongoosejs.com/docs/populate.html#populate-virtuals)

virtuals are not included in toJSON() output by default. If you want populate virtuals to show up when using functions that rely on JSON.stringify(), like Express' res.json() function, set the virtuals: true option on your schema's toJSON options.
when using populate projections, make sure foreignField is included in the projection.

Populate virtuals also support counting the number of documents with matching `foreignField` as opposed to the documents themselves. 

# Readings: Express Routing & Connected API
## Read: 08 - Class-08
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-08.md).


# Review, Research, and Discussion

## 1. Name 3 real world use cases where you’d want to change the request with custom middleware
  - Facebook post can be validated for malicious code before the actual post
  - In Instagram "stories" get request an ad middleware can be used to serve ads
  - In google photos, an object recognition middleware can be used to identify persons in a photo before storing it.


## 2. True or false: The route handler is middleware?
  - False

## 3. In what ways can a middleware function end the process and send data to the browser?
  - next

## 4. At what point in the request lifecycle can you “inject” middleware?
  - After making the request but before receiving the route handler
  
## 5. What can cause express to error with “Request headers sent twice, cannot start a second response”
  - Response more than once for the same request and the body is missing
  
  
  
# Vocbulary Terms

**Middleware**:
functions are functions that have access to the request object ( req ), the response object ( res ), and the next function in the application's request-response cycle.

**Request Object**: 
request object allows you to submit a POST or GET request to an URL. Essentially it provides a way to make REST API requests to another URL.

**Response Object**: 
The res object represents the HTTP response that an Express app sends when it gets an HTTP request.

**Application Middleware**: 
Bind application-level middleware to an instance of the app object.

**Routing Middleware**: 
Router-level middleware works in the same way as application-level middleware, except it is bound to an instance of express.Router().


# Preparation Materials

1. [using express routing](https://expressjs.com/en/guide/routing.html)
Routing refers to how an application’s endpoints (URIs) respond to client requests. For an introduction to routing, see Basic routing.

You define routing using methods of the Express app object that correspond to HTTP methods; for example, app.get() to handle GET requests and app.post to handle POST requests. For a full list, see app.METHOD. You can also use app.all() to handle all HTTP methods and app.use() to specify middleware as the callback function (See Using middleware for details).

These routing methods specify a callback function (sometimes called “handler functions”) called when the application receives a request to the specified route (endpoint) and HTTP method. In other words, the application “listens” for requests that match the specified route(s) and method(s), and when it detects a match, it calls the specified callback function.

In fact, the routing methods can have more than one callback function as arguments. With multiple callback functions, it is important to provide next as an argument to the callback function and then call next() within the body of the function to hand off control to the next callback.


2. [express routing](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)

here's an example of a basic express router being used:
```
// server.js
// we'll create our routes here

// get an instance of router
var router = express.Router();

// home page route (http://localhost:8080)
router.get('/', function(req, res) {
    res.send('im the home page!');  
});

// about page route (http://localhost:8080/about)
router.get('/about', function(req, res) {
    res.send('im the about page!'); 
});

// apply the routes to our application
app.use('/', router);
```

- route middleware can be run using router.use()
- route with params looks the same as the app.get equivalent.
- router.param() creates middleware that will run for a certain route parameter, for example "name" in the /person route, to do validation or whatever else we want.
- another example of app.route('/blah', ...) chainging with a.get () .post()... etc

# Readings: HTTP and REST
## Read: 06 - Class-06
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-06.md).


## Review, Research, and Discussion

### 1. Define three related pieces of data in a possible application. An example for a store application might be Product, Category and Department. Describe the constraints and rules on each piece of data and how you would relate these pieces to each other. For example, each Product has a Category and belongs in a Department.
An registeration system that has Student, Course and Department. Each Students is registered to a Course and belongs to a Department.

### 2. What is the advantage of an ORM, like Mongoose?
The net result of these is the simplification of database access from applications. MongooseJS provides an abstraction layer on top of MongoDB that eliminates the need to use named collections. Models in Mongoose perform the bulk of the work of establishing up default values for document properties and validating data. Functions may be attached to Models in MongooseJS. This allows for seamless incorporation of new functionality. Queries use function chaining rather than embedded mnemonics which result in code that is more flexible and readable, therefore more maintainable as well. The net result of these is the simplification of database access from applications.

### 3. How does the repository pattern compare with an ORM?
The ORM is an implementation detail of the Repository. The ORM just makes it easy to access the DB tables in an OOP friendly way. Repositories deal with Domain/Business objects (from the app point of view), an ORM handles DB objects. The repository abstract the access to all storage concerns, while the ORM abstract access to a specific RDBMS In a nutshell

### 4. When making a repository/facade, what flexibility do you gain?
The flexibility comes with if you need to move to another database layer later, you can code to an interface and then your application does not care what that initialization of that database layer is. It also makes testing a lot easier because then you can have a "TestingUsersRepository" that doesnt rely on anything but the class itself and your favorite js unit testing framework.

### 5. Name 3 cloud based NoSQL Databases
  - Firebase 
  - MongoDB 
  - AWS cloud
  
  
## Document the following Vocabulary Terms

**Lifecycle**
Program lifecycle phases are the stages a computer program undergoes, from initial creation to deployment and execution. The phases are edit time, compile time, link time, distribution time, installation time, load time, and run time.

**Collections**
MongoDB stores data records as documents (specifically BSON documents) which are gathered together in collections. A database stores one or more collections of documents.

**The “Repository” design pattern**
The repository pattern is one of the more popular patterns at the moment. It follows the solid principles and done right it is clean and easy to use. The repository pattern have two purposes; first it is an abstraction of the data layer and second it is a way of centralizing the handling of the domain objects.

**mongoose middleware**
Mongoose middleware are functions that can intercept the process of he init, validate, save, and remove instance methods. Middleware are executed at the instance level and have two types: pre middleware and post middleware. Pre middleware gets executed before the operation happens. For instance, a pre-save middleware will get executed before the saving of the document. This functionality makes pre middleware perfect for more complex validations and default values assignment. A pre middleware is defined using the pre() method of the schema object

**Object Relation Mapping (ORM)**
Object-relational mapping (ORM, O/RM, and O/R mapping tool) in computer science is a programming technique for converting data between incompatible type systems using object-oriented programming languages. This creates, in effect, a "virtual object database" that can be used from within the programming language.


## Preview

### [REST and HTTP](https://www.youtube.com/watch?v=Q-BpqyOT3a8)

**Hypertext Transfer Protocol HTTP**
In networks we have something called OSI which is consist of 7 layers. One of these layer is application layer which is an abstraction layer that specifies the shared communications protocols and interface methods used by hosts in a communications network. One the most important protocols in application layer is http. HTTP is protocol for transmitting hypermedia documents, such as HTML. It was designed for communication between web browsers and web servers, but it can also be used for other purposes.

**Application Program Interface API**
API is a contract provided by one piece of software to another. It receives a structured request and reply with a structured response.

**Representational state transfer (REST)**
REST is a software architectural style that defines a set of constraints to be used for creating Web services. REST is not a transfer protocol so it needs a carrier protocol such as HTTP. Web services that conform to the REST architectural style, called RESTful Web services, provide interoperability between computer systems on the internet. RESTful Web services allow the requesting systems to access and manipulate textual representations of Web resources by using a uniform and predefined set of stateless operations.


### [Http Basics](https://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-1--net-31177)
HTTP stands for Hypertext Transfer Protocol. It's a stateless, application-layer protocol for communicating between distributed systems, and is the foundation of the modern web. As a web developer, we all must have a strong understanding of this protocol.

![](https://cdn.tutsplus.com/net/authors/jeremymcpeak/http1-request-response.png)

Communication between a host and a client occurs, via a request/response pair. The client initiates an HTTP request message, which is serviced through a HTTP response message in return. We will look at this fundamental message-pair in the next section.


### [What is Rest](https://restfulapi.net/)
**REST** is acronym for **REpresentational State Transfer**.
The key abstraction of information in REST is a resource. Any information that can be named can be a resource: a document or image, a temporal service, a collection of other resources, a non-virtual object (e.g. a person), and so on. REST uses a resource identifier to identify the particular resource involved in an interaction between components.
Another important thing associated with REST is resource methods to be used to perform the desired transition. A large number of people wrongly relate resource methods to HTTP GET/PUT/POST/DELETE methods.

A lot of people prefer to compare HTTP with REST. REST and HTTP are not same.

> REST != HTTP

In simplest words, in the REST architectural style, data and functionality are considered resources and are accessed using Uniform Resource Identifiers (URIs). The resources are acted upon by using a set of simple, well-defined operations. The clients and servers exchange representations of resources by using a standardized interface and protocol – typically HTTP.


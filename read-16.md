# Readings: Event Driven Applications
## Read: 16 - Class 16
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-16.md).


# Review, Research, and Discussion

## 1. Why is access control important?
Security - to make sure only people who are authorized can do certain actions which is to minimize the risk of unauthorized access to physical and logical systems and ensures security technology and access control policies are in place to protect confidential information.

## 2. Describe an application that would need access control.
A governmental website would need access control to make sure that only people who are authorized at the appropriate level can modify the contents of the website that constituents are consuming, so some random hacker can't just go in there and change things up.

## 3. What is a role used for?
To specify the capabilities/access level users of that role are granted.

## 4. Why is role based access control more scalable than discretionary or mandatory access control?
Role based access control is more scalable because a new employee can be assigned a role and instantly be granted the same permissions as any other employee with the same role. Updating a role will updated permissions for all related users. Changing a user to another role would also update their permissions.


# Vocabulary Term

**Authorization** User credentials that confirm their permissions for a site or application. (sending credentials to be checked to see whether the user is authorized to proceed.)

**Role Based Access Control** assigning each user a generic role that specifies what that group of users is allowed to do (e.g. CRUD operations)

**Capabilities** The rights a user is granted in regard to site access and manipulation.


# Preparation Materials

[Event Driven Programming](https://www.digitalocean.com/community/tutorials/nodejs-event-driven-programming)

- Event Driven Programming a logical pattern that we can choose to confine our program to avoid complexity and collisions
- Event handler callback function that is called when an event is triggered
- Main loop primary logic listening for event triggers
- EventEmitter built in module to allow for interaction with events
   - `const EventEmitter = require('events').EventEmitter;`
   - `const myEventEmitter = new EventEmitter;`
   

[Node docs: events](https://nodejs.org/api/events.html)

- The EventEmitter calls all listeners synchronously in the order in which they were registered. This ensures the proper sequencing of events and helps avoid race conditions and logic errors. When appropriate, listener functions can switch to an asynchronous mode of operation using the setImmediate() or process.nextTick() methods:
```
const myEmitter = new MyEmitter();
myEmitter.on('event', (a, b) => {
    setImmediate(() => {
    console.log('this happens asynchronously');
    });
});
myEmitter.emit('event', 'a', 'b');
```

- Using the eventEmitter.once() method, it is possible to register a listener that is called at most once for a particular event. Once the event is emitted, the listener is unregistered and then called.
As a best practice, listeners should always be added for the 'error' events.
```
const myEmitter = new MyEmitter();
myEmitter.on('error', (err) => {
    console.error('whoops! there was an error');
});
myEmitter.emit('error', new Error('whoops!'));
// Prints: whoops! there was an error
```

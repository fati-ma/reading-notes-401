# Readings: TCP Servers
## Read: 17 - Class 17
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-17.md).


# Review, Research, and Discussion

## 1. Given the examples of front-end events such as button click, window resize, form submit, etc, what are some examples of back-end events?
When a user clicks on a button and fires of an event to submit a form, there is also an event that happens on the back-end to:
  - recieve the data
  - verify that the data is valid
  - process data

## 2. Why are events sometimes better than asynchronous actions with callbacks?
Events are something that has already happened whereas asnync callbacks are waiting to be called in order to run, and the benefit of events is that they can handle more complex tasks in a readable way, and they can be called many times, whereas a Promise can only be resolved once.

## 3. What does an EventEmitter instance do?
In Node.js, the EventEmitter is a class. All objects that emit events are instances of the EventEmitter class. A single instance of the EventEmitter can be used to have all events listen/emit on the same instance, therefore allowing them to communicate.

## 4. When is a program’s call stack, event queue, and event loop active?
The call stack and event queue contain all operations to be executed in a program. Tne event loop will run asynchronously, checking to see if the call stack is empty. Once the call stack is empty, there are no more operations to be run, then the event loop will end.

# Vocabulary Terms


**Observer Pattern** An object, called the subject, will have observers. When the state changes, the subject will immediately notify the objects.

**Listener** A function within a program whose sole puspose is to wait for a specified event to happen and when that event happends, do some stuff. Something that listens for an event that will trigger a function.

**Event Handler** A fucntion that is typically tied to a listener. When the event happens that the listener is waiting for, it's the event handler that does something in respose to the awaited event. The callback function that will run when an event triggers it.

**Event Driven Programming** Programming where when an event happens, the next function is called. It makes use of callback functions with an event handler, and a main loop that listens for event triggers.

**Event Loop** he paradigm, or perhaps the process by which JavaScript manages events or fucntions and the order in which they are executed. It is a behind the scenes part of JS that itslef manages the call stack event queue. When Node.js starts, it kicks off the event loop. There is a queue of phases that the loop goes through one at a time, and it will go back to the top when it is done with all of the phases.

**Event Queue** A queue where each "node" contains an event, and the application will run through the events as part of the event loop. It is a way to acheive asynchronous programming.

**Call Stack** The call stack is where functions are placed before they are called. When another function is called within a function, the called function goes to the top of the stack.

**Emit/Raise/Trigger** Emitters are the objects that trigger events. Raising describes when the event is emitted. Triggers signal that an event or action was completed.

**Subscribe** Subscribe an event handler to a specific event. This is how you listen for an event to happen. You subscribe to an event that will trigger the callback function.

**database** A structured collection of data that can be accessed, added to or manipulatd. A database is used when persisting data. There are many types of databases, but are essentially split into relational (SQL) and non-relational (NoSql). A structured and organized collection of data that is stored and accessed by a computer system.


# Preparation Materials

[OSI Model Explained](https://www.youtube.com/watch?v=vv4y_uOneC0)
[TCP Handshakes Explained](https://www.youtube.com/watch?v=xMtP5ZB3wSk)
[OSI Model](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)
[What is TCP](https://searchnetworking.techtarget.com/definition/TCP)
[Build a TCP Server (code only)](https://techbrij.com/node-js-tcp-server-client-promisify)
[Node docs: net module](https://nodejs.org/api/net.html)

## TCP
TCP (Transmission Control Protocol) is a standard that defines how to establish and maintain a network conversation through which application programs can exchange data. TCP works with the Internet Protocol (IP), which defines how computers send packets of data to each other. Together, TCP and IP are the basic rules defining the Internet. The Internet Engineering Task Force (IETF) defines TCP in the Request for Comment (RFC) standards document number 793.

How Transmission Control Protocol works TCP is a connection-oriented protocol, which means a connection is established and maintained until the application programs at each end have finished exchanging messages. It determines how to break application data into packets that networks can deliver, sends packets to and accepts packets from the network layer, manages flow control and – because it is meant to provide error-free data transmission – handles retransmission of dropped or garbled packets and acknowledges all packets that arrive. In the Open Systems Interconnection (OSI) communication model, TCP covers parts of Layer 4, the transport layer, and parts of Layer 5, the session layer.

## What TCP is used for
TCP is used for organizing data in a way that ensures the secure transmission between the server and client. It guarantees the integrity of data sent over the network, regardless of the amount. For this reason, it is used to transmit data from other higher-level protocols that require all transmitted data to arrive. Examples include:

Secure Shell (SSH), File Transfer Protocol (FTP), Telnet: For peer-to-peer file sharing, and, in Telnet’s case, logging into another user’s computer to access a file. Simple Mail Transfer Protocol (SMTP), Post Office Protocol (POP), Internet Message Access Protocol (IMAP): For sending and receiving email HTTP: For web access

## Why TCP is important
TCP is important because it establishes the rules and standard procedures for the way information is communicated over the internet. It is the foundation for the internet as it exists today and ensures that data transmission is carried out uniformly, regardless of the location, hardware or software involved. For this reason, it is flexible and highly scalable, meaning new protocols can be introduced to it and it will accommodate them. It is also nonproprietary, meaning no one person or company owns it.

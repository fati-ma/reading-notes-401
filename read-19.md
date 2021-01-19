# Readings: Message Queues
## Read: 19 - Class 19
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-19.md).


# Review, Research, and Discussion

## 1. What does it mean that web sockets are bidirectional? Why is this useful?
Bidirectional means that a single port can both receive and send data this allows for asynchronous responses without having to wait for additional requests

## 2. Does socket.io use HTTP? Why?
Yes, HTTP is required for the initial handshake to setup the communication

## 3. What happens when a client emits an event?
The event gets passed to the server through websockets

## 4. What happens when a server emits an event?
A callback function allows us to implement some sort of action on the client end

## 5. What happens if a client “misses” an event?
## 6. How can we mitigate this?
If an event is missed it is ignored. To avoid this have listeners always on and use internal logic to decide if the event is relevant


# Vocabulary Terms

**Web Socket** communication protocol that provides full-duplex comm over single TCP

**Socket.io** javascript library for building realtime web applications

**Client** a user computer that interacts with a server

**Server** computer that accepts requests from a client and returns data


# Preparation Materials

[Socket.io Chat Example](https://socket.io/get-started/chat/)

[Rooms and Namespaces](https://socket.io/docs/v3/rooms/index.html)

[Socket.io Emit Cheatsheet](https://socket.io/docs/v3/emit-cheatsheet/index.html)

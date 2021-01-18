# Readings: Socket.io
## Read: 18 - Class 18
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-18.md).


# Review, Research, and Discussion

## 1. What is the benefit of transforming data into packets?
Splitting the data allows each piece to be sent independent of the others and reassembled on the receiving end which allows for more network flexibility.

## 2. UDP is often refereed to as a connectionless protocol. Why is this?
UDP does not require a server and client to establish a three-way handshake prior to transmission.
UPD no connection needs to be established between the origin and destination before tranferring data.

## 3. Can a socket server application have multiple socket connections?
Yes, using socket.io

## 4. Can a socket connection application be connected to multiple socket servers?
Yes, as long as each connection is associated with a different client IP/Port.

## 5. Can an application be both a socket server and a socket connection?
Not if they are intended to be used at the same time on the same port.
Yes, we can but its not a good practice.

# Vocabulary Terms

**OSI Model** OSI stands for Open System Interconnection. It is a conceptual framework for understanding the networking process. The seven layers of OSI are Physical, Data Link, Network, Transport, Session, Presentation, and Application.

**TCP Model**  This is a more concise version of the OSI Model, and it consists of four layers: Application, Transport, Internet, and Network.

**TCP** This stands for Transmission Control Protocol. In this, the server must be listening for connections from clients.

**UDP** This stands for User Datagram Protocol. Unlike TCP, there is no need to establish a connection before transfering data.

**Packets** A unit of data that goes from one place to another over a network.

**Socket** A socket is an endpoint for sending and receiving data. Sometimes this refers to an internet socket, where a socket is identified to other hosts by its socket address.


# Preparation Materials

[Web Sockets](https://en.wikipedia.org/wiki/WebSocket)
[Socket.io Tutorial](https://www.tutorialspoint.com/socket.io/)
[Socket.io vs Web Sockets](https://www.educba.com/websocket-vs-socket-io/)
[Socket.io Documentation](https://socket.io/docs/v3/index.html)
[Socket.io Server API](https://socket.io/docs/v3/server-api/index.html)
[Socket.io Client API](https://socket.io/docs/v3/client-api/index.html)
[Socket Testing Tool](https://amritb.github.io/socketio-client-tool/)

- WebSocket communications protocol over single TCP
- WebSocket remains open all of the time to allow for realtime transfer, event driven
- Socket.io is a library that allows for full duplex communication, event driven
- WebSocket protocol schema ws://example.com:4000/chatroom.php
   - `ws:// Schema`
   - `example.com Host`
   - `:4000 Port`
   - `/chatroom.php` Server
   
- Socket.io allows for broadcasting multiple sockets at the same time
- Socket.io enables real-time bidirectional event-based communication, built on top of web sockets API and node.js
- This site offers a tutorial to help users build "moderately complex real-time websites, back-ends for mobile applications, and push notifications"
- Socket.io is a JS library for real-time web apps
- `$npm i socket.io` to install in a directory



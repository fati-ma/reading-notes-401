# Readings: OAuth
## Read: 12 - Class-12
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-12.md).


# Review, Research, and Discussion

## 1. Why is authentication important?
To protect the users and make sure each one fatch and access to his data only.

## 2. Why should we be careful about storing a user’s password?
To protect sensitive information for the users if to get access and permission.

## 3. What is the difference between hashing and encryption?
Encrypted can be decrypted, but hashed cannot be unhashed and hashing is more secure than encryption.

## 4. What is the difference between encryption and encoding?
Encoding can be reversed by the same algorithm, but encryption needs a key to be reversed, so encryption is more secure than encoding.

## 5. What is a token used for?
Authenticate a a user.


# Vocabulary Terms

**authentication** Verifying a user's identity by requiring pre-required details.

**authorization** The process of allowing a user access to a resource.

**encryption** The translation of data to another form so that only a secret key or password can read it.

**hashing** The conversion of one value to another. This is done to make data like passwords difficult to decipher.

**session** Interactions with a website that take place in a given time frame.

**cookie** A small amount of data that is stored by the web browser to so a website can remember information about you.

**token** With token based authentication, the user state is stored on the client. The data is encrypted in a JWT. The server then validates the JWT.

**Basic Auth** An authentication built into HTTP , where the authorization header contains the word basic followed by a space and an encoded string of username:password

**encoding** The process of converting one code of data to another. It goes from something a user can understand to something less clear.

**secret** This ia a secret that only the application and authorizaiton server know. It should be random enough that it can not be guessed.

**cryptography** Protecting information by transforming it into a format that can not be easily understood.


# Preparation Materials

## 1. [What is OAuth Really All About?](https://www.youtube.com/watch?v=t4-416mg6iU)
## 2. [OAuth2 simplified](https://aaronparecki.com/oauth-2-simplified/)

**Roles**
   - The Third-Party Application: "Client"
   - The API: "Resource Server"
   - The Authorization Server
   - The User: "Resource Owner"

The first step of OAuth 2 is to get **authorization** from the user.
OAuth 2 provides several "grant types" for different use cases:
   - Authorization Code
   - Password
   - Client credentials
   - Implicit
   
## 3. [Build a Node API with OAuth](https://developer.okta.com/blog/2018/08/21/build-secure-rest-api-with-node)

Node uses a package.json to manage dependencies and define your project. To create one, use npm init, which will ask you some questions to help you initialize the project.
The default entry point is index.js, so you should create a new file by that name.
The promisify function of util lets you take a function that expects a callback and instead will return a Promise, which is the new standard as far as handling asynchronous code. This also lets us use the relatively new async/await syntax and make our code look much prettier.
For some quick linting, install standard as a dev dependency.
Create a new file database.js.
The Sequelize function creates a database. This is where you configure details, such as what dialect of SQL to use. 

# Readings: Authentication
## Read: 11 - Class-11
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-11.md).


# Review, Research, and Discussion

## 1. Explain what a “Singleton” is (in Computer Science terms)
A class that you can only have one instance of.

## 2. Explain how the Singleton pattern can be used with Node modules, specifically with classes.
Create a single object to use with other objects without having to recreate that object multiple times. It allows us to uses one instance of an object through out different objects.

## 3. If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?
I'm not sure if I understood the question, but to build a middleware I will first think about the problem where trying to slove, then building the middleware function that solves this problem by using the right request method.


# Vocabulary Terms

**Router Middleware**: Router is a type of Express middlware that handles requests and sends them via the approproate route. They are functions that have access to the request and response objects and the next middleware function so that they can be run on a route before it goes on to do the work the user requested. 

**Dynamic Module Loading**: Allows us to dynamically load modules in our js code such as importing ES modules with import(), which we use as a function with a string param that can be any code that leads to a string. the function call is a promise, once the module is loaded, the promise is fulfilled. 

**Singleton Pattern**: Restricts instantiation of a class to only one instance. 

**CRUD -> REST Method Matches**: CRUD: CREATE READ UPDATE DELETE -> REST: GET POST PUT DELETE.

**Mock Testing**: An approach to unit testing using a mock server to run your tests on without using the actual server so that you don't add testing load to it and the dependencies are replaced with objects that simulate the behaviour of the real ones.


# Preparation Materials

1. [Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)

- General purpose cryptographic hash algorithms such as MD5, SHA1. SHA256, SHA512 and SHA-3 are susceptible to brute force attacks. A 16 letter strong password can be cracked in an hour.
- A Hash Collision attack is possible because hash functions take in infinite input length and produce same output length, which means some words will end up with the same hash. Salting your password (whatever that means) can foil dictionary attacks, but an attacker can stil use a wordlist to crack the hashes.
- PBKDF2 and Bcrypt are slow and very strong because they make brute force attacks slower by Key stretching. When computers get faster next year, we can increase the work factor to balance it out (to make the attack slower again).
   - Key stretching: "key stretching techniques are used to make a possibly weak key, typically a password or passphrase, more secure against a brute-force attack by increasing the resources (time and possibly space) it takes to test each possible key."
   - Bcrypt is an adaptive hash function based on the Blowfish symmetric block cipher cryptographic algoritm and introdcues a work factor (aka a security factor) that allows you too determine how expensive the hash function will be.
   - Implemented in PHP, Java, Ruby, C# and C... etc.
   
   
2. [Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)

- simplest technique for access control
- No cookies, session identifiers or login pages.
- Uses http header Authorization: Basic <credentials>
- Credentials is encoding of username:password. For example, if the browser uses Aladdin as the username and OpenSesame as the password, then the field's value is the Base64 encoding of Aladdin:OpenSesame, or QWxhZGRpbjpPcGVuU2VzYW1l. Then the Authorization header will appear as: Authorization: Basic QWxhZGRpbjpPcGVuU2VzYW1l
- Does not have hashing or encryption so should only be used over https. 


3. [Intro to JWT](https://jwt.io/introduction/)

- Authorization: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.

- Information Exchange: JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.

- What is the JSON Web Token structure?

   **Header** : The header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.

   **Payload** : The second part of the token is the payload, which contains the claims. Claims are statements about an entity (typically, the user) and additional data.

   **Signature** : can be defined at will by those using JWTs. But to avoid collisions they should be defined in the IANA JSON Web Token Registry or be defined as a URI that contains a collision resistant namespace.


4. [OWASP auth cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)

5. [bcrypt docs](https://www.npmjs.com/package/bcrypt)

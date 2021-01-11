# Readings: Bearer Authorization
## Read: 13 - Class-13
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-13.md).


# Review, Research, and Discussion

## 1. Write the following steps in the correct order:
   1. Register your application to get a client_id and client_secret
   2. Ask the client if they want to sign in via a third party
   3. Redirect to a third party authentication endpoint
   4. Make a request to a third-party API endpoint
   5. Receive authorization code
   6. Make a request to the access token endpoint
   7. Receive access token
   
## 2. What can you do with an authorization code?
Exchange it for an access token

## 3. What can you do with an access token?
Use it to make api calls on behalf of the user

## 4. What’s a benefit of using OAuth instead of your own basic authentication?
More secure because you don't have the burden of saving passwords in your own db and then having to worry about liability or being hacked giving away access to user accounts.


# Vocabulary Terms

**Client ID** Public identifier for apps unique across all clients that the auth server handles.

**Client Secret** Is a secret used by the OAuth Client to Authenticate to the Authorization Server. The Client Secret is a secret known only to the OAuth Client and the Authorization Server. Client Secret must be sufficiently random to not be guessable.

**Authentication Endpoint** Security mechanism to make sure that only authorized devices can connect.

**Access Token Endpoint** The token endpoint is where apps make a request to get an access token for a user.

**API Endpoint** One end of the communication channel between a client and the api (the api end).

**Authorization Code** The code the client sends to the auth api to get an access token.

**Access Token** The token we use to to make api calls on behalf of the authenticated user.


# Preparation Materials

## [JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo)

## [Intro to JWT](https://jwt.io/introduction/)

## [Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

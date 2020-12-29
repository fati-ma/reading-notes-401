# Readings: Advanced Mongo
## Read: 04 - Class 04

### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-04.md).


## Review, Research, and Discussion

### For this class, I will provide answers for the following questions:

1. **Why would a developer choose to make data models?**
Data models accelerate development, reduce maintenance, increase application quality, and lower execution risks. It is basically the blueprint for a building, outlining all of the details that will result in the proper operation of the application.

2. **What purpose do CRUD operations serve?**
This is a shortcut for Create, Read, Update and Delete. Those are the main operations that we can perform on a database.

3. **What kind of database is Postgres? What kind of database is MongoDB?**
Postgres is SQL and MongoDB is NoSQL

4. **What is Mongoose and why do we need it?**
Mongoose is a package or library that used to work with MongoDB in NodeJs. It helps in writing less code in easier way.


## Vocabulary Terms

**database**
Database is a file contains one table or more. These tables contain a well-organized data. This data’s source vary. It can be a user input, statistics from a website or data from a hospital. We use database for saving, retrieving, updating or deleting data.

**data model**
Data model is a folder that contains model files. Each model file define how data is connected to each other and how they are processed and stored inside the system.

**CRUD**
This is a shortcut for Create, Read, Update and Delete. Those are the main operations that we can perform on a database.

**schema**
Shema is a description for a structure. If we said that this file should follow this schema, this means the file should contain the information’s and datatypes as specified in the schema.

**sanitize**
means that you remove all dangerous characters from an input string before passing it to the SQL engine.

**Structured Query Language (SQL)**
Sometimes we called it Relational Database. The main features in SQL that it can join more than one table to make a query from more than one table in one query. This join process depends in the ability pf making relations between tables. The other feature in SQL that any data record should follow strict predefined schema.

**Non SQL (NoSQL)**
Sometimes we called it non-Relational Database. The main features in SQL that there is no need to join more than one table to make a query from more than one table in one query. The other feature in SQL that any data record should not follow strict predefined schema. This means a flexible way off adding data to DB.

**MongoDB**
MongoDB is one of the famous NoSQL databases. It is easy to use and you can store you database cloud instead of storing it locally in your device.

**Mongoose**
Mongoose is a package or library that used to work with MongoDB in NodeJs. It helps in writing less code in easier way.

**record**
In SQL databases, record is a row in the database that contains a data for a specific object.

**document**
In NoSQL databases, document is the alternative of record in SQL databases. This means it is a raw in the database that contains a data for a specific object.

**Object Relation Mapping (ORM)**
In computer science is a programming technique for converting data between incompatible type systems using object-oriented programming languages.


## Preview

1. **Which 3 things had you heard about previously and now have better clarity on?**
SQL, NoSQL, MongoDB

2. **Which 3 things are you hoping to learn more about in the upcoming lecture/demo?**
Mongoose, MongoDB, NoSQL

3. **What are you most excited about trying to implement or see how it works?**
Full app using MongoDB 

## Preparation Materials

1. [The Repository Design Pattern](https://cubettech.com/resources/blog/introduction-to-repository-design-pattern/)
Repository pattern separates the data access logic and maps it to the business entities in the business logic. Communication between the data access logic and the business logic is done through interfaces. To put it simply, Repository pattern is a kind of container where data access logic is stored. It hides the details of data access logic from business logic. In other words, we allow business logic to access the data object without having knowledge of underlying data access architecture. The separation of data access from business logic have many benefits. Some of them are: • Centralization of the data access logic makes code easier to maintain • Business and data access logic can be tested separately • Reduces duplication of code • A lower chance for making programming errors

2. [In Memory Database Testing](https://dev.to/paulasantamaria/testing-node-js-mongoose-with-an-in-memory-database-32np)
Pros:
- No need for mocks: Your code is directly executed using the in-memory database, exactly the same as using your regular database.
- Faster development: Given that I don't need to build a mock for every operation and outcome but only test the query, I found the development process to be faster and more straightforward.
- More reliable tests: You're testing the actual code that will be executed on production, instead of some mock that might be incorrect, incomplete or outdated.
- Tests are easier to build: I'm not an expert in unit testing and the fact that I only need to seed the database and execute the code that I need to test made the whole process a lot easier to me.

Cons:
- The in-memory database probably needs seeding
- More memory usage (dah)
- Tests take longer to run (depending on your hardware).

3. [mongo memory server](https://www.npmjs.com/package/mongodb-memory-server)


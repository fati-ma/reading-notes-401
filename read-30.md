# Readings: Hash Tables
## Read: 30 - Implementation: Hash Tables
### Hello this is ***Fatima*** :smile:, welcome to my blog where I will share with you the notes I take during reading from the resources provided each class. :closed_book: :pencil2:
### You can visit my GitHub repo for the readings notes from [here](https://github.com/fati-ma/reading-notes-401) or this webpage markdown file using this [link](https://github.com/fati-ma/reading-notes-401/blob/main/read-30.md).


# What Hash Tables are

Hashtables are a data structure that utilize key value pairs. This means every `Node` or `Bucket` has both a key, and a value.


# How they work

The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a `hash`. A `hash` is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time complexity. This is ideal when quick lookups are required.


# Collisions 

What would happen if two different keys resolved to be the same index of the array? This is called a `collision`. The hash map needs to be able to handle two keys resolving to the same index.

Collisions are solved by changing the initial state of the buckets. Instead of starting them all as null we can initialize a LinkedList in each one! Now if two keys resolve to the same index in the array then their key/value pairs can be stored as a node in a linked list. Each index in the array is called a “bucket” because it can store multiple key/value pairs.


# How they are implemented 

1. An element is converted into an integer by using a hash function. This element can be used as an index to store the original element, which falls into the hash table.
2. The element is stored in the hash table where it can be quickly retrieved using hashed key.
```
hash = hashfunc(key)
index = hash % array_size
```
In this method, the hash is independent of the array size and it is then reduced to an index (a number between 0 and array_size − 1) by using the modulo operator (%).


# Visualization

![hash](https://d18l82el6cdm1i.cloudfront.net/uploads/34EvJ7agjl-hash_table.gif)


### Resources

- [Intro to Hash Tables](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)
- [what is a hash table?](https://www.youtube.com/watch?v=MfhjkfocRR0)
- [basics of hash tables](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)
- [hash table wiki](https://en.wikipedia.org/wiki/Hash_table)

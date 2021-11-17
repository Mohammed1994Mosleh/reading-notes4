# class230 Reading Notes:Hash Tables

![Hash Tables](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d0/Hash_table_5_0_1_1_1_1_1_LL.svg/450px-Hash_table_5_0_1_1_1_1_1_LL.svg.png)

### What is Hash

- Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

- Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

- Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

- Why do we use them?

1. Hold unique values
2. Dictionary
3. Library

### How to utilize Hashmap:


* Hamap has complixity O(1) for time

- accept a key

- calculate the hash of the key

- use modulus to convert the hash into an array index

- use the array index to access the short LinkedList representing a bucket

- search through the bucket looking for a node with a key/value pair that matches the key you were given

- Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

- Hash Maps can have any number of buckets. If a hash map has only a few buckets it will be densely full and have many collisions
- Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.


### Internal Methods:

- Add() When adding a new key/value pair to a hashtable:

1. send the key to the GetHash method.
2. Once you determine the index of where it should be placed, go to that index
3. Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
4. If something does exist, add the new key/value pair to the data structure within that bucket.


- Find() The Find takes in a key, gets the Hash, and goes to the index location specified. 

- Contains() The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. 

- GetHash() The GetHash will accept a key as a string, conduct the hash, and then return the index of the array  where the key/value should be placed.
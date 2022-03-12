# Read: 30 - Hash Tables - 03/12/2022

1. Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
2. Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collison occurs.
3. Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.
4. Hashtable - A data structure that utilize key value pairs. This means every `Node` or `Bucket` has both a key, and a value.
5. Internal Methods
   - Add() - Adding a new key/value pair to a hashtable
   - Find() - takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the reponsibility of the algorithm the iterate throught the bucket and see if the key exists and return the value.
   - Contains() - will accept a key, and return a boolean on if that key exists inside the hashtable
   - GetHash() - will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.

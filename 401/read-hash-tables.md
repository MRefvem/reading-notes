# Read: Hash Tables

## Hashtables

### What is a Hashtable?
1. Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
2. Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
3. Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

### Why do we use Hashtables?
1. Hold unique values
2. Dictionary
3. Library

### What are they?
Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key and a value.

The basic idea of a hashtable is the ability to store the key into this data structure, and quickly retrieve the value. This is done through what we call a hash. A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time complexity. This is ideal when quick lookups are required.

### The difference between Arrays and Hashtables
Arrays actually have fast access. If we know the index of the information we want we can access that information in the O(1) time. The reason why searching for a piece of data in a collection is O(N) isn't because the array is slow, it's just that we have to look through all N things in the collection.

Hash maps take advantage of an array's O(1) read access. Instead of adding elements to an array from beginning to end, a hash map uses a "hash function" to place each item at a precise index location, based off it's key.

### Hashing
Basically, a hash code turns a key into an integer. It's very important that hash codes are deterministic: their output is determined only by their input. Hash codes should never have randomness to them. The same key should always produce the same hash code.

A hashtable is created from an array.

Here is one suggestion on how to has data:
1. Add or multiply all the ASCII values together.
2. Multiply it by a prime number such as 599.
3. Use modulo to get that remainder of the result, when divided by the total size of the array.
4. Insert into the array at that index.

Example:
```
Key = "Cat"
Value = "Josie"

67 + 97 + 116 = 280

280 * 599 = 69648

69648 % 1024 = 16

Key gets placed in index of 16.
```

Now that we know that our key, Cat, maps to index 16 of the array. We can view into this index and find "Josie", our value quickly.

### Collisions
A collision occurs when more than one key hashes to the same index in an array.
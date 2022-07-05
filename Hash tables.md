## Hash tables
These are really common.

These are key-value pair stores

Keys in hashmaps/ tables are put through a hashing function to produce a number to store the value against

remember idempotency? All hash functions should be idempotent (bcrypt is different per machine)

The hash function creates a memory address for the key to store the value (and the key often too) in memory.

Hashing taking a while could cause a bottleneck on performance. Langs generally implement their own hashing functions that are performant. We assume a big O of O1 (constant time) for the hash.

As the hash table isn't ordered, all ops (insert, lookup, delete) are all constant time.

Collisions on keys can occur when the hash function generates a value that matches an already assigned memory address in the hash table. When this happens, the keys and values of each pair are then stored in a linked list.

When the above happens, the big O becomes O(n) or linear time.

Javascript has M  aps and allows you to save expressions as keys. it also maintains insertion order (like the Set does)
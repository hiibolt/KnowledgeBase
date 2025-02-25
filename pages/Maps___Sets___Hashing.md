## Set
An *abstract data type* where elements are stored uniquely. Can be ordered and unordered.

**Insertion**: $$O(\log{n})$$
**Removal**: $$O(\log{n})$$
**Find**: $$O(\log{n})$$
**Size**: $$O(1)$$
- ## Map
  A *key-value pair* based collection.
  * `std::map` stores similarly to Rust's `BTreeMap`
  All operations for this datatype are $$O(\log{n})$$. Requires comparability.
  
  * `std::unordered_map` stores similarly to Rust's `HashMap` (quicker as it uses hashes for access)
  All operations are $$O(1)$$ on average for this datatype, except when there are hash collisions ($$O(n)$$ to rebuild). There is notable overhead for hash table buckets. Requires a hashing function for keys.
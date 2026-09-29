#CS2DA
- A **Hash Table** is an array, where each entry(bucket) holds a **Linked List**
- Each entry is made up of a key-value pair (`Entry<k, v>`), and supports the following operations:
	- `insert(k, v)` -> Maps the key `k` to the value `v` 
		- Pseudo code: `table[hash(k)] = {k, v} `
	- `get(k)` -> produces the associated value `v`
		- Pseudo code: `if: table[hash(k)] = {k, v} then return v else return nothing`
	- `remove(k)` -> removes the key `k` and its associated value
		- Pseudo code: `if table[hash(k)] = {k, _ } then table[hash(k)] = empty`
- Hashcode is the integer produced when running a key through the `hash()` method, used to determine **which entry a key belongs in**
- Hashing (`hash()`)only decides **where** a pair goes: the key is run through `hash()` to produce an index, which picks the bucket. The bucket then stores the whole **key-value pair**.
	- `insert("cat", 5)` -> `hash("cat")` = 3 -> store `{"cat", 5}` in bucket 3
	- `get("cat")` -> `hash("cat")` = 3 -> go to bucket 3 -> find the entry with the matching key -> return its value
>[!Collision]
> A collision can occur when 2 different keys hash to the same index.  To solve this, a linked list is created inside of the entry in order to store 2 key-value pairs 
## Creating a Hash Function
- There are different ways of creating a hash() method depending on the type of keys: 
	 - **Integer keys**:  Modulus (%) with table size (M)
	 - **String keys**: (where M refers to the number of entries and R refers to a prime constant multiplier)
```Java
int hash = 0;
for(int i = 0; i < s.length(); i++) {
	hash = (R * hash + s.charAt(i)) % M;
}
``` 
- However, Java does include a default `hashCode()` method that achieves the same purpose as `hash()`
- 

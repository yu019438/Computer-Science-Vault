#CS2DA
- A **Hash Table** is an array, where each bucket (index in the array) holds a **Linked List** -> within which entries are stored
- Each entry is made up of a key-value pair (`Entry<k, v>`), and supports the following operations:
	- `insert(k, v)` -> Maps the key `k` to the value `v` 
		- Pseudo code: `table[hash(k)].insert(k, v) `
	- `get(k)` -> produces the associated value `v`
		- Pseudo code: `return table[hash(k)].get(k)`
	- `remove(k)` -> removes the key `k` and its associated value
		- Pseudo code: `table[hash(k)].remove(k)`
- Hashcode is the integer produced when running a key through the `hash()` method, and is used to determine **which index the key belongs to**
	- Using the `hash()` method only decides **where** a pair goes: the key is run through `hash()` to produce an index, which picks the bucket. The bucket then stores the whole **key-value pair**:
		- `insert("cat", 5)` -> `hash("cat")` = 3 -> stores `{"cat", 5}` in bucket 3
		- `get("cat")` -> `hash("cat")` = 3 -> go to bucket 3 -> find the entry with the matching key -> return its value
## Collision
The bucket linked list will usually hold 0 or 1 key-value entry, unless a collision occurs
- A collision occurs when 2 or more different keys hash to the same index, meaning a bucket will store more than one key-value pair -> *this is why each bucket is a linked list*
- To solve this,  the most recent key is stored at the front of the linked list bucket
## Creating a Hash Function
- There are different ways of creating a `hash()` method depending on the type of keys: 
	 - **Integer keys**:  Modulus (%) with table size (M)
	 - **String keys**: (where M refers to the number of buckets and R refers to a prime constant multiplier)
```Java
int hash = 0;
for(int i = 0; i < s.length(); i++) {
	hash = (R * hash + s.charAt(i)) % M;
}
``` 
- However, Java includes a default `hashCode()` method that produces an integer used to determine which bucket an entry is stored in
---
## Time complexity in Hash Tables
- **Best Case**: Buckets are evenly distributed with 0 or 1 entry per bucket, resulting in fast constant-time performance where operations do not depend on data size
- **Worst Case**: All keys collide and hash to the same bucket, turning the structure into a single linked list where operations slow down significantly
- **Average Case**: With a 'good' choice of hash function, all operations (`insert`, `get`, `remove`) are typically **constant time** and do not depend on the size of the data structure
---
## Hash Table Size
- In the case of Hash Tables, there is a space-time trade off -> Increasing the table size (number of buckets) reduces the likelihood of collision, thus reducing time.  However, the increase in table size consumes more memory
- **Dynamic Resizing**: Library implementations typically monitor how full the table is and **resize it** if most buckets are used
- Resizing requires the **recalculation of all hash values** across the table
---
## Security Risks & Vulnerabilities
- **Denial of Service (DoS) via Collisions**: An attacker who knows the hash implementation could feed in deliberately bad data designed to trigger massive collisions, degrading program performance from constant time to quadratic time
- **Mitigation**: Use a balanced binary tree instead of a linked list (or instead of the hash table) to handle potential worst-case performance spikes safely
---
>[!Video revision]
>Here is a great explanation of Hash Tables with examples by BroCode:
>https://www.youtube.com/watch?v=FsfRsGFHuv4
---
## Related
## Covered in
- [[CS2DA_week_01_lecture.pdf]]

#CS1IP
A for-each loop is a loop used to iterate over every element of a collection (array, List, Set etc.) without the need for an index. 
```Java
for (Type variable : collection) {
    // use variable
}
```
For example: 
```Java
int[] arr = {1, 2, 3}
for(int x : arr) {
	System.out.println(x);
}
```
*..."For each `int x `in `arr`"*...

---
## Key points
- No index: direct access to each element without needing its position
- Not array specific (can work on Lists/sets etc.)
- Use standard for-loop instead if you need: index, to loop backwards, to modify array elements directly
---
## Related
- [[Iteration - For & While]]
- [[Arrays]]
## Covered in 
- [[CS1IP_week_05_lecture.pdf]]
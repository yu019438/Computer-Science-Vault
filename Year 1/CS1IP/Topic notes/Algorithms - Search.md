#CS1IP
## Time Measurement
- We can measure time in Java in order to identify the slowest parts of an algorithm in order to optimise its performance
``` Java
long startTime = System.currentTimeMillis();
algorithm(input);
long time = System.currentTimeMillis() - startTime;
```
## Linear Search
- Linear search is a search algorithm that checks each element in a list until the desired element has been found or the list ends.  
- For example: 
	1. Check index 0, determine whether a match has been found
	2. Move to next index and repeat until target is located or the list ends
```Java 
int linearSearch(ArrayList<Integer> list, int target) {
	for(int i = 0; i< list.size(); i++) {
		if(list.get(i) == target) {
			return i;
		}
	}
	return -1;
}
```
### Time Complexity:
- **Best case**: $O(1)$ first element == target
- **Worst case**: $O(log$ $n)$ last element == target || target not found
---
## Binary Search
- Binary search is a search algorithm that checks each elements in a sorted array until the desired element has been found or the list ends
- The array must first be sorted, then, during the sorting process the Array is divided in half to reduce the search data
- Search is conducted in both halves before data is combined again
- For example:
	1. Array = [2, 5, 8, 12, 16, 23, 38, 56, 72, 91] / target = 23
	2. Data is separated in the middle -> 23 > 16 therefore first half is discarded and search continues in the remaining half of the data
	3. The above step is repeated on the remaining data until the target element is found or the end of the Array is reached
```Java
int binarySearch(ArrayList<Integer> list, int target, int left, int right) {
	if (left > right) {
		return -1; //Base case: target not found
	}
	int mid = left + (right - left) / 2;
	
	if (list.get(mid) == target) {
		return mid; //Target found at the mid index
	}
	else if (target > list.get(mid)) {
		return binarySearch(list, target, mid + 1, right);//Search right
	}
	else {
		return binarySearch(list, target, left, mid - 1);//Search left
	}
}
```
- `left` = starting index of the Array
- `right` = Last index
- `mid` = Middle index (that is compared to the target)
```Java
ArrayList<Integer> intList = new ArrayList<>(List.of(5, 2, 16, 12, 8));
int target = 42;
Collections.sort(intList); //Sorts Array
int result = binarySearch(numbers, target, 0, numbers.size() -1);

if (result == -1) {
	System.out.println("Element not present");
}
else {
	System.out.println("Element found at index: " + result)
}
```
### Time Complexity:
- **Best case**: $O(1)$ target is in the centre of the Array
- **Worst cast**: $O(log$ $n)$ target is found in the last subdivision
---
## Linear vs Binary Search

| Feature        | Linear Search     | Binary Search         |
| :------------- | :---------------- | :-------------------- |
| **Input**      | No specific order | Requires sorted input |
| **Best Case**  | $O(1)$            | $O(1)$                |
| **Worst Case** | $O(n)$            | $O(log$ $n)$          |
- **Linear Search**: Simpler but slower on larger data sets
- **Binary Search**: More efficient for sorted arrays (required)

**-> View lecture notes for example measurement of linear/binary search walk-through**

---
## Related
- [[Algorithms - Big-O Notation]]
## Covered in
- [[CS1IP_week_09_lecture.pdf]]

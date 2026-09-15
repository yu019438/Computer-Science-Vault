#CS1IP 
Merge Sort, similar to Binary Search, is a 'Divide and Conquer' algorithm that splits the array, sorts it and merges the sorted sub divisions back together:
1. Array is spit in half using the `mergeSort` function
2. Each half is split again until sub divisions contain only 2 elements
3. Each subdivision is ordered individually (skipped if elements are already in order)
4. Gradually as more subdivisions are order they are merged back together using the merge `function`
5. Eventually the 2 halves are each sorted and a final merge combines them into a single, sorted array
```Java
void mergeSort(int[] data, int left, int right) {
	if((right - left) >= 1) {
		int middle1 = (left + right) / 2;
		int middle2 = middle1 + 1;
		mergeSort(data, left, middle1);
		mergeSort(data, middle2, right);
		merge(data, left, middle1, middle2, right);
	}
}
```
- `mergeSort(data, left, middle1)` handles sorting the left subdivision
- `mergeSort(data, middle2, right)` handles sorting the right subdivision
```Java
void merge(int[] data, int left, int middle1, int middle2, int right) {
	int leftIndex = left;
	int rightIndex = middle2;
	int combinedIndex = left;
	int[] combined = new int[data.length];
	//Merge arrays until reaching end of either
	while(leftIndex <= middle1 && rightIndex <= right) {
		if(data[leftIndex] <= data[rightIndex]) {
			combined[combinedIndex++] = data[leftIndex++];
		}
		else {
			combined[combinedIndex++] = data[rightIndex++];
		}
	}
	//If left array is empty
	if (leftIndex == middle2) {
		while(rightIndex <= right) {
		combined[combinedIndex++] = data[rightIndex++];
		}	
	}
	//If right array is empty
	else {
		while(leftIndex <= middle1) {
			combined[combinedIndex++] = data[leftIndex++];
		}
	}
	//Copy values back into original array
	for(int i = left; i <= right; i++) {
		data[i] = combined[i];
	}
}
```
- Comparison of elements is done using `leftIndex` and `rightIndex`
```Java
int[] numbers = {4, 7, 2, 6, 8, 5};
mergeSort(numbers);

System.out.println("Sorted Array: ");
for(int num : numbers) {
	System.out.println(num + " ");
}
```
---
### Time Complexity:
- **Best case**: $O(n$ $log$ $n)$:
	- `MergeSort` always divides the array in half
	- It is run regardless of how the data is already sorted
	- the merging process takes linear time $O(n)$for each level of recursion
- **Worse case**: 
	- MergeSort has the same time complexity in all cases, as the divide and conquer approach is consistent regardless of the initial input list/array
---
## Related
- [[BubbleSort]]
- [[BubbleSort vs MergeSort]]
## Covered in
- [[CS1IP_week_10_lecture.pdf]]

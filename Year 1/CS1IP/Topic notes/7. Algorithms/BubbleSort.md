#CS1IP 
Bubble Sort is the process of sorting elements of a  list/array into a certain order:
1. Iterate through the list
2. Compare adjacent elements
3. Swap those elements that are out of order
4. Repeat until the list is sorted
```Java
void bubbleSort(int[] array) {
	int n = array.length;
	boolean sorted = true;
	for (int i = n - 1; i >= 0; i--) {
		for (int j = 0; j < n - 1; j ++) {
			if (array[j] > array[j + 1]) {
				int temp = array[j];
				array[j] = array[j + 1];
				array[j + 1] = temp;
				sorted = false;
			}
		}
		if (sorted) {
			break;
		}
	}
}
```
### Time Complexity:
- **Best case**: $O(n)$ Array already sorted
- **Worst case**: $O(n^2)$ Each pair of numbers needs switching *(Array begins sorted in descending order)*
**-> Read through lecture notes for step-by-step example**
---
## Related
- [[MergeSort]]
- [[BubbleSort vs MergeSort]]
## Covered in
- [[CS1IP_week_10_lecture.pdf]]


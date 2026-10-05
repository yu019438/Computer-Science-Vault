#CS2DA
- Like merge sort, quick sort is divide and conquer -> but it arranges the elements first (partitioning around a pivot) and then recurses, whereas merge sort splits first and arranges the elements afterwards (merging)
- The key feature of quick sort is the use of a pivot -> The pivot (`p`) is an element chosen from the beginning, middle or end of an array and creates a partition, splitting it in two
## How does it work
1. Select a pivot (beginning, middle, end) and partition the remaining data around it -> Elements **smaller** than the pivot go to its left, elements **larger** go to its right:
	- For example: `[7, 2, 9, 4, 5]` With 5 as the pivot -> `[2, 4]` `5` `[7, 9]`
2. Of the remaining items on the left side, another pivot is chosen which partitions the remaining data like before. This is also continued on the right side *(unless the largest element was chosen as the pivot)*
3. Continue this step until there are either 1 or 0 numbers in a sublist
4. After partitioning, the pivot is already in its final sorted position, so once every sublist is sorted no merge step is needed
## Time Complexity in Quick Sort
- **Best case**: $O(n$ $log$ $n)$ -> Each partition creates 2 equal halves
- **Worst case**: $O(n^2)$ -> When the pivot is chosen to be either the smallest or largest element, meaning the remaining data is all allocated to either the left or right but not both
- **Average case**: $O(n$ $log$ $n)$ -> This is what makes quick sort so efficient - the average case shares the same time complexity as the best case
---
>[!Video Revision]
>Here is a quick breakdown of how quick sort works with a visual example:
>https://www.youtube.com/watch?v=XE4VP_8Y0BU
---
## Related
- [[MergeSort]]
## Covered in
- [[CS2DA_week_01_lecture.pdf]]
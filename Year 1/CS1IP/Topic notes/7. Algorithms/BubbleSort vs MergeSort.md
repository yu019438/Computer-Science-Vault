#CS1IP 
We can compare BubbleSort and MergeSort in order to understand the differences in sorting methods; simplicity vs efficiency:
- `BubbleSort`: $O(n^2)$
- `MergeSort`: $O(n$ $log$ $n)$
### Generating Test Data
```java
void generateSortInput(String filename, int count) throws IOException {
    Random rand = new Random();
    FileWriter writer = new FileWriter(filename);
    for (int i = 0; i < count; i++) {
        writer.write(rand.nextInt(10000) + "\n");
    }
    writer.close();
}

generateSortInput("sort10.txt", 10);
generateSortInput("sort100.txt", 100);
generateSortInput("sort10000.txt", 10000);
```
### Measuring Runtime
Assume `measureBubbleSort` and `measureMergeSort` each read a file, time how long the corresponding sort takes, and return that duration.
```java
long measureMergeSort(String filename) throws IOException { ... }
long measureBubbleSort(String filename) throws IOException { ... }
```

```java
System.out.println("BubbleSort:");
measureBubbleSort("sort10.txt");
measureBubbleSort("sort100.txt");
measureBubbleSort("sort10000.txt");

System.out.println("MergeSort:");
measureMergeSort("sort10.txt");
measureMergeSort("sort100.txt");
measureMergeSort("sort10000.txt");
```
### Results

| Input size | BubbleSort | MergeSort |
|-----------|-----------|-----------|
| 10        | ~0        | ~0        |
| 100       | ~30ms     | ~1ms      |
| 10,000    | ~2000ms   | ~20ms     |

As input size grows, BubbleSort's runtime shoots up sharply while MergeSort stays close to flat -> demonstration of
`O(n²)` vs `O(n log n)`.
![[Pasted image 20260912194437.png]]

---
## Takeaway
- **BubbleSort**: simple to implement and understand, but scales badly.  Fine for small or nearly-sorted datasets.
- **MergeSort**: more complex to implement, but scales much better for large datasets. The standard choice when performance matters.
---
## Related
- [[BubbleSort]]
- [[MergeSort]]
## Covered in
- [[CS1IP_week_10_lecture.pdf]]
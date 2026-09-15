#CS1IP 
## Built-in sorting [[methods]] in Java
`Arrays.sort()` -> Sorts arrays
```Java
int[] numbers = {6, 5, 8, 1};
Arrays.sort(numbers);
System.out.println(Arrays.toString(numbers)); //[1, 5, 6, 8]
```

`Collections.sorts()` -> Sorts collections
```Java
var numbers = new ArrayList<Integer>(List.of(6, 5, 8, 1));
Collection.sort(numbers);
System.out.println(numbers); //[1, 5, 6, 8]
```
## Comparators
### Java inline comparator 
Comparators allow users to define customer sorting logic within the `Arrays.sort()` or `Collections.sort()`
### Inline Comparator Syntax
- The pattern is always: create an anonymous `Comparator` object ->  implement `compare()` with whatever logic you want. 
- Whichever value comes out negative/zero/positive decides the order (same idea as `compareTo()`):
```java
Arrays.sort(names, new Comparator<String>() {
    public int compare(String o1, String o2) {
        return o1.compareTo(o2);
    }
});
```
- Same idea for `Collections.sort()` just swap the array for a list.
### Sorting Numbers Ascending/Descending
- Flipping the order is just a case of swapping which value you subtract from which:
```java
// Ascending
Collections.sort(numbers, new Comparator<Integer>() {
    public int compare(Integer a, Integer b) {
        return a - b; //b - a for descending
    }
});
```
- You can also compare elements by other characteristics, *i.e. String length*:
```java
Collections.sort(words, new Comparator<String>() {
    public int compare(String a, String b) {
        return a.length() - b.length();
    }
});
```
### Worked example: student IDs (format: `AB123456`, two letters + six digits)
The same list but two can have 2 different comparators applied depending on what criteria the list is being sorted by:
- Sort by the **numeric** part only -> extract `substring(2)`, parse to int, compare
- Sort by the **letter prefix** only -> extract `substring(0, 2)`, compare as strings
- A comparator lets you sort the *same objects* in completely different ways depending on which part of the data you extract for comparison
## Parallel Sorting
`Arrays.parallelSort()` is the same as `Arrays.sort()` but splits the work across multiple processor threads in order to **boost performance**.  This is worth using on larger datasets:
```java
int[] largeArray = {5, 2, 8, 1, 3};
Arrays.parallelSort(largeArray);
System.out.println(Arrays.toString(largeArray));
```
---
## Related
- [[Arrays]]
- [[Collections]]
## Covered in
- [[CS1IP_week_10_lecture.pdf]]

#CS1IP
## Algorithms
- An algorithm is a step-by-step procedure designed to perform a specific task/ solve a particular problem
- E.g. Finding the maximum number in an `int` Array:
	- Initialise variable `max` to the first element
	- Iterate through the array and compare each element with `max`
	- When `max` encounters a bigger number, reassign `max`
	- Once all elements have been compared, return `max`
- What makes a good algorithm:
	- An algorithm must terminate after a certain number of iterations to avoid running forever
	- Each step should be clear-cut and unambiguous 
	- ^ As well as this, there must be specified inputs/outputs
	- There should be consideration over time and size of the algorithm (is it inflated, running a simple task over a long period of time... inefficient?)
## Time Complexity
- Time complexity refers to the way in which we determine the efficiency of an algorithm.  This is crucial for understanding how an algorithm might scale with input size -> therefore, optimising performance
- In order to properly analyse time complexity, we refer to the best and worse cases:
	- Best case: When the algorithm performs the fewest operations
	- Worst case: When the algorithm performs the greatest possible number of operations
---
## Big-O Notation
This is the mathematical notation used to define the worse-case scenario of an algorithm's performance in relation to input size: 
### 1. $O(1)$: Constant time
e.g. Searching element-by-element
```Java
int getFirstElement(int[] arr) {
	return arr[0];
}
```
### 2. $O(n))$: Linear time
e.g. Summing elements in an array
```Java
int sumArray(int[] arr) {
	int sum = 0;
	for(int i = 0; i < arr.length; i++) {
		sum += arr[i];
	}
}
```
### 3. $O(n^2)$: Quadratic
e.g. Nested loops - printing pairs of elements
```Java
void printPairs(int[] arr) {
	for(int i = 0; i < arr.length; i++) {
		for(int j = 0; j < arr.length; j++) {
			System.out.println(arr[i] + ", " + arr[j])
		}
	}
}
```
NOTE: Doesn't have to apply to just nested loops
### 4. $O(log$ $n)$: logarithmic time
e.g. Count the number of digits in an integer -> number of digits in int n is approximately $log10(n)$
```Java
int countDigits(int n) {
	int count  = 0;
	while(n > 0) {
		n = n / 10;
		count ++;
	}
	return count;
}
System.out.println(countsDigits(123456)); //Output 6
System.out.println(countDigits(1000)); //Output 4
```
### Other common Big-O notations include:
- $O(n$ $log$ $n)$ -> log-linear time
- $O(2^n)$ -> Exponential time
- $O(n!)$ -> Factorial time
**-> View lecture notes for diagram ranking Big-O notations from bad-good**
---
## Optimising Code
- Reduce nested loops
- Efficient data structure
- Avoid unnecessary computation
---
## Related
- [[Algorithms - Comparing Algorithms]]
- [[Algorithms - Search]]
## Covered in
-  [[CS1IP_week_09_lecture.pdf]]
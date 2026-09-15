#CS1IP 
An Array is a collection of elements (of the same [[Data Types|data type]]) stored in 'contiguous' memory -> Arrays have a **fixed size** (number of elements) that is specified when initialised:
- Int array: `0, 1, 1, 2, 4`
- Double array: `0.5, 1.5, 2.5, 8.5`
- String array: `Hello, Bonjour, Hola`
- Boolean array: `True, False, False, True`
**-> An array can NOT mix data types**
## Declaring/allocating an Array
- Syntax:
```Java
TYPE[] VAR_NAME = new TYPE[SIZE]
```
- For example:
```Java
int[] arr = new int[5]; //int array [0, 0, 0, 0, 0]
String[] arr = new String[5]
```

- ^ The keyword new is used to allocate computer memory 
- You can't edit the size an an array, but you can reallocate to increase/decrease size:
```Java
int[] arr = new int[5] //[0, 0, 0, 0, 0]
arr = new int[3] // [0, 0, 0]
```
- If the required size isn't known upfront, one option is to over-allocate for a worst-case size (e.g. `new int[100]`). A more common approach is using an `Arraylist` (see [[Collections]], Week 7)
## Indexing
- Arrays have 0-based indexing, meaning the first element is `0`, and the last element is `array length - 1`
- Trying to access an index outside of the defined range (e.g. the 4th element in an array of 3 elements) with present an IndexOutOfBoundsException
## Array as the parameter and return of a method
```Java
int[] incrementArray(int[] numbers) {
	int[] incrementedArray = new int[numbers.length];
	for (int i = 0; i < numbers.length; i++) {
		incrementedArray[i] = numbers[i] + 1;
	}
	return incrementedArray;
}
```
- **Array as the parameter**: An array is being passed into the [[Methods|method]] as an argument 
- **Array as the return**: The method gives an array as output rather than a single value
---
## Initialisation 
Typically, an array has to be initialised before used in Java:
```Java
int[] arr; //Declaration
arr = new int[5]; //Allocation
arr[0] = 1; //Initialising first element
arr[1] = 2; //Initialising second element
arr[2] = 3; //Initialising third element
```
- The above can be written in the following shortcut `int[] arr = {1, 2, 3}`
- Initialising arrays with other data types is done in an identical manner
- Default initialisation for each data type: 
```Java
int[] arr1 = new int[3]; //[0, 0, 0]
double[] arr2 = new double[3]; //[0.0, 0.0, 0.0]
boolean[] arr3 = new boolean[3]; //[False, False, False]

```
- By default, Java does **not** provide a default initialisation for `String` arrays:
```Java
String[] arr4 = new String[3]
System.out.println(Arrays.toString(arr4)); //[null, null, null]
```
- The default initialisation is technically null, but not a usable `String` value

> [!info] Displaying Arrays
> Arrays.toString() is the built in method that converts the array to a readable String -> otherwise you get something like: [I@1b6d3586]
## Loop through Arrays
To iterate (loop) through Arrays, you must remember that Java has 0-based indexing
- Iterate `0` to `array length` -> accessed with `ARRAY_NAME.length`:
```Java
int[] arr = {1, 2, 3, 4, 5};
System.out.println(arr.length); //5
```
- Use a `for loop` to iterate through the array:
```Java
int[] arr = {1, 2, 3, 4, 5};
for(int i = 0; i < arr.length; i++) {
	System.out.println(arr[i]);
}
```

Array has a length property while String has a length() method:
```Java
String[] str = {"a", "b", "c"};
for(int i = 0; i < str.length; i++) {
	System.out.println(str[i]);
}
```
---
## Best practices
*-> Refer to the lecture notes for a set of best practices when using arrays, including thought process and other properties*

---
## Covered in
- [[CS1IP_week_05_lecture.pdf]]

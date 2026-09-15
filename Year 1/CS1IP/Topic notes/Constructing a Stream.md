#CS1IP
The stream pipeline is an operation that is composed of:
- The source
- Intermediate operations
- Terminal operations
## The Source
The source refers to the collection or array that is being streamed. For example:
- `IntStream.rangeClosed()`
- `IntStream.range()`
- `array_object.stream()`
- `collection_objection.stream()`
## Intermediate Stream Operations
An intermediates stream operation transforms elements in the stream:
- `map()` -> applies a method to each element:
```Java
//Traditional 
int total = 0;
for (int i = 1; i <= 5; i++) {
	System.out.println(i * 2 + " " );
}

//With Stream
IntStream.rangeClosed(1, 5).map(n -> n*2).forEach(System.out::println);

//Or with an Array (also stream)
int[] numbers = {1, 2, 3, 4, 5};
int[] doubled = Arrays.stream(numbers).map(n -> n * 2).toArray();
System.out.println(Arrays.toString(doubled));

```
- `filter()` -> selects an elements to match a condition:
```Java
//Traditional
String[] names = {"Alice", "Bob", "Sam"};
for (String name : names) {
	if (name.startsWith("A")) {
		System.out.println(name);
	}
}

//With Stream
String[] names = {"Alice", "Bob", "Sam"};
names.stream().filter(name -> name.startsWith("A")).forEach(System.out::println);
//Output: Alice
```
- `sorted()` -> sorts elements:
```Java
//Traditional
int[] numbers = {5, 1, 4, 3, 2};
Arrays.sort(numbers);
for(int number : numbers) {
	System.out.print(number + " ");
}
//With Stream
int[] numbers = {5, 1, 4, 3, 2};
Arrays.stream(numbers).sorted.forEach(n -> System.out.print(n + " "));
```
## Terminal Stream Operators
Terminal stream operators are used to produce a result or side effect of the lambda and after the intermediate operator has been declared:
- `forEach()` -> Iterate through each element in the list/array:
- `count()` -> Count the elements in the list/array:
- `sum()` -> Sum elements in the list/array:
- `collect()` -> Gathers elements into a **new collection**:
```Java
var numbers = Arrays.asList(1, 2, 3, 4, 5);
var squares = numbers.stream().map(x -> x * x).collect(Collectors.toList());
System.out.println(squares);
//Output: [1, 4, 9, 16, 25]
```
---
## Related
- [[Lambdas]]
- [[Streams]]
## Covered in
- [[CS1IP_week_11_lecture.pdf]]

#CS1IP
## What is a Stream
A Stream is a sequence of elements supporting sequential/parallel operations -> It does this through the use of:
- Lambdas
- Iteration
## How to Create a Stream
The first part of the Stream is the Source, which can be:
- From a collection -> using the `stream()` method
```Java
var names = new ArrayList(Arrays.asList("Alice", "Bob", "Sam"));
Stream<String> stream = names.stream();
stream.forEach(System.out::println);
```
- From an array -> using the `Arrays.stream()` method with array as the parameter
```Java
String[] fruit = {"Apple", "Banana", "Cherry"};
Arrays.stream(fruit);
```
Streams are created from methods, for example: 
```Java
IntStream.range(1, 5); //[1, 2, 3, 4]
IntStream.rangeClosed(1, 5) //[1, 2, 3, 4, 5] end inclusive
```
^ `IntStream` is a specialised Stream used for `int` values -> `Stream<Integer>` would work with the wrapper object Integer rather than dealing with primitive int values directly -> thus providing a small improvement in performance.
## External vs Internal Iteration
- **External iteration**: A traditional loop in which an iterator `i` iterates through a list
```Java
for(int i = 1; i < 5; i++) {
	System.out.println(i);
}
```
- **Internal iteration**: When you pass a function to a method to iterate through a list
```Java
IntStream.range(1, 5).forEach(System.out::println);
```
- Here's an example of when an internal iteration can be used to replace an external iteration
```Java
int total = 0;
for(int i = 1; i <= 10; i++) {
	total += i;
}
```
- Can be rewritten as: `int sum = IntStream.rangeClosed(1, 10).sum();`
---
## Related
- [[Lambdas]]
- [[Collections]]
- [[Arrays]]
## Covered in
- [[CS1IP_week_11_lecture.pdf]]
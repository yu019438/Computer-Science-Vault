#CS1IP 
### Syntax
A lambda is used to represent an anonymous function (i.e. a function without a name).  This allows you to pass behaviour as a method argument:
- `(parameters) -> function;`, for example: `x -> System.out.println(x);`
This would otherwise have looked like: 
```Java
void print(String x) {
	System.out.println(x);
}
```
You can also use {} to return blocks: `(parameters) -> body: 
```Java
(a, b) -> {
	int sum = a + b;
	return sum;
};
```
### Application
We can apply this to method reference ([[Collections]]) in order to reduce code complexity and improve general readability.  We start with:
```Java
var list1 = new ArrayList<String>(Arrays.asList("a", "b", "c"));
list1.forEach(System.out::println);
```
By using lambdas we get:
```Java
var list1 = new ArrayList<String>(Arrays.asList("a", "b", "c"));
list1.forEach(letter -> System.out.println(letter));
```
Here is another example of lambdas in collections:
```Java
var names = new ArrayList<String>(Arrays.asList("Alice", "Bob", "Sam"));
var upperCaseNames = new ArrayList<String>();

names.forEach(name -> upperCaseNames.add(name.toUpperCase()));
upperCaseNames.forEach(name -> System.out.println(name));

```
We can also use lambdas in maths:
```Java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4);
numbers.replaceAll(n -> n + 1);
numbers.forEach(n -> n = n * 2)
numbers.forEach(System.out::println);

//Output: [2, 3, 4, 5]
```
`forEach` is a void method that hands you a disposable local copy of each element.  Reassigning it is a no-operation effect on the collection. `replaceAll` is different, it's specifically contracted to take your lambda's return value and write it back into the list. That's why `replaceAll(n -> n + 1)` above actually changed `numbers`, but `numbers.forEach(n -> n = n * 2)` did nothing.

---
## Related
- [[Streams]]
- [[Constructing a Stream]]

## Covered in
- [[CS1IP_week_11_lecture.pdf]]
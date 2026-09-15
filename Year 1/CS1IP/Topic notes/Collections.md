#CS1IP
- A collection is a container of objects/elements
- The most common collections include: 
	- **Lists**: Ordered elements
	- **Sets**: Elements are unique -> no duplicates
- Diamond notation is used to determine the type of elements stored in the Set/List
- e.g.`ArrayList<String> items = new ArrayList<>(); //ArrayList of Strings`
### ArrayList
- `ArrayList` is a resizable array that allows for duplicate elements and maintains the order of elements
- Fast access
- Common methods:
	- `get()`
	- `add()`
	- `remove()`
```Java
ArrayList<String> fruit = new ArrayList<>();
fruit.add("Banana");
fruit.add("Apple");
fruit.add("Pear");

System.out.println("Fruit: " + fruit);
fruit.remove("Banana");
System.out.println("Fruit after removal: " + fruit);

String fruit = fruit.get(1);
System.out.println("Fruit at index 1: " + fruit)
```
### LinkedList
- `LinkedList` is a 'doubley linked' list that implements `List` and `Deque` interfaces
- Efficient for adding/removing at the beginning and end of the list
- Slow access, fast inserts/removal
- Common methods: 
	- `addFirst()`
	- `addLast()`
	- `removeFirst()`
	- `removeLast()`
```Java
LinkedList<String> fruits = new LinkedList<>();
fruit.add("Banana");
fruit.add("Apple");
fruit.add("Pear");

System.out.println("Fruit: " + fruit);

fruit.addFirst("mango");
fruit.removeLast();
System.out.println(fruits);
```
### HashSet
- `HashSet` is a set -> it functions like a list but can contain no duplicate elements
```Java
HashSet<String> set = new HashSet<>();
set.add("Dog");
set.add("Cat");
set.add("Bird");
set.add("Dog"); //Won't be added
```
## Var keyword
The `var` keyword is used to reduce code redundancy by allowing 'local variable type inference'
```Java
ArrayList<String> listA = new ArrayList<>();
LinkedList<String> listB = new LinkedList<>():
HashSet<String> setA = new HashSet<>();

//With var
var listA = new ArrayList<String>();
var listB = new LinkedList<String>();
var setA = new HashSet<String>();
```
## Summary
- `ArrayList` is better for storing and accessing data -> use for frequent access
- `LinkedList` is better for data manipulation -> inserting/removing elements
- `HashSet` is used for lists that require unique elements
---
## ArrayLists and LinkedLists Continued
### Inserting elements at a specific index
- We can add elements to the list at a desired index using `add(int index, E element`:
```Java
var list1 = new ArrayList<String>(Arrays.asList("Alice", "Bob", "Sam"));
list1.add(2, "Alan");
```
- The above code will add the String "Alan" to the ArrayList at the index 2
- NOTE: This can be slow for larger ArrayLists due to shifting elements
### Checking for existence
- We can check whether a list already contains an element by using `contains(E element)`:
```Java
var list1 = new ArrayList<String>(Arrays.asList("Alice", "Bob", "Sam"));
list1.contains("Bob"); //True
list1.contains("Alan"); //False
```
### Searching for elements
- Similar to the above, we can search for elements (and their index) in a list by using `indexOf`:
```Java
var list1 = new ArrayList<String>(Arrays.asList("Alice", "Bob", "Sam"));
int index = list1.indexOf("Alice"); //0
```
- This is useful in those lists where duplicates are not expected
### Iterating over elements
- We can iterate over elements in a list by using `forEach` SYNTAX:
	- `list.forEach(METHOD_REFERENCE);`
- What are method references:
	- A shorthand syntax used to refer to methods
	- The general syntax: `ClassName::methodName`
	- For example: `System.out::println`
```Java
var list1 = new ArrayList<String>(Arrays.asList("Alice", "Bob", "Sam"));
list1.forEach(System.out::println);
```
---
## Related
- [[Arrays]]
## Covered in
- [[CS1IP_week_07_lecture.pdf]]
- [[CS1IP_week_11_lecture.pdf]]

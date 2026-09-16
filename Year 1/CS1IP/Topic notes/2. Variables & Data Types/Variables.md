#CS1IP 
- A variable is a named container used to store information in the computer memory
	- "A labelled storage box"
```Java
String x;
x = "Hello";
System.out.println(x);
```
* In the above example, x is the variable name, and 'String' is the variable's [[Data Types|data type]]
* We can have an infinite number of variables, but two variables can't share the same name in the same scope
	- Variables, unlike Strings are **mutable**: their value can be changed after assignment by **reassignment**
```Java
String x;
x = "Hello";
System.out.println(x);
x = "Goodbye";
System.out.println(x);
```
* Here, the output would read:
```Java
//Hello
//Goodbye
```
* Once x has been reassigned, when called to print will show the output "Goodbye", unless reassigned once again as [[Sequencing|sequencing]] executes [[Java Statements|statements]] top to bottom
* This means that only the most recent value 'survives', and any older values are discarded from computer memory

> [!note] Mutable vs immutable
> Immutability is a different idea -> The String value itself is immutable, not the variable. `"Hello"` never changes once created — reassigning `x` doesn't edit that string, it just points `x` at a brand new string, `"Goodbye"`, and abandons the old one. This distinction matters more once objects/references come up properly (in CS1OP).

### Declaration, Initialisation, Assignment
* As seen in an example early on the page, there are steps on creating variables:
	1. **Declaration**: Declare the variable name, along with the data type
		```String x;```
	2. **Assignment**: Assign the variable a value
		```x = Hello";```
	3. **Initialisation**: This is not another step but rather a method of combining steps 1 and 2 ->  Initialisation of a variable declares and assigns a value *simultaneously*
		```String x = "Hello";```
``
---
## Related
- [[Java Statements]]
- [[Sequencing]]
- [[Iteration - For & While]]
---
## Covered in
- [[CS1IP_week_01_lecture.pdf]]

- Python is technically written in C (CPython), and was designed to readable/extensible
- It is generable purpose and supports many programming paradigms:
	- **Imperative**: step-by-step simple lines of code
	- **Declarative**: stating desired outcome without outlining each step 
	- **Functional**: Calculates mathematical functions
	- **Procedural**: *has a subroutine?*
	- **Object-Oriented**: Instances of data and methods to modify data (see java)
- Code is processed at runtime with no need to compile, and like Java, is constructed using objects and classes to build complex systems from reusable patterns
- Python is broad and is used in a wide range of fields:
	- Data science
	- Scientific computation
	- Machine learning
	- Neural networks
	- Automation
	- Web development etc.
---
## Syntax
Python is considered to have simple and intuitive syntax compared to other languages.  For example:
```Java
public static Main {
	public class void main(String[] args) {
		System.out.printlnt("Hello world!");
	}
}
```
^ Becomes:
```Python
print("Hello world!")
```
Alternatively:
```Java
if(x < y) {
	z = x;
}
else {
	if(x == y) {
		y = y + 1;
	}
	else {
		z = y;
	}
}
```
^ Becomes:
```Python
if x < y:
	z = x
else:
	if x == y
		y = y + 1
	else:
		z = y
```
## Static vs Dynamic
- Java is a **static** language -> variables cannot change type once declared:
```Java
String name;  //Variable declared and has type String
name = "John"; //Value updated to "John"
name = 36; //Error: variable unable to change data type
```
- Python is a dynamic language -> variables can be changed throughout the program:
```Python
name = "John" # Variable declared and value has been assigned
name = 36 #Variable data type is changed dynamically
```
---
## Related

## Covered in
- [[CS2PP_week_01_lecture.pdf]]
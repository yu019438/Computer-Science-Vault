## Static vs dynamic languages
- Java is a **static** language -> variables cannot change type once declared:
```Java
String name;  //Variable declared and has type String
name = "John"; //Value updated to "John"
name = 36; //Error: type mismatch
```
- Python is a dynamic language -> variables can be changed throughout the program:
```Python
name = "John" # Variable declared and value has been assigned
name = 36 #Variable data type is changed dynamically
```
---
## Syntax comparison
Python is considered to have simple and intuitive syntax compared to other languages.  For example:
```Java
public class Main {
	public static void main(String[] args) {
		System.out.println("Hello world!");
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
	if x == y:
		y = y + 1
	else:
		z = y	
```
---
## Related

## Covered in
- [[CS2PP_week_01_lecture.pdf]]

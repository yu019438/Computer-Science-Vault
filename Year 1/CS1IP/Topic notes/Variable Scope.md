#CS1IP
Variable scope refers to the visibility of a [[Variables|variables]] inside of a Java program.  Scope is primarily determined  by **where** the variable is declared.  
## Global scope
A variable has global visibility when it is:
- Declared at the start of a document
- Accessible within all [[Methods|methods]]
- When using Java classes, these variables use the static keyword
```Java
public class Test1 {
	static int add(int a, int b) {
		return a + b;
	}
	public static void main(String args[]) {
		System.out.println(add(2, 2));
	}
}
```
## Local scope
- Variables declared inside of methods/ code blocks
- Accessible only within that method or block
```Java
public class Test2 {
	static int x = 5; //Global variable
	static void print() {
		int y = 6; //Local variable
		System.out.println(y);
	}
	public static void main(String args[]) {
		print();
	}
}
```
- Local scope also applies to method **parameters** -> Parameters behave as local variables, only accessible within that method
- If a parameter shares its name with a global variable, the parameter takes priority within that method (this is called **shadowing**)
```Java
public class Test3 {
	static int x = 5; //Global variable
	static void print(int x) { //Parameter shares name with global variable
		System.out.println(x); //Prints 6, not 5 - parameter shadows the global x
	}
	public static void main(String args[]) {
		print(6);
	}
}
```
- If the parameter has a **different** name to the global variable, there's no shadowing - the global variable resolves normally when referenced inside the method
```Java
public class Test4 {
	static int x = 5; //Global variable
	static void print(int z) { //Parameter named differently to global variable
		int y = x; //No shadowing - refers to global x
		System.out.println(y); //Prints 5
	}
	public static void main(String args[]) {
		print(6);
	}
}
```
---
## Related
- [[Recursion]]
---
## Covered in
- [[CS1IP_week_04_lecture.pdf]]

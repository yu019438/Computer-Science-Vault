#CS1IP
A method (or function) is a modular code block that is designed to perform a specific task and be reused throughout the program.
- Methods receive input as `parameters` and produce a `return`
- Methods can be thought of as 'subprograms'
- Method syntax:
```Java
static RETURN_TYPE functionName(parameters) {
	//Code block 
	return value;
}
```
- For example:
```Java
static int add(int a, int b) {
	return a + b;
}
```
- The method is then called from `main()` by using its name and passing the required arguments
```Java
public class Test1 {
	public static void main(String args[]) {
		System.out.println(add(5, 8)); //Returns 13
	}
}
```
- In [[Imperative Programming|imperative programming]] the keyword `static` is used, as the class does not need instantiating
- A method with no return statement will use the keyword `void`:
 ```Java
static void print(int x) {
	System.out.println(x); 
}
public static void main(String args[]) { //Main method
	print(5); //The method (print) above is called -> output = 5
}
 ```

## Method overloading
- Method overloading is the way in which multiple methods share the same name but have different parameters.  
- The difference in arguments is how the compiler is able to select the correct method:
```Java
public class Test1 {
	static int add(int a, int b) {
		return a + b;	
	}
	static double add(double a, double b) {
		return a + b;
	}
	public static void main(String args[]) {
		System.out.println(add(2.5, 2));
	}
}
```
- In the above example, both add methods share the same name, but have different parameters.  
- The program is able to select the correct method from the parameters and therefore perform the correct arithmetic (doesn't try to add `double` + `int`)
- **Note**: The methods above must be declared `static` to be called directly from `main()`. If they weren't `static`, this would cause a compilation error, as `main()` itself is`static` and cannot call instance (non-static) methods directly.
---
## Related
- [[Object Orientated Programming]]
- [[Variable Scope]]
---
## Covered in
- [[CS1IP_week_04_lecture.pdf]]

#CS1IP
## `Assert`
The assert keyword is used to test whether a condition behaves as expected.
- **True**: code continues
- **False**: code stops with `AssertionError`
```Java
int x = 5;
assert x > 0;
System.out.println(x) //Only reached if the above assert is valid
```
## Method Testing using `Assert`
Assert can be used to test whether a [[Methods|method]] behaves as expected:
```Java
public class Test1 {
	static int add(int a, int b) {
		return a + b;
	}
	public static void main(String args[]) {
		assert add(0, 0) == 0;
		assert add(1, 1) == 2;
		assert add(2, 3) == 5;
	}
}
```
- In order to use assert it needs to be enabled in your code editor.  This is done by using the `-ea` parameter
- On VSCode you can set the param by `cmd+shift+p` to open actions
- Preferences: `Opens User Settings (JSON)`
- Add line: `"java.debug.settings.vmArgs": "-ea"`
### Testing method specifications
- **Specification**: detailed description of what a method should do -> inputs, output, and behaviour
	- **Preconditions**: What must be true *before* the method is called
	- **Postconditions**: What will be true *after* the method completes execution
- These are documented as comments:
```Java
/**
* Adds two integers and returns the result
* param a -> first int between 0-1
* param b -> second int between 0-1
* Return sum a and b
*/
static int add(int a, int b) {
	...
}
```
### Assert to check pre-conditions
```Java
static double divide(double a, double b) {
	assert b != 0;
	return a * b;
}
public static void main(String args[]) {
	divide(10, 0)
}
```
---
**Thorough testing ensures**:
- Code correctness
- Edge cases and errors identified early on
- Time saved in debugging/maintenance
---
## Related
- [[Recursion]]
## Covered in
- [[CS1IP_week_04_lecture.pdf]]


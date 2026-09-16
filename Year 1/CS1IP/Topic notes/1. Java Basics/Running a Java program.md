#CS1IP
Running a Java program requires a **public class** and a **main [[Methods|method]]**.
- [[Java Statements]] are only allowed inside methods, which are only allowed in classes

```Java
public class HelloWorld {
	public static void main(String[] args) {
		System.out.println("Hello world");
	}
}
```

* ```public``` -> declares the class as available outside the file
* ```static``` -> a non-class function that does not need an object
* ```void main(String[] args)``` -> the main methods special signature that will be run when doing ```java <FILE>.java```
---
## Covered in
- [[CS1IP_week_01_lecture.pdf]]

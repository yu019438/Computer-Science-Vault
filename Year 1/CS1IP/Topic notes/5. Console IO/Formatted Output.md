
#CS1IP
Formatted output uses ```printf()``` to reduce the tediousness of concatenating strings (see [[Operators and Expressions]])
```Java
int weeks = 12;
int days = weeks * 7
System.out.println("In " + weeks + " weeks there are " + days + " days."); 
```
Becomes:
```Java
int weeks = 12;
int days = weeks * 7;
System.out.printf("In %d weeks there are %d days.%n", weeks, days);
```
- ```System.out.printf()``` is the [[Methods|method]] (or function)
- This method has multiple arguments, which are each separated by a ```,``` 
- ```"In %d weeks there are %d days.%n"``` is a **format string**.
	- ```%d``` is a **format specifier** -> substitute the next argument in here, which is specified to be in integer
	- ```%n``` is a **format specifier** -> substitute with a newline here
- The remaining arguments ```weeks``` and ```days``` are turned into strings and substituted into the format string

> [!note] Other format specifiers include:
> - %s for Strings
> - %f for decimal (of floating-point) numbers

---
## Covered in
- [[CS1IP_week_01_lecture.pdf]]

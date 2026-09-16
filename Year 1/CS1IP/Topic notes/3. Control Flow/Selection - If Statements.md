#CS1IP
### If and else
- `if` is a **keyword** (a word with a fixed meaning) with parentheses that surround a condition
- A condition is a boolean expression e.g. `age >= 18`
- {...} follow the condition and contain an if-block (true block) -> This code is only run if the condition is true.  
- If the condition is false, the if-block is skipped and the else-block is run 
```Java 
if (age < 18) {
	...
}
else {
	...
}
```

* Else is technically optional -> if using multiple if [[Java Statements|statements]] that are independent from each other, there is no need for a list of chained statements when more than one may be true:
```Java
if (age >= 12) {
	...
}
if (age >= 18) {}
```
- In the above example, age could be >= 12 and >=18, meaning there is no need for an else statement as both ifs are true.  
### Else-if
- Else-if is used to chain if statements together in an order:
```Java
if (age >= 18) {
	...
}
else if (age >= 15) {
	...
}
else if (age >= 12) {
	...
}
else {
	...
}
```
-> Only one if-block (or the else block) can be true.
### Nested ifs
You can also run if statements within the if-block of another if-statement -> This is **nesting**
```Java
if (age >= 18 {
	if (time >= 21) {
		...
	}
	else {
		...
	}
}
else {
	...
}
```
---
## Covered in
- [[CS1IP_week_02_lecture.pdf]]

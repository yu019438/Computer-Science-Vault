#CS1IP
Loops are used to reduce code repetition and hand repetitive tasks (e.g. searching through data)
### For loops
- A for loop continues to iterate based on the increment and condition for a number of iterations that is fixed before the loop starts:
```Java
for (initialisation; condition; increment) {
	//Statements to execute
}
```
- For example:
```Java
for(int i = 0; i < 5; i++) {
	System.out.println(i);
}
```

> [!important] Increment/decrement
> `n = n + 1` to increment and `n = n - 1` to decrement can be replaced by `n++` and `n--` respectively

---
### While loop
- A while loop iterates as long as the established condition is true.  Hence, the number of iterations are unbounded:
```Java
int i = 0;
while (i < 5) {
	System.out.println(i);
	i++;
}
```
- But, this means that as long as the condition remains false the while loop may never run...
- A do-while loop functions like a while loop but guarantees at least one iteration:
```Java
do {
	//Statements
} while (condition);
```
- The statement is executed before the while loop is declared -> hence at least one iteration is run
## Tracing 
- Tracing means manually checking through code line-by-line and recording [[Variables in Java|variables]] values at a fixed point in each iteration in order to predict output/ spot bugs
- Always trace at the same fixed point each iteration (e.g. "just after `i++`") to avoid confusing before/after values.
**While loop example**: trace just after `x--`: 
```Java 
int x = 3;
while (x > 0) {
	x--; 
}
``` 

| Iteration | `x` |
| --------- | --- |
| 1         | `2` |
| 2         | `1` |
| 3         | `0` |

---
**For loop example**: Trace just after `println`: 
```Java
for (int i = 0; i < 5; i++) {
	System.out.println(i); 
}
``` 

| Iteration | `i` |
| --------- | --- |
| 1         | `0` |
| 2         | `1` |
| 3         | `2` |
| 4         | `3` |
| 5         | `4` |

---

> [!attention] Off-by-one bugs
> Tracing exposes bugs where the loop runs one iteration too many/few. E.g. this "integer square root" loop outputs `4` instead of the expected `3`, because the condition is checked *after* `sqrt` is already incremented one step too far:
> ```Java
> int sqrt = 0;
> while (sqrt * sqrt < 10) {
> 	sqrt++;
> }
> ```
## Nested For Loops
- You can nest for loops within other for loops:
```Java
for(int i = 0; i < MAX_I; i++) {
	for(int j = 0; j < MAX_J; j++) {
	//Statements to execute
	}
}
```
- For example: 
```Java
for (int i = 1; i < 3; i++) {
	for (int j = 1; j < 3; j++) {
		System.out.println("i = " + i);
		System.out.println("j = " + j);
	}
}
```

| Iteration | `i` | `j` |
| --------- | --- | --- |
| 1         | `1` | `1` |
| 2         | `1` | `2` |
| 3         | `2` | `1` |
| 4         | `2` | `2` |
### `Break` statement
- The `break` statement is useful for exiting a loop early:
```Java
for (int i = 0; i < 10; i++) {
	if (i == 5) {
		break; //Exit loop when i is 5
	}
	System.out.println(i);
}
```

> [!attention] Break nested loops
> `break` inside a nested loop only exits the **inner** loop. The outer loop keeps running. Uses an [[Selection - If Statements|if statement]] to detect when to break:
> 
> ```Java
> for (int i = 1; i <= 3; i++) {
> 	for (int j = 1; j <= 2; j++) {
> 		if (i == 2 && j == 2) { 
> 			break;
> 		} 
> 	System.out.print("i=" + i); 
> 	System.out.println(",j=" + j); 
> 	} 
> }
> ```
> 

Output of the above:

| Iteration | i   | j   |
| --------- | --- | --- |
| 1         | 1   | 1   |
| 2         | 1   | 2   |
| 3         | 2   | 1   |
| 4         | 3   | 1   |
| 5         | 3   | 2   |

---
## Covered in
- [[CS1IP_week_03_lecture.pdf]]

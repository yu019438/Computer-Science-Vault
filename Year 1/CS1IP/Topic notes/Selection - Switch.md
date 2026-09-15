#CS1IP
`Switch` statements are used as a way to avoid drawn-out, complex sequences of [[Selection - If Statements|if statements]]:
```Java
switch(option) { //The switch chooses what to do based on variable
	case 'a':
		System.out.println("x");
		break;
	case 'b':
		System.out.println("Y");
		break;
	case 'c':
		System.out.println("z");
		break;
	default: //if no cases match, execution continues here (else)
		System.out.println("incorrect input");
		break;
}
```

- `break` completely exits the switch block once a case has run
- Without it, execution will not stop and execution will continue through all cases
- However, you can intentionally omit `break`:
```Java
switch(option) {
	case 'a': case 'b': case 'c':
		System.out.println("x, y, z");
		break;
	default:
		System.out.println("incorrect input");
		break;
}
``` 
Here, `case 'a'`, `'b'`, and `'c'` are deliberately stacked with no `break` between them, so that all three share the same output -> The shared output is a result of this technique, not the reason for it.
### Case switch pitfalls
It is easy to forget `break` and can cause issues:
```Java
switch(option) {
	case 'a': System.out.println("x"); //Accidentally forgot break
	case 'b': System.out.println("y");
	case 'c': System.out.println("z");
}
```
Here, as break was not used no matter the case, all 3 outputs (x,y,z) will get printed, which is undesirable as all outputs are different (unlike the previous example).

---

> [!danger] Limitations
> `switch` cases must be constants: fixed or known values like `'a'` or `18`. Unlike [[Selection - If Statements|if statements]], you **can't** use expressions or conditions as a case (e.g. `case age > 18:` is not valid) -> Condition evaluate to a [[Boolean & Chars |boolean]], and `switch` only matches literal values, **not booleans**.
> 
> This is a key reason `switch` is rarely preferable to `if` in practice  -> `if` can test any boolean condition, while `switch` can only match a value exactly.

---
## Covered in
- [[CS1IP_week_02_lecture.pdf]]

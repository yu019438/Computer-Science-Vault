#CS1IP
### Relational operators
- `x < 12` -> less than: x = 11, 10, 9...
- `x > 12 `-> greater than: x = 13, 14, 15...
- `x <= 12` -> less than or equal to: x = 12, 11, 10...
- `x >= 12` -> greater than or equal to: 12, 13, 14...
- `x == 12` -> 12
- `x != 12` -> 10, 11, 13, 14...

> [!tip] = vs ==
> = is used for assignment (e.g. `x = 12`) while == is used for equality (e.g. if(`x == 12`) {...}

Each of these produces a boolean, which is what an `if` condition in [[Selection - If Statements]] actually checks

---
### Boolean operators
The logical operators take two booleans as input and produce one boolean as output:
- `(x < 10) && (x > 5)` -> condition A **and** condition B
- `(x > 10) || (x < 5)` -> condition A **or** condition B
Without `&&`/`||`, an if statement (see [[Selection - If Statements]]) could only test one thing at a time
```Java
boolean morning = (time >= 6) && (time < 12);
boolean afternoon = (time >= 12) && (time < 18);

boolean daytime = morning || afternoon;
boolean nighttime = !daytime;
```
- Booleans are values -> you can assign them to variables and perform calculations with them using (logic) operators 
- `!` is a logic operator used to negate a boolean in the example above (like a - sign)

> [!warning] ! vs !=
 >These look similar but are **not** related:
> - `!` (unary) takes **one** boolean and flips it: `!daytime` → true becomes false, false becomes true
> - `!=` (binary) takes **two** values and compares them: `age != 18` → true if age is *not* 18
>  -  `!=` is the opposite of `==` (comparison), not a version of `!` (negation).

---
### Char data type
- A Char is a [[Data Types|data type]] that holds a single character
- **NOTE**: Character values are enclosed in single quotes `'` rather than double quotes `"`
```Java
char vowel1 = 'a';
char vowel2 = 'e';
char vowel3 = "i"; //Compiler Error -> double quotes
```
### Char input
Scanner has no `nextChar()`[[Methods]], so we read the input as a whole line (`String`) using `nextLine()` -> see [[Formatted Input]] ->  then identify the character we want with the`charAt(x)` method.
```Java
Scanner input = new Scanner(System.in);
System.out.println("Are you a student? (y/n)");
char isStudent = input.nextLine().charAt(0);
```

---
## Covered in 
- [[CS1IP_week_02_lecture.pdf]]

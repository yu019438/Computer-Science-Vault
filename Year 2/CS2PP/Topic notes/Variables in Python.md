#CS2PP
- All values in python are objects -> variables names point to the object
- In Python there is no variable declaration ->  `x = 6` creates an int object (with the value 6) and binds it to the name x in a single step with assignment operator `=`
- You can also have multiple and chained assignments:
	- Multiple assignments: `a, b = 100, 200` -> assigns object values to variable names respectively
	- Chained assignments: `c = d = 5` -> creates one object and binds both names to it
- Python doesn't require the data type to be specified -> in the above example, the data type `int` is not required
	- Taking this one step further, variables can change type at any time 
	```Python
	number = 100
	type(number) #int
	
	number = -1.5
	type(number) #float
	```
	- The `type()` function can be used to inspect the data type of a variable
---
## Functions vs Methods
- **Function**: standalone, called directly: `type(x)`
- **Method**: belongs to an object/class, called with dot notation, takes the object as an implicit first argument: `x.bit_length()`, `"rex".upper()`
- Java has _only_ methods (everything lives inside a class), whereas Python has both
---
## Variable Names
Accurate/consistent variable names in programming are essential to maintain readable code that is intuitive for yourself and other programmers.  This is done by following a set of naming rules:
- A variable name must start with either a letter or `_`
	- Cannot start with a number
- Cannot contain special characters or spaces
- Variable names are case sensitive 
- Python uses `snake_case` to separate words in a variable name, unlike Java which uses `camelCase`
- Finally, variable names cannot mimic keywords such as `class`, `for`, `if` etc.
---
## Displaying Variables
- `print(a, b) `-> comma separated args are auto-converted to strings and joined with a space
- `print(a + b)` -> concatenates strings directly (no space added) but renders an error if combining strings with other data such as `int`/`float`
- `.format()` -> uses `{}` as placeholders and `.format()`to fill them:
```Python
name = "Ro"
age = "19"
print("My name is {} and I am {} years old".format(name, age))
```
- `f-strings` (update version of the method above) in which variables are labelled directly inside the placeholder, eliminating the need for `.format()` at the end:
```Python
first = "Ro"
last = "Fairs-Billam"
print(f'My name is {first} {last}") 
#My name is Ro Fairs-Billam
```
- f-strings are the preferable option as they are the most straight forward, without having to worry about `.format()` or `+` vs `,`
---
## Related

## Covered in
- [[CS2PP_week_01_lecture.pdf]]
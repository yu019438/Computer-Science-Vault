#CS2PP 
## Indentation
- Like Java, Python uses indentation to define code blocks, allowing code to be more easily readable and interpreted by other programmers:
```Python
if x < y:
z = x
else: 
if x == y:
y = y + 1
else:
z = y
```
- When utilising indentation becomes:
```Python
if x < y:
	z = x
else: 
	if x == y:
		y = y + 1
	else:
		z = y
```
- Block indentation is typically 4 spaces, or in any IDE/code editor `tab`
## Comments
- Comments are used in code to inform other programmers of why a code block method exists, and why it looks the way it does
- **NOTE**: Comments are not used to reiterate exactly what a code block/method will output, as this should be obvious when reading the code
### Types of comments
- **In-line comments** (#...): These are used to drop a small note into a program, such as a heading/reminder or brief explanation
- **Docstrings** ("""..."""): While technically string literals rather than comments, these are used immediately following module, class, or function definitions to create accessible, multi-line documentation.
	- Unlike in-line comments which are entirely ignored at execution, Python actually stores docstring comments in the memory as an official attribute called `__doc__` attached to that function or class.
	- This allows docstrings to be accessed while running a program through the use of the `help()` method
---
## Related
## Covered in
- [[CS2PP_week_01_lecture.pdf]]

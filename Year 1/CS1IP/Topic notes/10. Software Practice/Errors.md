#CS1IP
### Compile-time errors
These are errors made in the program that are spotted immediately that prevent a program from running:
- **Syntax errors** -> forgetting to end [[Java Statements|statements]] with ```;```
- **Undeclared variables** -> `String x;` without following up with `x = "..."` (see [[Variables in Java]])
- **Missing references** -> using a particular function without importing the package
### Run-time errors
These errors aren't computed straight away but occur when a program is run:
- **Maths error** -> Attempting to divide by zero during calculations
- **Out-of-bounds access** -> Trying to access the 10th item in an array of 5
- **Missing files** -> Trying to access files that do not exist
- **Memory** -> Running out of system memory
### Semantic errors
These errors are the hardest to fix and occur when the grammar/syntax of a program are correct, meaning it runs from start to finish, but the core logic or meaning is fundamentally incorrect:
- **Sign errors** -> adding variables when subtraction is required
- **Adding strings instead of integers** -> `"5" + "5" = "55"`, not 10 etc. (concatenation behaviour from [[Operators and Expressions]] that's normally useful becomes a serious bug here...)
---
## Covered in
- [[CS1IP_week_01_lecture.pdf]]

#CS1IP
* Operators are typically used for calculation/computation.  However, we can also use them in conjunction with variables and constants to build **expressions**
* The combination of Strings and integers (as well as other [[Data Types|data types]])  is called concatenation: 
```Java
int weeks = 12;
int days = weeks * 7
System.out.println("In " + weeks + " weeks there are " + days + " days.");
```
- In order to create a String, Java concatenated text (String) and numbers (int) to create a longer string
- The above example can be seen using [[Formatted Output|formatted output]], offering a cleaner alternative
---
### Precedence
-> The **B.I.D.M.A.S**. order of operations applies to all mathematical computation in Java
### Division
- Integer division rounds towards 0
- The modulus operator (%) can be used to divide and produce the remainder from the division
### Updating a variable
```Java
int x = 1;
x = x + 1;
```
- Looks like algebraic nonsense (`x` can't equal `x + 1`), but it isn't an equation, it's an **instruction**
- Java evaluates the right-hand side first (`x + 1`), then assigns that result back to `x`
- Relies on [[Sequencing]] -> the old value of `x` is read before it gets overwritten
---
## Covered in 
- [[CS1IP_week_01_lecture.pdf]]

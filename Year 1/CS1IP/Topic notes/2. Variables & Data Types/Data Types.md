#CS1IP
Programming languages use data types to tell the computer how to store, manipulate and interpret data -> Every [[Variables|variable]] must have one.
- `String`: A text value, or sequence of characters
- `Int` (integer): A whole number
- `Double`: A decimal number (floating point)
- `Boolean`: True/False
- `Char`: A single character

> [!warning] Floating point pitfalls
> - `int / int` always does **integer division first**, even when assigned to a `double`:
>   ```Java
>   double x = 1/10;   // = 0.0, NOT 0.1 -> integer division happens before the result is converted
>   double y = 1.0/10.0;   // = 0.1 -> correct, because both operands are already doubles
>   ```
> - Every floating-point calculation is **rounded**, so repeated arithmetic can drift off the "expected" exact value:
>   ```Java
>   double t = 1.0/10.0;
>   double one = t+t+t+t+t+t+t+t+t+t;   // "should" be 1.0, often isn't exactly
>   ```


---
## Covered in
- [[CS1IP_week_01_lecture.pdf]]

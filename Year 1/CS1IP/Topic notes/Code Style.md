#CS1IP
### Whitespace
Java ignores whitespace and line breaks entirely. Code will run identically whether squished onto one line or spread across many. But just because you *can* format code however you want doesn't mean you should.
### Indentation
- Indent the contents of any `{}` block, typically by 4 spaces
- Nested blocks get multiple levels of indentation (8, 12 spaces, etc.)
- Closing braces `}` go on their own line, one level back from the block's contents
- Spaces vs. tabs is a personal choice, but **never mix both within the same project** -> tab is standard across JetBrains/VScode
- Modern convention favours 4 spaces per level rather than a historical 8-space tab due to space of deeply nested blocks
### Comments
- `//` starts a single-line comment, running to the end of the line
- `/* ... */` spans multiple lines — often used to temporarily disable a block of code
- Comments are for programmers and will be ignored when executed

> [!warning] Bad commenting patterns
>
> - **Re-describing what code already makes clear**: `// if age is less than 18, do this` above `if (age < 18){...}`)
> - **No comments at all**: Leave no explanation of *why* the code does what it does
 > - **Commented-out code left in**: Using `//` to temporarily disable a line while debugging is fine, but forgetting to remove it afterward leaves confusing clutter

Good comments explain *why* the code is there, not what it already does, giving it context. 

---
## Covered in
- [[CS1IP_week_02_lecture.pdf]]

#CS2PP 
## Implementation
Python is a language specification -> syntax/semantics/standard library, meaning it does not determine machine-level implementation (how it is interpreted by the machine directly) -> there are multiple implementations:
- **CPython**: This is the reference implementation (standard python form) and is a compiled C program
- **PyPy**: Uses JIT (just-in-time) compilation for speed
- **Jython**: Runs on the Java Virtual Machine
- **IronPython**: Runs on .NET
- **MicroPython**: Designed for microcontrollers/embedded devices
## Execution
1.  When python runs a `.py` file it is parsed into an Abstract Syntax Tree (AST) and checked for syntax -> if failed at this stage would produce a `SyntaxError`
2. Then, it's compiled into a bytecode instruction set and a cached version is saved:
	- Bytecode is a lower level, simplified set of instruction that a machine understands quickly (not binary, which is 1's and 0's -> this is an intermediate translation)
	-  Bytecode is 'platform agnostic', meaning execution is not affected by the platform on which it runs (e.g. MacOS, Windows, Linux) -> but **is** specific to the CPython **version/optimisation level**
	- Caching *speeds up execution* when code is run more than once -> avoids re-compiling the same code each time -> Only imported modules are cached as they are reused often.  The `__main__` code is compiled in the memory **each time**
3. **Python Virtual Machine (PVM)** is the interpreter that runs code by looping through the bytecode version of each python instruction, one by one
4. For each instruction, the PVM doesn't actually compute the result, it just matches the bytecode with a corresponding pre-compiled C function that actually uses binary to complete the instruction -> Genuine machine code that translates to output from the CPU 

> [!warning] Compiling vs Running -> don't conflate these
> - In languages like C/Java, compiling and running are two separate, visible steps (compile to an executable first, run it separately/later)
> - In Python, this distinction is invisible -> writing and running code feel like one action, because the parse -> AST -> bytecode step happens automatically and immediately, hidden inside a single `python myscript.py` command
- Because of this invisibility, you can execute strings of Python code from within a program
- The following isn't a `.py` file, yet `exec()` runs it through the same pipeline:
```Python
code_as_a_string = "print(2+2)"
exec(code_as_a_string)
```
---
## Related

## Covered in
- [[CS2PP_week_01_lecture.pdf]]

#CS1IP
Recursion is when a [[Methods|method]] calls on **itself** to solve a problem.  This involves a:
- **Base case**: This is the simplest case that stops recursion *(no recursion occurs)*
- **Recursive case**: This is when the method calls itself
Recursion should be used with caution, as excessive use can cause computer memory related issues. This is because each call that hasn't finished yet is kept on the **call stack**, waiting for the call below it to return. 
-> If there's no base case (or `n` never actually reaches it), the stack keeps growing until it runs out of memory causing a `StackOverflowError`
## Factorial example
```Java
static int factorial(int n) {
	if (n == 0) {
		return 1; //Base case
	}
	return n * factorial(n - 1); //Recursive case
}
```
- **Base case**: return `1` when `n == 0`
- **Recursive case**: return `n * factorial(n - 1)`
**Trace of**`factorial(5)`: Calls go down until the base case is hit, then values return back up:
```Java
factorial(5) = 5 * factorial(4)
factorial(4) = 4 * factorial(3)
factorial(3) = 3 * factorial(2)
factorial(2) = 2 * factorial(1)
factorial(1) = 1 * factorial(0)
factorial(0) = 1 //Base case

// unwinding:
factorial(1) = 1 * 1  = 1
factorial(2) = 2 * 1  = 2
factorial(3) = 3 * 2  = 6
factorial(4) = 4 * 6  = 24
factorial(5) = 5 * 24 = 120

```
^ This is a linear recursion, each call makes a further, recursive call
## Fibonacci example
```Java
static int fibonacci(int n) {
	if (n == 0) return 0;      //Base case
	if (n == 1) return 1;      //Base case
	return fibonacci(n - 1) + fibonacci(n - 2); //Recursive case
}
```
- **Base case**: return `0` when `n == 0 `or `1` if `n == 1`
- **Recursive case**: return `fib(n - 1)` + `fib(n - 2)`
**Trace of** `fibonacci(4)`: unlike factorial, each call branches into _two_ further calls, forming a recursion tree rather than a single chain:
```Java
fibonacci(4)
├── fibonacci(3)
│   ├── fibonacci(2)
│   │   ├── fibonacci(1) = 1 //Base case
│   │   └── fibonacci(0) = 0 //Base case
│   │   → fibonacci(2) = 1 + 0 = 1
│   └── fibonacci(1) = 1 //Base case
│   → fibonacci(3) = 1 + 1 = 2
└── fibonacci(2)
    ├── fibonacci(1) = 1 //Base case
    └── fibonacci(0) = 0 //Base case
    → fibonacci(2) = 1 + 0 = 1
→ fibonacci(4) = 2 + 1 = 3
```
^ Because each call spawns two more, the number of calls grows very quickly as `n` increases. This is why recursive Fibonacci can be a common example of **inefficient** recursion.
## Common mistakes
- **Missing base case**: `sum(n) { return n + sum(n - 1); }` with no stopping condition never terminates and eventually crashes with `StackOverflowError`.
- **Base case never reached**: The recursive case must move `n` *towards* the base case (e.g. `n - 1`, not `n + 1` or unchanged), or recursion never stops.

---
## Covered in
- [[CS1IP_week_04_lecture.pdf]]

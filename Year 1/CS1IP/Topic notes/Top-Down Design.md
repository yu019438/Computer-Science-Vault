#CS1IP
- Top-down design defines a problem solving approach, in which more complex problems into smaller, more manageable parts
- Why is this imporant?
	- Code is **modular** -> maintainable and reusable
	- Clear **structure** and separation -> clear road map for code implementation
	- Easier debugging
	- **Scalable** -> adapts well to larger, complex projects
## How to Implement Top-down Design
1. Define the high-level (complex) task
2. Break this down into smaller 'sub-tasks'
3. Solve/refine each sub-problem individually
---
- ### TODO Comments:
	- Using TODO comments to separate a task and put clear instructions inside of a program/code block
	- Using the TODO comment allows the problem to be broken down into subtasks with the reminder to fill in code at a later time -> focus can be on **structure** rather than programming
- ### Java [[Methods|methods]]
	- Reusable code blocks allow problems to be broken down into different methods
	- This means that code can be broken down into subtasks more easily, as the process can be thought about from a *logical* point of view before worrying about code syntax
For example:
```Java
void drawBox(int n) {
	//TODO draw top row
	//TODO draw middle columns n times
	//TODO draw bottom row 
}
```

```Java
void drawBox(int n) {
	drawTopRow();
	drawMiddleColumns();
	drawBottomRow();
}
drawBox(5)
```
^ The problem is broken down into key steps so the programmer may think about the logic of the code, rather than worrying about code syntax
## Common Pitfalls
- Making methods TOO granular -> not everything needs its own method/object
- The opposite of the above, having poor abstraction -> key logic/idea not easily visible
- Jumping straight into coding -> Design first, programming second
- Assuming that once a method is complete it can be left alone -> constant review/refactoring is key to ensure there are no bugs/errors in execution
---
## Further Examples
Review lecture notes for Dungeon Game example and application of top-down design: 
- Breaks down the dungeon game into:
	- Player Data
	- Main Game loop
		- Door mechanism
		- Monster encounter/Treasure collection
-> Shows detailed code example of logic from this lecture
---
## Related
- [[Code Style]]
- [[Testing]]
- [[Recursion]]
## Covered in
- [[CS1IP_week_08_lecture.pdf]]


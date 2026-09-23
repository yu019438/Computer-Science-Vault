#CS2PP
## Title
- Modular programming is done in python with methods.  Like in Java, methods are used to break down larger coding tasks into more manageable, reusable subtasks.  
- Here is key terminology to be aware of:
	- **Variable**: Named storage location on the computer memory
	- **Method** (function): Repeatable blocks of code, with inputs/outputs designed to perform a specific subtask
	- **Class**: Defined encapsulation of data, variables and methods, in which objects are created
	- **Module**: Related code saved in a `.py` file -> installable
	- **Package**: A directory containing modules (and possibly subpackages) -> installable, may include an `__init__.py` for setup on import
	- **Library**: Often used interchangeably with "Package" is an umbrella term for a reusable blocks of code, which could be a whole package, several packages, or even a single module
	- **Framework**: Structure/architecture that combines the above components to assemble a program
	- **Environment**: All code elements visible in the python instance (IDE), including system resources
- Below is an example image of the component hierarchy:
![[Pasted image 20260922153642.png]]
## Connecting Components
- In the environment we can install new libraries and packages using the `Anaconda Navigator `
- We can also `import` working code into the current component by checking for modules using the following locations:
	- Local working directory: Allows Python to import any code within the same directory as where you are currently running your script
	- `$PYTHONPATH`: An environment variable you can set on your computer to tell Python extra directories it should search for modules
	- `sys.path`: A built in list inside of python that contains all file paths python checks whenever import is executed
---
## Related

## Covered in
- [[CS2PP_week_01_lecture.pdf]]

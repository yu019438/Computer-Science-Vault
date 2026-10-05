#CS2PP
## Overview

| Type Category | Type Representation          |
| ------------- | ---------------------------- |
| Text          | str                          |
| Numbers       | int, float, complex          |
| Sequence      | list, tuple, range           |
| Mapping       | dict                         |
| Sets          | set, frozenset               |
| Boolean       | bool                         |
| Binary        | bytes, bytearray, memoryview |
| None          | NoneType                     |
## Detail
- **Text**: 
	- Type: `str`
	- Example: `first_name = "Ro"`
- **Numbers**: 
	- Type: 
		- `int` -> whole number, positive/negative, can be any size
		- `float` -> decimal (can include scientific notation such as $e$ or $E$ for powers of 10); capped at 64-bit size
		- `complex` -> a number with a real and imaginary part
	- Example: 
		- `int` -> $x = 12$
		- `float` -> $y= 1.5$
		- `complex` -> $3 + 2.1j$
- **Sequence**: 
	- Type:
		- `list` -> ordered, mutable collection (dynamic array)
		- `tuple` -> immutable collection of elements
		- `range` -> integers between numbers (start included, end excluded)
	- Example
		- `list` -> `a =[2, 3, 2, 3, 3]`
		- `tuple` -> `t = (1, 2, 3)`
		- `range` -> `r = range(6)` (output: 0, 1, 2, 3, 4, 5)
- **Mapping**: 
	- Type: `dict` -> Dictionary of mapped key-value pairs 
	- Example: `d = {1: "Hello", 2: "world"}`
- **Sets**: 
	- Type:
		- `set` -> unordered collection of unique elements
		- `frozenset` -> unchangeable set
	- Example: 
		- `set` ->  `s = {"A", "B", "C"}`
		- `frozenset` -> `f = frozenset({"A", "B", "C"})`
- **Boolean**: 
	- Type: `bool` 
	- Example: `yes = True`
- **Binary**: 
	- Type: 
		- `bytes` -> immutable sequence of bytes
		- `bytearray` -> mutable array of bytes
		- `memoryview` -> read memory of another binary object without duplicating
	- Example: 
		- `bytes` -> `b = bytes(7)` (creates 7 individual bytes)
		- `bytearray` -> `ba = bytearray(7)` (creates array of 7 bytes)
		- `memoryview` -> `m = memoryview(bytes(5))` (view contents of 5 bytes)
- **None**:
	- Type: `None` -> no information 
	- Example: `n = None` -> `n` holds `None`, meaning it has no value
---
## Related

## Covered in 
- [[CS2PP_week_02_lecture.pdf]]

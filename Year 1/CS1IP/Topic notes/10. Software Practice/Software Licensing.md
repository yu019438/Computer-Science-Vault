#CS1IP
- Software licensing is the legal term that defines which software can be used, how it can be used or modified, and/or distributed in order to protect the user and creator's rights
- This matters as it enables the reusability of existing, open-source software, as well as the collaboration involved with open-source. It also ensures legal guidelines are followed, and creates a standard of software that is produced
- Types of software licensing:
	- **Proprietary licenses**:
		- Software owned by an entity
		- Cannot be modified/redistributed
		- e.g. Windows, Adobe PhotoShop, Skype...
	- **Open-source licenses**:
		- Source code is publicly available
		- e.g. Linux, Apache, MySQL...
## Types of Open-Source Licenses 
There many different open-source licenses but they can all be categorised into:
- **Copyleft licenses**:
	- General Public Licenses (GPL):
		- Completely free to use/modify/distribute
		- Any derivative work must also be open-source
		- Any modifications must be GPL compliant
	- Lesser General Public Licenses (LGPL):
		- Allows linking to proprietary code under certain condition
- **Permissive licenses**:
	- MIT licenses:
		- Completely free to use, modify, distribute
		- Can be used in proprietary software
		- Must include original license/copyright notice
	- Apache Licenses (2.0):
		- Similar to MIT -> adds a patent grant
		- Must include copy of license
## How to Choose a License
- Do you want others to contribute to the project -> **Open-source**
- Is the software owned by an entity/company -> **Proprietary** 
- Do you want all derivates to also be open source -> **Copyleft vs Permissive**
## How to Apply a License
- When creating a piece of software, include a `LICENSE` or `COPYING` file to the root of the project
- Include a comment at the top of each source file indicating the license:
**-> View lecture notes for an example of an MIT License**
## Best Practice
- Always include a license in your projects so that nothing may be stolen/claimed by someone else
- Understand the licenses in the libraries you use
- Choose the correct license
- AVOID: 
	- Ignoring license requirements -> *comply with license terms*
	- Mixing incompatible licenses -> *When combining code from different sources, be aware of conflicts in license terms*
---
## Related
- [[Git & Version Control]]
- [[Code Style]]
- [[Software Security]]
## Covered in
- [[CS1IP_week_12_lecture.pdf]]


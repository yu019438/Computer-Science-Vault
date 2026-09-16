#CS1IP
IO stands for Input/Output -> When a program is executed is reads files, and then writes to them.  This allows for **Data Persistence** (retaining data long-term even after the program stops running). The main way in which files/directories are represented is by using `path` objects (replacing the old `file` object)
- **File**: a container that stores data: text, code, an image, a program's binary, etc. It's the basic unit of storage; when you open it, you get its contents.
- **Directory** (folder): a container that organises other files and directories. It doesn't hold data itself (beyond metadata); it holds references to its contents.
## `Path` objects
- Path specifies the location of a file/directory in the storage. 
- **Path Capabilities**:
	- Check if a file/directory exists
	- Create/delete files and directories
	- List files in a directory
	- Access file attributes -> size, last modified, date created etc.
- **Absolute path**:
	- This starts from the 'root directory'
	- Contains the full directory path to the file/folder from the home directory
	- For example: 
		- `/home/User/documents/file.txt` 
		- `C:\User\Documents\file/txt`
- **Relative path**:
	- This path is relative to another directory (often an applications starting directory)
	- For example: `documents/file.txt`

>[!Warning]
>Absolute paths provide a fixed location -> Relative paths are flexible and adapt based on the base directory (application/folder)
## Creating a `path`
Creating a path object uses the Path.of() method:
```Java
Path path = Path.of("example.txt");
System.out.println("File name: " + path.getFileName());
System.out.println("Parent directory: " + path.getParent());
System.out.println("Absolute path: " + path.toAbsolutePath());

//example.txt
//null
//C:/path/to/example.txt
```
^ Other Path [[Methods|methods]]:
- `Path.of()`: Creates a path object that represents a file/directory location without touching the file system
- `getFileName()`: Returns the file name
- `getParent()`: Returns the parent directory *(e.g. folder containing the file)*
- `toAbsolutePath()`:Converts to the absolute directory *(e.g. the home folder)*
## `Files` class
The `path` objects above are usually used as parameters for the `Files` class
- Enables reading/writing/manipulating files and directories
- Provides methods for performing file and directory operations
- Designed to work with `Path` objects
Files and directory management can be done with the following methods:
- `Files.exists()`: Checks if file/directory exists in the path *(returns boolean)*
- `Files.size()`: Returns number of bytes equal to the file size
- `Files.createFile()`: Create file at the specified path (creates new .txt file in the current directory)
- `Files.createDirectory()`: Create directory at the specified path (creates new folder in the current directory)
- `Files.delete()`: Deletes a file at the current directory
	- You must ensure that all files are deleted before running otherwise received a `DirectoryNotEmptyException`
- `Files.list()`: Displayed each file/directory entry within the current directory -> Returns a `Stream<Path>` object that must be closed: `stream.close()`
## Directories
Different operating systems use different ways to represent paths:
- Windows: `C:\Users\Documents\file.txt`
- MacOS (and UNIX/linux): `/home/user/files.txt`
### Cross-platform file paths
The issue with Windows and Mac/Linux using different methods of path representation is that hardcoding path separators (`\` or `/`) causes the code to break when running between different operating systems. 
- The solution to this is using `Paths.get()` method to get directories individually and then recreate the full path by adding the separate directories back together
- `Path path1 = Paths.get("C:", "Users", "Downloads", "file.txt");
### URI
It is also possible to locate files by using URI (Uniform Resource Identifier) -> `file://`
```Java
Path path1 = Paths.get(new URI("file:///C:/Users/file.txt"));
```
This allows the program to treat both types of addresses the same.

---
## Related
- [[Formatted Input]]
- [[Formatted Output]]
- [[Reading & Writing Files]]
## Covered in
- [[CS1IP_week_07_lecture.pdf]]

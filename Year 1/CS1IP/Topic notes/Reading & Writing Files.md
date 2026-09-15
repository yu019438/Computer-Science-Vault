#CS1IP
- In Java, files are viewed as a series of bytes
- Different operating systems have different ways to determine the end of a file, but the most common marker is 'EOF'
- When processing files, Java uses the Stream concept -> This handles data sequentially;
	- InputStream: Reads data from the source(s)
	- OutputStream: Writes data to destinations
- Therefore, the Java program reads the `InputStream` and writes the `OutputStream`
- Common examples of InputStream and OutputStream usage are: 
	- Scanner(system.in)
	- System.out.println()
---
## Process of read/write
There are 2 main ways of reading/writing files in Java:
- Sequential IO (e.g. `FileWriter`, `Scanner`, `Formatter`)
- Buffered IO (e.g. `BufferedWriter`, `BufferedReader`)
### Sequential IO
- Sequential files store records in a specific order
- This is useful for applications that store ordered/persistent data
- Common sequential operations:
	- Creating/writing records
	- Reading/retrieving records
	- Replacing records
- The main ways to write sequential text files are by using `FileWriter` or `Formatter`
	- Their main methods are `write()` and `format` to write, and `close()` to finish writing/release the file
- `FileWriter` is used to write text data to files, and has no built-in formatting    -> this must be manually applied to attain a structured output:
```Java
FileWriter writer = new FileWriter("client.txt");
writer.write("100 Bob Blue 24.98\n");
writer.write("200 Steve Green -345.67\n");
writer.close();
```
- `Formatter` writes text to files (like `FileWriter`) but applies a format -> allows more precision/control over the output:
```Java
Formatter output = new Formatter("clients.txt");
int account number = 100;
String firstName = "Bob";
String lastName = "Blue";
double accountBalance = 24.98;
output.format("%d %s %s %.2f%n", accountNumber, firstName, lastName, balance);

int account number = 200;
String firstName = "Steve";
String lastName = "Green";
double accountBalance = -345.67;
output.format("%d %s %s %.2f%n", accountNumber, firstName, lastName, balance);
```
When writing a sequential file, use Scanner to read text data from the file -> it reads line-by-line and parses each field according to expected data types: 
- `hasNext()` checks for the EOF
- `nextLine()` is used to get the entire next line
```Java
Scanner file = bew Scanner(Path.of("input.txt"));
while (file.hasNext()) {
	String line = file.nextLine();
	System.out.println(line);
}
```

>[!Attention]
>- Both FileWriter and Formatter require the close() method to complete
>- If the file already exists, FileWriter or Formatter replace all previous content -> This involves reading the existing data, modifying the necessary parts, then writing the updated version to a new file
### Buffered IO
- Buffered IO provides a performance boost as the number of I/O operations are significantly reduced
- Buffered IO uses what's called a 'Buffered Stream' -> instead of accessing the SSD drive directly when data is read/written, data is stored **temporarily** in the memory
- This reduces the time spent accessing the drive/file system
- `BufferedWriter`:
	- Its main function is to `write()`
```Java
var path = Path.of("example.txt");

var writer = Files.newBufferedWriter(path);
writer.write("Hello World!\n");
writer.write("Welcome to Java File I/O with buffering");

writer.close();
```
- `BufferedReader`:
	- Its main function is to `readLine()`
```Java
var path = Path.of("example.txt");
var reader = Files.newBufferedReader(path);

var line = reader.readLine();
while(line != null) {
	System.out.println(line);
	line = reader.readLine();
}
```

---
## Related
- [[File IO]]
- [[Formatted Input]]
- [[Formatted Output]]
## Covered in
- [[CS1IP_week_07_lecture.pdf]]

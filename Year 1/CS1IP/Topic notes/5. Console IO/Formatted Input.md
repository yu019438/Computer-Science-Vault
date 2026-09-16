#CS1IP
Formatted input is when a program is told exactly how to interpret the input data, by assigning a [[Data Types|data type]] to the user's input.
```java
Scanner input = new Scanner(System.in);
System.out.println("How many weeks until the end of the semester?");
int weeks = input.nextInt();
int days = weeks * 7;
System.out.println("In " + weeks + " weeks there are " + days + " days.");
```
In the above example we can see that:
- `Scanner input = new Scanner(System.in);` allows the program to interpret standard input -> whatever is typed back into the program when run
- The method `input.nextInt()` reads the next token and converts it to an integer, which will crash the program (`InputMismatchException`) if the input isn't a valid int.

### Inputting a whole line vs a single value 
```java 
Scanner input = new Scanner(System.in); System.out.println("What is your name?"); String name = input.nextLine(); System.out.println("How old are you?"); int age = input.nextInt(); System.out.printf("Hello %s, you are %d years old.%n", name, age); 
```
*Output is displayed using a printf() statement -> see [[Formatted Output]] for format specifiers*
- `nextLine()` reads a full line of text and returns it as a `String`
- `nextInt()` reads only the next token and returns it as an `int`
- Other methods exist for different datatypes e.g.`nextDouble()`
### Type mismatch 
If `nextInt()` receives text that isn't a valid integer (e.g. the user types a word instead of a number), Java throws an `InputMismatchException` and the program crashes.
### Mixing nextInt() and nextLine()
- `nextInt()` only consumes the number itself — it leaves the trailing newline character in the input buffer. 
- If a `nextLine()` call follows immediately after, it reads that leftover newline as an empty string instead of waiting for new input. This is a very common first-week bug when combining these two methods.
---
## Covered in
- [[CS1IP_week_02_lecture.pdf]]

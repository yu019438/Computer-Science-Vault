#CS1IP
- Software security is the protection of a software application from threats and vulnerabilities to:
	- Protect sensitive data
	- Maintain software performance integrity 
	- Prevent financial losses
	- Build trust *(in a business environment)*
- Common threats to security:
	- **Malware** -> software designed to exploit users/intend to cause harm
	- **Phishing attempts** -> A device designed to trick users into relinquishing sensitive data
	- **SQL injection** -> Malicious SQL input designed to exploit vulnerabilities in database queries
- Of these, SQL injection is an example of an **adversarial input attack**
## Adversarial Input Attacks
- Adversarial input attacks are malicious inputs intended to exploit vulnerabilities in a program -> It is important to understand how these work in order to design security systems.  
- Types of adversarial input attacks:
	- Algorithmic complexity attacks
	- Buffer overflow attacks
	- SQL Injection attacks
### Algorithmic complexity attacks
- This attacks targets the efficiency of an applications search algorithm
- e.g. Providing input that causes excessive recursion or deep tree traversal, massively slowing down search:
```Java
boolean search(List<Integer> list, int target) {
	return list.contains(target);
}
//Adversarial input
List<Integer> advInput = new LinkedList<>(Collections.nCopies(1_000_000, 0));
advInput.add(1);
search(advInput, 1); //Inefficient for linked lists due to linear traversal
```
- This input forces the algorithm to traverse an immensely large linked list before finding the target -> exploiting the complexity of the `contains()` method
### Buffer overflow attack
- A buffer overflow attacks is when a threat actor writes more data into a buffer than it was designed to hold, causing the excess to spill into adjacent memory (like the return address)
- The danger here is the possible data that the attacker writes to be overflown, as this can rewrite previous instructions with new information telling the program what to do next:
![[Pasted image 20260915160852.png]]
- These attacks are less common in modern languages which can check the buffer automatically, but older languages such as C/C++ are more susceptible to these attacks 
```Java
void processInput(String advInput, int amountToCopy) {
	byte[] buffer = new byte[16];
	for(int i = 0; i < amountToCopy; i++) {
		buffer[i] = (byte) advInput.charAt(i);	
	}
	System.out.println("Buffer content: ");
	for(byte b : buffer) {
		System.out.println((char) b);
	}
	System.out.println();
}
String advInput = "AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA";
int amountToCopy = 24; //Intentionally causes a buffer overflow
processInput(advInput, amountToCopy);
```
### SQL Injection attacks
- SQL injection attacks are when malicious code is fed into a database in order to manipulate queries, possibly revealing sensitive information that would not have previously been made available
```SQL
SELECT * FROM users WHERE username = 'admin' AND password = '' OR '1' = '1'; 
```
- ^ Input manipulates the SQL query to bypass authentication by always evaluating to `True` -> Allowing access into a private database
## How to Prevent Attacks
Ways to program defensively:
- Preventing Null/Empty inputs
- Sanitise user input
- Handle division by 0
- Check array index bounds
---
Related
- [[Algorithms - Big-O Notation]]
- [[Algorithms - Comparing Algorithms]]
- [[Collections]]
- [[Testing]]
## Covered in
- [[CS1IP_week_12_lecture.pdf]]

#CS1IP
## Why compare algorithms?
Different approaches can solve the *same* problem with different time complexities. Comparing brute-force vs optimised versions shows how a change in strategy shifts the [[Algorithms - Big-O Notation|Big-O notation]].

---
## Example: Prime Checking
### Brute Force
```java
boolean isPrime(int n) {
    if (n <= 1) return false;
    for (int i = 2; i < n; i++) {
        if (n % i == 0) return false;
    }
    return true;
}
```
- Time Complexity: $O(n)$
### Optimised
```java
boolean isPrime(int n) {
    if (n <= 1) return false;
    for (int i = 2; i <= Math.sqrt(n); i++) {
        if (n % i == 0) return false;
    }
    return true;
}
```
- Time Complexity: **$O(\sqrt n)$**
- **Insight**: Factors come in pairs either side of $\sqrt n$. Once you've checked up to there, you've already ruled out anything bigger by proxy. Checking further is just re-testing pairs you've already covered from the other direction.
---
## Power Calculation
### Iterative Approach
```java
int power(int base, int exp) {
    int result = 1;
    for (int i = 0; i < exp; i++) {
        result *= base;
    }
    return result;
}
```
- Time Complexity: $O(n)$ -> where $n$ is the exponent
### Exponentiation by Squaring
```java
int power(int base, int exp) {
    if (exp == 0) return 1;
    if (exp % 2 == 0) {
        int half = power(base, exp / 2);
        return half * half;
    } else {
        return base * power(base, exp - 1);
    }
}
```
- Time Complexity: $O(log$ $n)$
- **Insight:** $base^{exp}=(base^{exp/2})^2$.  You never need to do exp multiplications as you just need to solve a problem half the size and square it. Halving the problem each step is what gives you logarithmic depth instead of linear.
---
## Fibonacci Numbers
### Mathematical definition:
- $fib(n) = 0$ if $n = 0$
- $fib(n) = 1$ if $n = 1$
- $fib(n) = fib(n−1) + fib(n−2)$ if $n > 1$
### Naive Recursive
```java
int fib(int n) {
    if (n <= 1) {
        return n; // Base case
    }
    return fib(n - 1) + fib(n - 2);
}
```
- Time Complexity: $O(2^n)$
- **Insight:** Each call branches into two more calls, forming a binary tree of ~$2^n$ nodes. Massive redundant re-computation of the same sub-values.
### With Memoization
```java
int[] memo;
int fib(int n) {
    if (memo[n] != -1) {
        return memo[n]; // Return from memo
    }
    if (n <= 1) {
        return n; // Base case
    }
    memo[n] = fib(n - 1) + fib(n - 2); // Store result
    return memo[n];
}
```
- Time Complexity: **O(n)**
- **Insight:** Each unique Fibonacci value is computed once and cached, eliminating the redundant recursive calls entirely.
---
## Takeaway
None of them made the *algorithm* smarter -> They made it stop doing work it didn't need to.
- Prime checking stops early once it's covered both sides of a factor pair ($n$ -> $\sqrt n$)
- Power calculation reuses one sub-result twice instead of computing it twice ($n$ -> $log(n)$)
- Fibonacci stops recalculating values it's already solved ($2^n$ -> $n$)
---
## Related
- [[Recursion]] (contains examples of)
- [[Algorithms - Big-O Notation]]
- [[Algorithms - Search]]
## Covered in
- [[CS1IP_week_09_lecture.pdf]]
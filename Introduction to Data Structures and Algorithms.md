### Introduction to Data Structures and Algorithms  

**Data Structures** define how data is stored, while **Algorithms** describe the steps to solve problems using these structures. Together, they form the foundation for efficient problem-solving in computer science.  

---

### What are Data Structures?  
A **Data Structure** organizes and stores data effectively, tailored to specific tasks.  

Example: A **family tree** visually represents relationships, making it easy to trace connections across generations.  

#### Types of Data Structures:  
1. **Primitive Data Structures**: Basic types like integers, floats, characters, and booleans.  
2. **Abstract Data Structures**: Built on primitive types, offering more complex operations, e.g., arrays, stacks, queues, trees, and graphs.  

Efficient data structures enable the management of vast amounts of data, such as in databases or search engines.

---

### What are Algorithms?  
An **Algorithm** is a step-by-step method to solve a problem or achieve a goal.  

Example: A recipe for cooking is an algorithm with instructions and ingredients (data structures).  

#### Algorithm Applications:  
- Finding the fastest GPS route.  
- Search engines identifying relevant results.  
- Sorting items (e.g., movies by rating).  

Efficient algorithms improve performance and reduce resource usage.  

---

### Data Structures + Algorithms  
Data structures are the foundation; algorithms make them useful. Together, they:  
- Enable efficient data storage, retrieval, and manipulation.  
- Help solve complex problems systematically.  
- Optimize program speed and memory usage.  

---

### Applications of DSA  
DSA is critical in:  
- Operating systems, databases, and search engines.  
- Scheduling tasks (e.g., in computers or GPS systems).  
- Machine learning, cryptography, and gaming.  

---

### Key Terms to Know:  
| **Term**              | **Description**                                                                 |
|------------------------|---------------------------------------------------------------------------------|
| **Algorithm**          | Step-by-step instructions to solve problems.                                   |
| **Data Structure**     | Organized storage of data for efficiency.                                      |
| **Time Complexity**    | Measures how long an algorithm takes to run.                                   |
| **Space Complexity**   | Measures how much memory an algorithm uses.                                    |
| **Big O Notation**     | Describes the performance limits of an algorithm.                              |
| **Recursion**          | A function that calls itself to solve problems.                                |
| **Divide and Conquer** | Solves problems by breaking them into smaller sub-problems.                    |
| **Brute Force**        | Tries all possible solutions to find the best one.                             |

---

### Simple Algorithm

---

### 1. **Using a For Loop**
This method is efficient and easy to understand:
```javascript
function fibonacciLoop(n) {
  let prev2 = 0, prev1 = 1;
  console.log(prev2);
  console.log(prev1);
  for (let i = 2; i < n; i++) {
    let current = prev1 + prev2;
    console.log(current);
    prev2 = prev1;
    prev1 = current;
  }
}

fibonacciLoop(20); // Generates the first 20 Fibonacci numbers
```

---

### 2. **Using Recursion**
Recursion allows us to express the Fibonacci sequence elegantly but is less efficient:
```javascript
let count = 0;
function fibonacciRecursive(prev1, prev2, n) {
  if (count < n - 2) {
    let current = prev1 + prev2;
    console.log(current);
    count++;
    fibonacciRecursive(current, prev1, n);
  }
}

console.log(0);
console.log(1);
fibonacciRecursive(1, 0, 20); // Generates the first 20 Fibonacci numbers
```

---

### 3. **Finding the Nth Fibonacci Number (Recursion)**
This uses a mathematical approach but becomes inefficient for large `n` due to repeated calculations:
```javascript
function nthFibonacci(n) {
  if (n <= 1) return n;
  return nthFibonacci(n - 1) + nthFibonacci(n - 2);
}

console.log(nthFibonacci(19)); // 20th Fibonacci number (0-based index)
```

---

### 4. **Optimized Nth Fibonacci (Memoization)**
To make recursion efficient, we use memoization:
```javascript
function nthFibonacciMemoized(n, memo = {}) {
  if (n in memo) return memo[n];
  if (n <= 1) return n;
  memo[n] = nthFibonacciMemoized(n - 1, memo) + nthFibonacciMemoized(n - 2, memo);
  return memo[n];
}

console.log(nthFibonacciMemoized(19)); // 20th Fibonacci number
```

---


# Data Structures in C: Stack & Circular Queue

Array-based implementations of two fundamental data structures, with overflow/underflow handling and complexity analysis.

## Contents

| # | Data Structure | Implementation |
|---|----------------|----------------|
| 1 | Stack | Array |
| 2 | Circular Queue | Array |

---

## Q1. Stack using Array

A stack follows the **LIFO** (Last In, First Out) principle.

### Operations

- `PUSH(x)`: insert an element on top of the stack
- `POP()`: remove the top element
- `PEEK()`: return the top element without removing it
- `DISPLAY()`: print all elements of the stack

### Error Handling

- **Stack Overflow**: raised when pushing into a full stack
- **Stack Underflow**: raised when popping or peeking from an empty stack

### Complexity

| Operation | Time |
|-----------|------|
| PUSH | O(1) |
| POP | O(1) |
| PEEK | O(1) |
| DISPLAY | O(n) |

**Space Complexity:** O(n)

---

## Q2. Circular Queue using Array

A queue follows the **FIFO** (First In, First Out) principle. In a circular queue, the last position is connected back to the first, so the array is used as a ring.

### Operations

- `ENQUEUE(x)`: insert an element at the rear
- `DEQUEUE()`: remove an element from the front
- `FRONT()`: return the front element without removing it
- `DISPLAY()`: print all elements from front to rear

### Error Handling

- **Queue Full**: detected when no free position is left for insertion
- **Queue Empty**: detected when there is no element to remove or read

### Complexity

| Operation | Time |
|-----------|------|
| ENQUEUE | O(1) |
| DEQUEUE | O(1) |
| FRONT | O(1) |
| DISPLAY | O(n) |

**Space Complexity:** O(n)

### Circular Queue vs Linear Queue

| Feature | Linear Queue | Circular Queue |
|---------|--------------|----------------|
| Memory usage | Freed positions at the front are not reused | Freed positions are reused |
| Overflow | `REAR` can reach the last index even when empty slots exist at the beginning (false overflow) | Overflow occurs only when the queue is truly full |
| Efficiency | Wastes space | Better space utilization |

A circular queue reuses positions freed at the beginning of the array. In a linear queue, `REAR` can reach the last index even when unused positions exist at the beginning, causing a false overflow condition.

**Katyayni Yadav**
Invertis University

## License

This project is open source and available for learning purposes.

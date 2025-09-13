# Tower of Hanoi (Recursive Solution)

## Overview
The Tower of Hanoi is a classic puzzle that demonstrates the power of recursion.  
You are given **n disks** stacked on one rod (source), arranged in ascending order of size (smallest at the top). The objective is to move the entire stack to another rod (target), using a helper rod, while obeying the rules:

1. Only one disk may be moved at a time.  
2. A disk can only be placed on an empty rod or on top of a larger disk.  
3. All disks must be moved from the source to the target rod.

---

## Implementation
The algorithm works recursively:
1. Move the top `n-1` disks from **source → helper**.  
2. Move the largest disk (`n`) from **source → target**.  
3. Move the `n-1` disks from **helper → target**.  

This breaks the large problem into smaller subproblems until the base case (`n = 0`) is reached.

---

## Complexity
- **Time Complexity:** `O(2^n)` moves (minimum possible).  
- **Space Complexity:** `O(n)` for the recursive call stack.  

---

## Example Usage
```bash
python toh_recursive.py
```

## Example Output (for n = 3):
```bash
Move disk 1 from A → C
Move disk 2 from A → B
Move disk 1 from C → B
Move disk 3 from A → C
Move disk 1 from B → A
Move disk 2 from B → C
Move disk 1 from A → C
```

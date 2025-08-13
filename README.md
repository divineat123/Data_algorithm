# Algorithm Checkpoint

---

## Problem 1: Sum of Distinct Elements
**Description:**  
Given two sets of elements, find the sum of all elements that appear in only one of the sets.

**Algorithm Steps:**
1. Create a variable `total_sum = 0`.
2. For each element in `set1`:
   - Check if it exists in `set2` using a nested loop.
   - If not found, add it to `total_sum`.
3. For each element in `set2`:
   - Check if it exists in `set1` using a nested loop.
   - If not found, add it to `total_sum`.
4. Output `total_sum`.

**Example:**

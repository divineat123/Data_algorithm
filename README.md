# Algorithm Checkpoint

**Author:** Your Name  
**Date:** 13/08/2025  

---

## Description
This file contains solutions for:  
1. Sum of distinct elements from two sets (using arrays and nested loops).  
2. Dot product calculation and orthogonality check.

---

## Problem 1: Sum of Distinct Elements

**Algorithm:**
1. Create a variable `total_sum = 0`
2. For each element in `set1`:
   - Check if it exists in `set2` using a nested loop
   - If not found, add it to `total_sum`
3. For each element in `set2`:
   - Check if it exists in `set1` using a nested loop
   - If not found, add it to `total_sum`
4. Output `total_sum`

**Example Implementation (Python syntax for clarity):**
```python
def sum_distinct_elements(set1, set2):
    total_sum = 0
    for i in range(len(set1)):
        found = False
        for j in range(len(set2)):
            if set1[i] == set2[j]:
                found = True
                break
        if not found:
            total_sum += set1[i]

    for i in range(len(set2)):
        found = False
        for j in range(len(set1)):
            if set2[i] == set1[j]:
                found = True
                break
        if not found:
            total_sum += set2[i]

    return total_sum

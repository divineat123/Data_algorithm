# Algorithms

## Problem 1: Sum of Distinct Elements from Two Sets

### Description
Given two sets of elements, find the sum of all distinct elements that appear in either of the given sets.

Example:  
Set1 = [3, 1, 7, 9]  
Set2 = [2, 4, 1, 9, 3]  
Output = 13 (distinct elements are 4, 7, 2)

---

### Algorithm (Using Arrays)
1. Initialize `sum` ← 0
2. For each element `x` in Set1:
   - Search for `x` in Set2
   - If `x` is **not found**, then:
     - `sum` ← `sum` + `x`
3. For each element `y` in Set2:
   - Search for `y` in Set1
   - If `y` is **not found**, then:
     - `sum` ← `sum` + `y`
4. Output `sum`

---

## Problem 2: Dot Product and Orthogonality Check

### Description
Write a procedure called `dot_product` which calculates, in the variable `ps`, the dot (scalar) product of two vectors `v1` and `v2` (both in IR).  
Then, write an algorithm that determines for `n` pairs of given vectors whether they are orthogonal, by calling `dot_product`.  
Two vectors are orthogonal if their dot product is zero.

---

### Algorithm (Procedure Version)
**Procedure** `dot_product(v1[], v2[], n, ps)`  
1. `ps` ← 0  
2. For `i` from 0 to `n-1`:
   - `ps` ← `ps` + (v1[i] × v2[i])  
**End Procedure**

**Main Algorithm:**
1. Read number of pairs `n_pairs`
2. Repeat for each pair:
   - Read vector size `n`
   - Read vector `v1[]`
   - Read vector `v2[]`
   - Call `dot_product(v1, v2, n, ps)`
   - If `ps` = 0:
     - Output "Vectors are orthogonal"
   - Else:
     - Output "Vectors are not orthogonal"

---

### Algorithm (Function Version)
**Function** `dot_product(v1[], v2[], n)`  
1. `ps` ← 0  
2. For `i` from 0 to `n-1`:
   - `ps` ← `ps` + (v1[i] × v2[i])  
3. Return `ps`  
**End Function**

**Main Algorithm:**
1. Read number of pairs `n_pairs`
2. Repeat for each pair:
   - Read vector size `n`
   - Read vector `v1[]`
   - Read vector `v2[]`
   - `ps` ← `dot_product(v1, v2, n)`
   - If `ps` = 0:
     - Output "Vectors are orthogonal"
   - Else:
     - Output "Vectors are not orthogonal"

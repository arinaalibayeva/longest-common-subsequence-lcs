# longest-common-subsequence-lcs
Dynamic Programming and Greedy Algorithms for Longest Common Subsequence and Genealogy Tree Construction.

# Longest Common Subsequence (LCS) and Genealogy Tree Construction

**Summary**  
Implementation of dynamic programming and greedy algorithms to compute the **Longest Common Subsequence (LCS)**, build **genealogy binary trees** using local and global strategies, and analyze **time complexity** and **mutation probabilities** in a simulated dataset of DNA-like strings.

---

## Project Overview
This project was completed for **CS110: Problem Solving with Data Structures and Algorithms** at Minerva University.  
The objective was to use **dynamic programming** to compute all possible LCS values and analyze relationships between multiple gene-like sequences.

---

## Key Features
- **LCS Computation:**  
  Finds all possible longest common subsequences between two strings.
- **Matrix of LCS Lengths:**  
  Generates a symmetric matrix of pairwise LCS values for 7 labeled sequences.
- **Local (Greedy) Genealogy Tree:**  
  Builds a binary tree by comparing each node with its closest neighbors.
- **Global (DP) Genealogy Tree:**  
  Constructs a globally optimized tree using a “Similarity Ratio Score”.
- **Complexity Analysis:**  
  Empirical and theoretical comparison of time complexities.
- **Probability Estimation:**  
  Calculates insertion, deletion, and mutation probabilities using LCS values.

---

## Methods Summary

| Algorithm | Approach | Complexity | Description |
|------------|-----------|-------------|--------------|
| **LCS** | Dynamic Programming | O(m × n) | Builds DP table for two sequences and backtracks to find all LCSs. |
| **Local Tree (Greedy)** | Greedy BFS | O(n²) | Selects immediate neighbors based on pairwise LCS values. |
| **Global Tree (DP)** | Dynamic Programming | O(n² × m²) | Considers all pairwise similarities using a normalized similarity ratio metric. |

## Results Summary

- Generated a **7×7 LCS matrix** identifying the degree of similarity between strings.  
- Constructed **genealogy trees** using both local and global strategies.  
- Verified that:
  - Global DP algorithm achieves a higher total similarity metric (1442)  
  - Local Greedy algorithm achieves 1336  
- Confirmed **O(n²)** growth experimentally using runtime analysis from n = 10 → 100.  
- Estimated probabilities:  
  - **Insertion:** 0.379  
  - **Deletion:** 0.329  
  - **Mutation:** 0.292  

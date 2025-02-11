# LeetCode Patterns Study Guide

This repository contains a curated list of LeetCode problems organized by common patterns and techniques. 

Each section focuses on specific problem-solving patterns that are frequently used in coding interviews.

## Array String
Common techniques: Array manipulation, string handling, two pointers, in-place operations

1. **Merge Sorted Array** (Easy)
   - Pattern: Two arrays manipulation
   - Key concept: Merging from the end to avoid overwriting elements

2. **Remove Element** (Easy)
   - Pattern: In-place array modification
   - Key concept: Maintaining array order while removing elements

3. **Remove Duplicates From Sorted Array** (Easy)
   - Pattern: Two pointers
   - Key concept: Utilizing sorted property to identify duplicates

4. **Remove Duplicates From Sorted Array II** (Medium)
   - Pattern: Two pointers with counter
   - Key concept: Allowing up to two occurrences of each element

## Two Pointers
Common techniques: Left/right pointers, fast/slow pointers, window sliding

1. **Valid Palindrome** (Easy)
   - Pattern: Two-way string traversal
   - Key concept: Character comparison from both ends

2. **Two Sum II** (Medium)
   - Pattern: Binary search variation
   - Key concept: Using sorted array property to optimize search

3. **Container With Most Water** (Medium)
   - Pattern: Area calculation with two pointers
   - Key concept: Maximizing area between vertical lines

## Sliding Window
Common techniques: Dynamic window size, fixed window size, string/array substring problems

1. **Minimum Size Subarray Sum** (Medium)
   - Pattern: Variable size window
   - Key concept: Finding smallest subarray with sum ≥ target

2. **Longest Substring Without Repeating Characters** (Medium)
   - Pattern: Dynamic window with hash set
   - Key concept: Tracking unique characters in current window

3. **Substring With Concatenation Of All Words** (Hard)
   - Pattern: Fixed window with dictionary
   - Key concept: Handling multiple word combinations

4. **Minimum Window Substring** (Hard)
   - Pattern: Dynamic window with character frequency
   - Key concept: Finding smallest window containing all required characters

## Matrix
Common techniques: 2D array traversal, matrix manipulation, boundary checking

1. **Valid Sudoku** (Medium)
   - Pattern: Grid validation
   - Key concept: Row, column, and box checking

2. **Spiral Matrix** (Medium)
   - Pattern: Layer by layer traversal
   - Key concept: Boundary handling and direction changes

3. **Rotate Image** (Medium)
   - Pattern: Matrix transformation
   - Key concept: In-place rotation using symmetry

4. **Set Matrix Zeroes** (Medium)
   - Pattern: Matrix modification
   - Key concept: Efficient marking of rows and columns

5. **Game Of Life** (Medium)
   - Pattern: Cell simulation
   - Key concept: State tracking and neighbor counting

## Hashmap
Common techniques: Key-value mapping, frequency counting, string matching

1. **Ransom Note** (Easy)
   - Pattern: Character frequency counting
   - Key concept: Comparing character availability

2. **Isomorphic Strings** (Easy)
   - Pattern: Character mapping
   - Key concept: Bi-directional character relationships

3. **Word Pattern** (Easy)
   - Pattern: String-to-pattern mapping
   - Key concept: One-to-one correspondence

4. **Valid Anagram** (Easy)
   - Pattern: Character frequency comparison
   - Key concept: String composition matching

5. **Group Anagrams** (Medium)
   - Pattern: String grouping
   - Key concept: Sorted string as key for grouping

## Intervals
Common techniques: Interval merging, overlap detection, range operations

1. **Summary Ranges** (Easy)
   - Pattern: Range construction
   - Key concept: Consecutive number grouping

2. **Merge Intervals** (Medium)
   - Pattern: Interval merging
   - Key concept: Overlapping interval combination

3. **Insert Interval** (Medium)
   - Pattern: Interval insertion
   - Key concept: Finding correct position and merging

4. **Minimum Number Of Arrows To Burst Balloons** (Medium)
   - Pattern: Interval overlap
   - Key concept: Finding minimum points of overlap

## Stack
Common techniques: LIFO (Last-In-First-Out) operations, parsing, expression evaluation

1. **Valid Parentheses** (Easy)
   - Pattern: Bracket matching
   - Key concept: Using stack to track opening brackets

2. **Simplify Path** (Medium)
   - Pattern: Path parsing
   - Key concept: Directory navigation with stack

3. **Min Stack** (Medium)
   - Pattern: Stack design
   - Key concept: Maintaining minimum value with O(1) operations

4. **Evaluate Reverse Polish Notation** (Medium)
   - Pattern: Expression evaluation
   - Key concept: Postfix notation calculation

5. **Basic Calculator** (Hard)
   - Pattern: Complex expression evaluation
   - Key concept: Operator precedence and parentheses handling

## Linked List
Common techniques: Pointer manipulation, two pointers, dummy nodes

1. **Linked List Cycle** (Easy)
   - Pattern: Fast/slow pointers
   - Key concept: Cycle detection using Floyd's algorithm

2. **Add Two Numbers** (Medium)
   - Pattern: List traversal with carry
   - Key concept: Digit-by-digit addition

3. **Merge Two Sorted Lists** (Easy)
   - Pattern: Merge traversal
   - Key concept: Maintaining sorted order during merge

4. **Copy List With Random Pointer** (Medium)
   - Pattern: Deep copying
   - Key concept: Handling additional pointer relationships

5. **Reverse Linked List II** (Medium)
   - Pattern: Partial reversal
   - Key concept: Reversing specific portion of list

6. **Reverse Nodes In K Group** (Hard)
   - Pattern: Group reversal
   - Key concept: K-size chunk reversal

7. **Remove Nth Node From End Of List** (Medium)
   - Pattern: Two pointers gap
   - Key concept: Finding position from end

## Binary Tree General
Common techniques: Tree traversal, recursion, path finding

1. **Maximum Depth Of Binary Tree** (Easy)
   - Pattern: Depth calculation
   - Key concept: Recursive height determination

2. **Same Tree** (Easy)
   - Pattern: Tree comparison
   - Key concept: Structure and value matching

3. **Invert Binary Tree** (Easy)
   - Pattern: Tree transformation
   - Key concept: Recursive node swapping

4. **Symmetric Tree** (Easy)
   - Pattern: Tree symmetry
   - Key concept: Mirror comparison

5. **Construct Binary Tree From Preorder And Inorder** (Medium)
   - Pattern: Tree construction
   - Key concept: Using traversal properties

6. **Flatten Binary Tree To Linked List** (Medium)
   - Pattern: Tree linearization
   - Key concept: Preorder traversal transformation

7. **Path Sum** (Easy)
   - Pattern: Path traversal
   - Key concept: Root-to-leaf sum validation

## Binary Tree BFS
Common techniques: Level-wise traversal, queue-based processing

1. **Binary Tree Right Side View** (Medium)
   - Pattern: Level-end nodes
   - Key concept: Rightmost node at each level

2. **Average Of Levels In Binary Tree** (Easy)
   - Pattern: Level averaging
   - Key concept: Level-wise value collection

3. **Binary Tree Level Order Traversal** (Medium)
   - Pattern: Level grouping
   - Key concept: Queue-based level separation

## Binary Search Tree
Common techniques: Binary search properties, in-order traversal

1. **Minimum Absolute Difference In BST** (Easy)
   - Pattern: In-order property
   - Key concept: Adjacent value comparison

2. **Kth Smallest Element In a BST** (Medium)
   - Pattern: In-order counting
   - Key concept: Using BST properties for selection

3. **Validate Binary Search Tree** (Medium)
   - Pattern: Range validation
   - Key concept: Maintaining valid value ranges

## Graph General
Common techniques: DFS, BFS, connectivity

1. **Number Of Islands** (Medium)
   - Pattern: Connected components
   - Key concept: Grid-based DFS/BFS

2. **Surrounded Regions** (Medium)
   - Pattern: Border processing
   - Key concept: Outside-in traversal

3. **Course Schedule** (Medium)
   - Pattern: Cycle detection
   - Key concept: Topological sort/cycle check

## Graph BFS
Common techniques: Level-wise traversal, shortest path

1. **Snakes And Ladders** (Medium)
   - Pattern: Shortest path on board
   - Key concept: BFS with game rules

2. **Minimum Genetic Mutation** (Medium)
   - Pattern: String transformation
   - Key concept: Character-wise mutations

3. **Word Ladder** (Hard)
   - Pattern: Word transformation
   - Key concept: Minimal changes path

## Trie
Common techniques: Prefix tree operations, word dictionary

1. **Implement Trie** (Medium)
   - Pattern: Trie implementation
   - Key concept: Character-by-character storage

2. **Word Search II** (Hard)
   - Pattern: Trie with backtracking
   - Key concept: Grid word search optimization

## Backtracking
Common techniques: State exploration, constraint satisfaction

1. **Letter Combinations Of A Phone Number** (Medium)
   - Pattern: String combination
   - Key concept: Digit-to-letter mapping

2. **Generate Parentheses** (Medium)
   - Pattern: Valid sequence generation
   - Key concept: Opening/closing bracket balance

3. **Word Search** (Medium)
   - Pattern: Grid exploration
   - Key concept: Path finding with backtrack

## Divide Conquer
Common techniques: Problem subdivision, merge results

1. **Sort List** (Medium)
   - Pattern: Merge sort
   - Key concept: List splitting and merging

2. **Merge K Sorted Lists** (Hard)
   - Pattern: Multi-way merge
   - Key concept: Efficient list combination

## Binary Search
Common techniques: Search space reduction, sorted array properties

1. **Search Insert Position** (Easy)
   - Pattern: Position finding
   - Key concept: Insertion point in sorted array

2. **Search In Rotated Sorted Array** (Medium)
   - Pattern: Modified binary search
   - Key concept: Handling rotation point

3. **Find First And Last Position** (Medium)
   - Pattern: Range boundaries
   - Key concept: Finding exact ranges

## Heap
Common techniques: Priority queue, k-element processing

1. **Find Median From Data Stream** (Hard)
   - Pattern: Two heaps
   - Key concept: Balanced median maintenance

2. **Kth Largest Element In An Array** (Medium)
   - Pattern: Selection
   - Key concept: Heap-based selection

3. **IPO** (Hard)
   - Pattern: Greedy with heap
   - Key concept: Profit maximization

## Bit Manipulation
Common techniques: Bit operations, binary representation

1. **Add Binary** (Easy)
   - Pattern: Bit addition
   - Key concept: Carry handling

2. **Reverse Bits** (Easy)
   - Pattern: Bit reversal
   - Key concept: Position swapping

3. **Number Of 1 Bits** (Easy)
   - Pattern: Bit counting
   - Key concept: Set bit calculation

4. **Single Number** (Easy)
   - Pattern: XOR
   - Key concept: Duplicate elimination

## Math
Common techniques: Mathematical properties, numeric operations

1. **Palindrome Number** (Easy)
   - Pattern: Number properties
   - Key concept: Digit comparison

2. **Plus One** (Easy)
   - Pattern: Array addition
   - Key concept: Carry propagation

3. **Pow(x,n)** (Medium)
   - Pattern: Fast power
   - Key concept: Binary exponentiation

## 1D DP
Common techniques: State transition, optimal substructure

1. **Climbing Stairs** (Easy)
   - Pattern: Fibonacci-like
   - Key concept: Step combinations

2. **House Robber** (Medium)
   - Pattern: Maximum with constraints
   - Key concept: Non-adjacent selection

3. **Word Break** (Medium)
   - Pattern: String segmentation
   - Key concept: Substring validity

## Multidimensional DP
Common techniques: Matrix DP, multiple state dimensions

1. **Triangle** (Medium)
   - Pattern: Path finding
   - Key concept: Bottom-up minimization

2. **Minimum Path Sum** (Medium)
   - Pattern: Grid traversal
   - Key concept: Cumulative minimum path

3. **Best Time To Buy And Sell Stock III** (Hard)
   - Pattern: State machine
   - Key concept: Limited transactions
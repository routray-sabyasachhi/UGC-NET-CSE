# Data Structures and Algorithms

This folder is for data structures, algorithms, and interview problem solving. It is also useful for UGC NET CSE preparation because DSA questions usually test definitions, time complexity, recurrence solving, traversal logic, and algorithm design techniques.

## How To Use This Notes File

- Learn the concept first, then memorize important operations and complexities.
- Practice dry runs for algorithms such as binary search, DFS, BFS, heap operations, quick sort, merge sort, and dynamic programming.
- For every problem, identify the input size, expected output, data structure used, and time-space complexity.
- Revisit solved problems after a few days and write down mistakes.

## 1. Introduction

### 1.1 Variables

A variable is a named memory location used to store a value. Algorithms use variables to hold counters, indexes, temporary values, flags, references, and results.

### 1.2 Data Types

Data types define the kind of value a variable can store and the operations allowed on it. Common data types include integer, float, character, boolean, string, array, pointer/reference, and user-defined types.

### 1.3 Data Structures

A data structure is a method of organizing data so that operations such as access, insertion, deletion, search, and update can be performed efficiently. Examples include arrays, linked lists, stacks, queues, trees, graphs, hash tables, and heaps.

### 1.4 Abstract Data Types

An Abstract Data Type (ADT) describes what operations are supported without specifying how they are implemented. For example, a stack ADT supports `push`, `pop`, and `peek`; it may be implemented using an array or linked list.

### 1.5 Algorithm

An algorithm is a finite sequence of clear steps used to solve a problem. A good algorithm must be correct, finite, unambiguous, and efficient.

### 1.6 Analysis of Algorithms

Algorithm analysis compares algorithms based on resource usage, mainly time and memory. It helps choose the best approach for large inputs.

### 1.7 Running Time Analysis

Running time analysis estimates how the number of operations grows with input size `n`. It usually ignores machine-dependent constants and focuses on growth rate.

### 1.8 Comparing Algorithms

Algorithms are compared using time complexity, space complexity, simplicity, scalability, stability, and suitability for the input constraints.

### 1.9 Rate of Growth

Rate of growth describes how quickly running time increases as input size grows. For example, `O(log n)` grows slower than `O(n)`, and `O(n log n)` grows slower than `O(n^2)`.

### 1.10 Common Growth Rates

Common complexities from faster to slower are:

- `O(1)`: constant time
- `O(log n)`: logarithmic time
- `O(n)`: linear time
- `O(n log n)`: linearithmic time
- `O(n^2)`, `O(n^3)`: polynomial time
- `O(2^n)`: exponential time
- `O(n!)`: factorial time

### 1.11 Types of Analysis

- Best case: minimum time for the most favorable input.
- Average case: expected time over all typical inputs.
- Worst case: maximum time for any input of size `n`.

### 1.12 Asymptotic Notation

Asymptotic notation describes algorithm growth for large input sizes.

- Big-O `O`: upper bound.
- Omega `Omega`: lower bound.
- Theta `Theta`: tight bound.

### 1.13 Big-O Notation

Big-O gives an upper bound on running time. If an algorithm is `O(n^2)`, its running time does not grow faster than a constant multiple of `n^2` for large `n`.

### 1.14 Omega Notation

Omega gives a lower bound. If an algorithm is `Omega(n)`, it takes at least linear time for sufficiently large input.

### 1.15 Theta Notation

Theta gives a tight bound. If an algorithm is `Theta(n log n)`, its running time grows exactly in the order of `n log n`.

### 1.16 Important Asymptotic Rules

- Drop constants: `O(5n)` becomes `O(n)`.
- Keep the highest-order term: `O(n^2 + n)` becomes `O(n^2)`.
- Sequential code adds complexities.
- Nested loops usually multiply complexities.
- Divide-and-conquer recurrences are often solved using recursion trees or Master Theorem.

### 1.17 Logarithms and Summations

Important formulas:

- `log(ab) = log a + log b`
- `log(a^b) = b log a`
- `1 + 2 + ... + n = n(n + 1) / 2`
- `1 + 2 + 4 + ... + 2^k = 2^(k + 1) - 1`

### 1.18 Master Theorem

For recurrences of the form `T(n) = aT(n/b) + f(n)`:

- If `f(n)` is smaller than `n^(log_b a)`, then `T(n) = Theta(n^(log_b a))`.
- If `f(n)` is equal to `n^(log_b a)`, then `T(n) = Theta(n^(log_b a) log n)`.
- If `f(n)` is larger than `n^(log_b a)`, then `T(n) = Theta(f(n))`, if the regularity condition holds.

### 1.19 Subtract and Conquer Recurrences

Subtract and conquer reduces the problem by a constant or variable amount, such as `T(n) = T(n - 1) + n`. It commonly appears in insertion sort, selection sort, and recursive linear search.

### 1.20 Amortized Analysis

Amortized analysis finds the average cost per operation over a sequence of operations, even if some individual operations are expensive. Dynamic array resizing is a common example.

## 2. Recursion and Backtracking

### 2.1 Recursion

Recursion is a technique where a function calls itself to solve a smaller version of the same problem. Every recursive function must have a base case and a recursive case.

### 2.2 Recursive Function Format

A recursive function usually contains:

- Base condition to stop recursion.
- Work done at the current step.
- Recursive call on a smaller input.
- Optional combination of results.

### 2.3 Recursion and Memory

Each recursive call is stored in the call stack with its own local variables. Deep recursion may cause stack overflow.

### 2.4 Recursion vs Iteration

Iteration uses loops and generally consumes less memory. Recursion can make tree, graph, divide-and-conquer, and backtracking algorithms easier to express.

### 2.5 Backtracking

Backtracking is a controlled recursion technique that builds a solution step by step and abandons a path when it cannot lead to a valid answer. It is used in N-Queens, Sudoku, permutations, combinations, and subset problems.

## 3. Linked Lists

### 3.1 Linked List

A linked list is a linear data structure where elements are stored in nodes. Each node contains data and one or more links to other nodes.

### 3.2 Why Linked Lists?

Linked lists support efficient insertion and deletion when the node position is known. They do not require contiguous memory, unlike arrays.

### 3.3 Arrays vs Linked Lists

Arrays provide `O(1)` random access but costly middle insertion/deletion. Linked lists provide sequential access and easier insertion/deletion but require extra memory for links.

### 3.4 Types of Linked Lists

- Singly linked list: each node points to the next node.
- Doubly linked list: each node points to previous and next nodes.
- Circular linked list: last node links back to the first node.
- Unrolled linked list: each node stores multiple elements.
- Skip list: layered linked structure that supports fast search on average.

## 4. Stacks

### 4.1 Stack

A stack is a linear ADT that follows LIFO: Last In, First Out. The last inserted element is removed first.

### 4.2 Stack Operations

- `push`: insert an element.
- `pop`: remove the top element.
- `peek/top`: read the top element.
- `isEmpty`: check whether the stack has no elements.

### 4.3 Applications

Stacks are used in expression evaluation, balanced parentheses, recursion, undo operations, browser history, DFS, and function call management.

### 4.4 Implementation

A stack can be implemented using an array or linked list. Array implementation is simple but may need resizing; linked list implementation grows dynamically.

## 5. Queues

### 5.1 Queue

A queue is a linear ADT that follows FIFO: First In, First Out. The first inserted element is removed first.

### 5.2 Queue Operations

- `enqueue`: insert at rear.
- `dequeue`: remove from front.
- `front`: read the first element.
- `isEmpty`: check whether the queue is empty.

### 5.3 Applications

Queues are used in scheduling, buffering, BFS, printer queues, CPU task management, and producer-consumer systems.

### 5.4 Types of Queues

- Simple queue
- Circular queue
- Double-ended queue
- Priority queue

## 6. Trees

### 6.1 Tree

A tree is a hierarchical data structure made of nodes and edges. It has a root node, parent-child relationships, and no cycles.

### 6.2 Important Terms

Root, parent, child, sibling, leaf, internal node, degree, level, height, depth, subtree, and path are common tree terms.

### 6.3 Binary Tree

A binary tree is a tree where each node has at most two children: left child and right child.

### 6.4 Types of Binary Trees

- Full binary tree: every node has either 0 or 2 children.
- Complete binary tree: all levels are filled except possibly the last, filled left to right.
- Perfect binary tree: all internal nodes have two children and all leaves are at the same level.
- Balanced binary tree: height is kept small, usually `O(log n)`.

### 6.5 Tree Traversals

- Inorder: left, root, right.
- Preorder: root, left, right.
- Postorder: left, right, root.
- Level order: breadth-first traversal using a queue.

### 6.6 Binary Search Tree

A Binary Search Tree (BST) stores values so that left subtree values are smaller and right subtree values are larger than the root. Search, insert, and delete are `O(h)`, where `h` is tree height.

### 6.7 Balanced Trees

Balanced trees such as AVL trees and Red-Black trees keep height near `O(log n)`, improving search and update operations.

### 6.8 Expression Trees

Expression trees represent arithmetic expressions. Operators are internal nodes and operands are leaf nodes.

## 7. Priority Queues and Heaps

### 7.1 Priority Queue

A priority queue removes elements according to priority instead of insertion order.

### 7.2 Heap

A heap is a complete binary tree that satisfies the heap property.

- Max heap: parent is greater than or equal to children.
- Min heap: parent is less than or equal to children.

### 7.3 Heap Operations

- Insert: `O(log n)`
- Delete root/extract min or max: `O(log n)`
- Peek min or max: `O(1)`
- Build heap: `O(n)`

### 7.4 Heapsort

Heapsort builds a heap and repeatedly extracts the root. Its time complexity is `O(n log n)` and it sorts in-place, but it is not stable.

## 8. Disjoint Sets ADT

### 8.1 Disjoint Set

Disjoint Set Union (DSU), also called Union-Find, manages non-overlapping sets.

### 8.2 Operations

- `find(x)`: returns the representative of the set containing `x`.
- `union(a, b)`: merges the sets containing `a` and `b`.

### 8.3 Optimizations

Path compression and union by rank/size make operations nearly constant time in practice.

### 8.4 Applications

DSU is used in Kruskal's algorithm, cycle detection in undirected graphs, connected components, and equivalence class problems.

## 9. Graph Algorithms

### 9.1 Graph

A graph consists of vertices and edges. Graphs may be directed or undirected, weighted or unweighted, connected or disconnected, cyclic or acyclic.

### 9.2 Graph Representation

- Adjacency matrix: good for dense graphs; uses `O(V^2)` space.
- Adjacency list: good for sparse graphs; uses `O(V + E)` space.

### 9.3 Graph Traversals

- BFS uses a queue and explores level by level.
- DFS uses recursion or a stack and explores deeply before backtracking.

### 9.4 Topological Sort

Topological sorting orders vertices of a Directed Acyclic Graph (DAG) so that every directed edge `u -> v` places `u` before `v`.

### 9.5 Shortest Path Algorithms

- BFS: shortest path in an unweighted graph.
- Dijkstra: shortest path with non-negative weights.
- Bellman-Ford: handles negative edges and detects negative cycles.
- Floyd-Warshall: all-pairs shortest paths.

### 9.6 Minimum Spanning Tree

A Minimum Spanning Tree connects all vertices with minimum total edge weight.

- Kruskal's algorithm uses sorting and DSU.
- Prim's algorithm grows the MST using a priority queue.

## 10. Sorting

### 10.1 Sorting

Sorting arranges data in a specific order, usually ascending or descending. It makes searching, merging, duplicate detection, and ranking easier.

### 10.2 Classification

Sorting algorithms can be classified as comparison-based or non-comparison-based, stable or unstable, internal or external, recursive or iterative, and in-place or not in-place.

### 10.3 Basic Sorting Algorithms

- Bubble sort: repeatedly swaps adjacent wrong-order elements; `O(n^2)`.
- Selection sort: repeatedly selects the minimum element; `O(n^2)`.
- Insertion sort: inserts each element into a sorted prefix; `O(n^2)`, good for small or nearly sorted data.

### 10.4 Efficient Comparison Sorting

- Merge sort: divide and conquer; `O(n log n)`, stable, needs extra space.
- Quick sort: partition-based; average `O(n log n)`, worst `O(n^2)`.
- Heap sort: heap-based; `O(n log n)`, in-place, not stable.

### 10.5 Linear Sorting Algorithms

- Counting sort: works when key range is small.
- Bucket sort: distributes values into buckets.
- Radix sort: sorts digits/characters position by position.

### 10.6 External Sorting

External sorting is used when data is too large to fit in main memory. External merge sort is a common technique.

## 11. Searching

### 11.1 Searching

Searching finds whether an element exists and often returns its position.

### 11.2 Linear Search

Linear search checks elements one by one. It works on unsorted data and takes `O(n)` time.

### 11.3 Binary Search

Binary search works on sorted data by repeatedly dividing the search range in half. It takes `O(log n)` time.

### 11.4 Interpolation Search

Interpolation search estimates the likely position of a key in uniformly distributed sorted data. Average time can be `O(log log n)`, but worst case is `O(n)`.

### 11.5 Hash-Based Searching

Hash tables support average `O(1)` search, insert, and delete, but performance depends on hash function quality and collision handling.

## 12. Selection Algorithms

### 12.1 Selection Problem

Selection algorithms find the kth smallest or kth largest element without necessarily sorting the whole array.

### 12.2 Selection by Sorting

Sort the array and return the kth element. This takes `O(n log n)`.

### 12.3 Quickselect

Quickselect uses partitioning like quick sort. Its average time is `O(n)`, but worst case is `O(n^2)`.

### 12.4 Median of Medians

Median of Medians guarantees linear time selection by choosing a good pivot. It is theoretically important but has a larger constant factor.

## 13. Symbol Tables

### 13.1 Symbol Table

A symbol table stores key-value pairs and supports insert, search, delete, and update operations.

### 13.2 Implementations

Symbol tables can be implemented using unsorted arrays, sorted arrays, linked lists, binary search trees, balanced trees, or hash tables.

### 13.3 Applications

Symbol tables are used in compilers, interpreters, dictionaries, databases, caches, and indexing systems.

## 14. Hashing

### 14.1 Hashing

Hashing maps keys to array indexes using a hash function. It aims to provide fast search, insertion, and deletion.

### 14.2 Hash Table ADT

A hash table supports key-value operations such as put, get, remove, and contains.

### 14.3 Hash Function

A good hash function distributes keys uniformly, is fast to compute, and minimizes collisions.

### 14.4 Load Factor

Load factor is `number of elements / table size`. A high load factor increases collisions and may require resizing.

### 14.5 Collisions

A collision occurs when two keys map to the same index.

### 14.6 Collision Resolution

- Separate chaining: each table index stores a list or bucket.
- Open addressing: finds another empty slot using probing.
- Linear probing, quadratic probing, and double hashing are common probing methods.

### 14.7 Bloom Filter

A Bloom filter is a probabilistic data structure used to test set membership. It may give false positives but never false negatives.

## 15. String Algorithms

### 15.1 String Matching

String matching finds occurrences of a pattern in a text.

### 15.2 Brute Force Matching

The brute force method checks the pattern at every possible position. Worst-case time is `O(nm)`.

### 15.3 Rabin-Karp

Rabin-Karp uses hashing to compare pattern and substring hashes. It is useful for multiple pattern matching but may need collision checks.

### 15.4 KMP Algorithm

KMP uses the LPS table to avoid rechecking characters after a mismatch. It runs in `O(n + m)`.

### 15.5 Boyer-Moore

Boyer-Moore compares from right to left and uses skip rules. It is very efficient in practice for large alphabets.

### 15.6 Tries

A trie stores strings character by character. It supports fast prefix search and dictionary operations.

### 15.7 Suffix Trees

Suffix trees store all suffixes of a string and support advanced substring queries efficiently.

## 16. Algorithm Design Techniques

### 16.1 Design Techniques

Algorithm design techniques are general strategies for solving problems. Important techniques include brute force, recursion, backtracking, divide and conquer, greedy method, dynamic programming, randomized algorithms, and branch and bound.

### 16.2 Classification by Implementation

Algorithms may be recursive, iterative, serial, parallel, deterministic, or randomized.

### 16.3 Classification by Design Method

Algorithms may be based on brute force, decrease and conquer, divide and conquer, transform and conquer, greedy choice, dynamic programming, or approximation.

## 17. Greedy Algorithms

### 17.1 Greedy Strategy

A greedy algorithm builds a solution by choosing the locally best option at each step.

### 17.2 When Greedy Works

Greedy works when the problem has the greedy-choice property and optimal substructure.

### 17.3 Advantages and Disadvantages

Greedy algorithms are usually simple and fast, but they do not always produce an optimal answer.

### 17.4 Applications

Examples include activity selection, fractional knapsack, Huffman coding, Prim's algorithm, Kruskal's algorithm, and Dijkstra's algorithm.

## 18. Divide and Conquer Algorithms

### 18.1 Strategy

Divide and conquer solves a problem by dividing it into smaller subproblems, solving them recursively, and combining the results.

### 18.2 Steps

- Divide the problem.
- Conquer each subproblem.
- Combine the subproblem results.

### 18.3 Applications

Merge sort, quick sort, binary search, closest pair of points, Strassen matrix multiplication, and fast exponentiation use divide and conquer ideas.

### 18.4 Advantages and Disadvantages

Divide and conquer often leads to efficient algorithms and natural parallelism, but recursion may add memory overhead and combining results may be costly.

## 19. Dynamic Programming

### 19.1 Dynamic Programming

Dynamic Programming (DP) solves problems by storing results of overlapping subproblems.

### 19.2 Properties

DP is useful when a problem has:

- Overlapping subproblems.
- Optimal substructure.

### 19.3 Approaches

- Memoization: top-down recursion with caching.
- Tabulation: bottom-up table filling.

### 19.4 Common DP Problems

Common examples include Fibonacci numbers, 0/1 knapsack, longest common subsequence, matrix chain multiplication, edit distance, coin change, and shortest paths.

### 19.5 Longest Common Subsequence

LCS finds the longest sequence that appears in two strings in the same relative order. It is a classic `O(nm)` DP problem.

## 20. Complexity Classes

### 20.1 Polynomial and Exponential Time

Polynomial-time algorithms run in `O(n^k)` for some constant `k`. Exponential-time algorithms such as `O(2^n)` grow much faster and become impractical for large `n`.

### 20.2 Decision Problem

A decision problem has a yes/no answer, such as "Does a path exist between two vertices?"

### 20.3 Complexity Class

A complexity class groups problems by the resources needed to solve them.

### 20.4 Important Classes

- P: problems solvable in polynomial time.
- NP: problems whose solutions can be verified in polynomial time.
- NP-Complete: hardest problems in NP; if one is solved in polynomial time, all NP problems are.
- NP-Hard: at least as hard as NP-Complete problems, but not necessarily in NP.

### 20.5 Reductions

A reduction transforms one problem into another. Reductions are used to prove hardness and compare problem difficulty.

## 21. Arrays and Matrices

### 21.1 Arrays

An array stores elements in contiguous memory locations. It supports direct index access in `O(1)` time, which makes it one of the most important basic data structures.

### 21.2 Array Operations

- Access by index: `O(1)`
- Search in unsorted array: `O(n)`
- Insert at end: `O(1)` if space is available
- Insert at middle: `O(n)` because shifting is required
- Delete from middle: `O(n)` because shifting is required

### 21.3 Dynamic Arrays

A dynamic array grows automatically when capacity is full. Resizing may take `O(n)` time, but append is `O(1)` amortized.

### 21.4 Matrices

A matrix is a two-dimensional array arranged in rows and columns. Matrix problems often involve traversal, rotation, transpose, spiral order, prefix sums, and graph-like movement.

### 21.5 Common Matrix Traversals

- Row-wise traversal
- Column-wise traversal
- Diagonal traversal
- Spiral traversal
- Boundary traversal
- BFS/DFS in grid problems

## 22. Bit Manipulation

### 22.1 Bits

Bit manipulation works directly with binary representation. It is useful for fast arithmetic, flags, subsets, masks, and optimization problems.

### 22.2 Common Bit Operators

- AND `&`: checks common set bits.
- OR `|`: sets bits.
- XOR `^`: toggles bits and cancels equal values.
- NOT `~`: flips bits.
- Left shift `<<`: multiplies by powers of 2.
- Right shift `>>`: divides by powers of 2 for non-negative integers.

### 22.3 Important Bit Tricks

- Check even/odd: `n & 1`
- Check if kth bit is set: `n & (1 << k)`
- Set kth bit: `n | (1 << k)`
- Clear kth bit: `n & ~(1 << k)`
- Toggle kth bit: `n ^ (1 << k)`
- Remove lowest set bit: `n & (n - 1)`
- Check power of two: `n > 0 && (n & (n - 1)) == 0`

### 22.4 Bitmasking

Bitmasking represents a set using bits. It is used in subset generation, DP over subsets, permission flags, and state compression.

## 23. Problem-Solving Patterns

### 23.1 Two Pointers

The two-pointer technique uses two indexes to scan data efficiently. It is common in sorted arrays, pair-sum problems, removing duplicates, merging arrays, and palindrome checks.

### 23.2 Sliding Window

Sliding window maintains a moving range over an array or string. It is useful for subarray and substring problems involving maximum, minimum, count, sum, or frequency.

### 23.3 Prefix Sum

Prefix sum stores cumulative sums so that range sum queries can be answered in `O(1)` after `O(n)` preprocessing.

### 23.4 Difference Array

A difference array supports efficient range updates. After all updates, prefix sum reconstructs the final array.

### 23.5 Frequency Counting

Frequency counting uses arrays or hash maps to count occurrences. It is useful for anagrams, duplicates, majority element, and counting-based problems.

### 23.6 Fast and Slow Pointers

Fast and slow pointers are used to detect cycles, find the middle of a linked list, and solve problems involving repeated states.

### 23.7 Monotonic Stack

A monotonic stack keeps elements in increasing or decreasing order. It is used for next greater element, previous smaller element, stock span, largest rectangle in histogram, and daily temperatures.

### 23.8 Monotonic Queue

A monotonic queue maintains ordered candidates in a sliding window. It is used for sliding window maximum/minimum in `O(n)`.

## 24. Range Query Data Structures

### 24.1 Segment Tree

A segment tree stores information about intervals and supports range queries and point updates in `O(log n)`. It can answer range sum, minimum, maximum, gcd, and custom associative queries.

### 24.2 Lazy Propagation

Lazy propagation extends segment trees to handle range updates efficiently. Pending updates are stored and pushed only when needed.

### 24.3 Fenwick Tree

A Fenwick Tree, or Binary Indexed Tree, supports prefix queries and point updates in `O(log n)` using less code and memory than a segment tree.

### 24.4 Sparse Table

A sparse table answers static range queries such as range minimum query in `O(1)` after `O(n log n)` preprocessing. It does not support efficient updates.

## 25. Advanced Tree Data Structures

### 25.1 B-Tree

A B-Tree is a balanced multiway search tree used in databases and file systems. It reduces disk access by storing many keys in each node.

### 25.2 B+ Tree

A B+ Tree stores actual records at leaf nodes and links leaves for fast range queries. It is widely used in database indexing.

### 25.3 Splay Tree

A splay tree is a self-adjusting BST that moves recently accessed elements near the root. It has amortized `O(log n)` operations.

### 25.4 Treap

A treap combines BST ordering with heap priority. It uses random priorities to maintain expected balance.

### 25.5 Trie Variants

Compressed tries, suffix tries, and bitwise tries are used for efficient string storage, prefix matching, and maximum XOR queries.

## 26. Advanced Graph Algorithms

### 26.1 Connected Components

Connected components are groups of vertices where each vertex is reachable from every other vertex in the same group. DFS, BFS, or DSU can find components.

### 26.2 Strongly Connected Components

Strongly Connected Components (SCCs) exist in directed graphs where every vertex in a component can reach every other vertex in that component. Kosaraju's and Tarjan's algorithms find SCCs in `O(V + E)`.

### 26.3 Bridges

A bridge is an edge whose removal increases the number of connected components. Bridges are found using DFS discovery time and low-link values.

### 26.4 Articulation Points

An articulation point is a vertex whose removal increases the number of connected components. These are important in network reliability problems.

### 26.5 Bipartite Graph

A graph is bipartite if its vertices can be divided into two sets such that no edge connects vertices within the same set. BFS or DFS coloring can test bipartiteness.

### 26.6 Euler Path and Circuit

An Euler path uses every edge exactly once. An Euler circuit starts and ends at the same vertex while using every edge exactly once.

### 26.7 Hamiltonian Path and Circuit

A Hamiltonian path visits every vertex exactly once. A Hamiltonian circuit starts and ends at the same vertex. These problems are generally harder than Euler problems.

### 26.8 Network Flow

Network flow studies how much flow can pass from a source to a sink in a directed graph with capacities. Ford-Fulkerson and Edmonds-Karp are standard algorithms.

### 26.9 Matching

Matching selects edges so that no two selected edges share a vertex. Bipartite matching is solved using augmenting paths and has applications in assignment problems.

## 27. Advanced Dynamic Programming

### 27.1 DP on Trees

Tree DP solves problems where answers for a node depend on answers from its children or parent. It is used in independent set on trees, tree diameter variants, and subtree optimization.

### 27.2 Bitmask DP

Bitmask DP stores states using subsets. It is useful when `n` is small, usually up to 20 to 25, and appears in travelling salesman style problems.

### 27.3 Digit DP

Digit DP counts numbers satisfying constraints within a range by processing digits from left to right with states such as position, tight bound, and started flag.

### 27.4 Interval DP

Interval DP solves problems over ranges. Matrix chain multiplication, palindrome partitioning, and optimal binary search tree are common examples.

### 27.5 DP with State Optimization

State optimization reduces memory or time by removing unnecessary dimensions, using rolling arrays, compressing states, or changing the order of computation.

### 27.6 DP on Graphs

DP on DAGs uses topological order. Shortest path in DAGs, longest path in DAGs, and counting paths can be solved this way.

## 28. Randomized Algorithms

### 28.1 Randomized Algorithm

A randomized algorithm uses random choices during execution. Randomness may improve average performance or simplify the algorithm.

### 28.2 Las Vegas Algorithms

Las Vegas algorithms always produce the correct answer, but running time may vary. Randomized quicksort is a common example.

### 28.3 Monte Carlo Algorithms

Monte Carlo algorithms have bounded running time but may return an incorrect answer with small probability. Probabilistic primality tests are examples.

### 28.4 Randomized Quick Sort

Randomized quick sort chooses a random pivot to reduce the chance of worst-case partitioning. Expected time is `O(n log n)`.

## 29. Approximation Algorithms

### 29.1 Approximation Algorithm

An approximation algorithm finds a near-optimal solution for optimization problems where exact solutions are too expensive.

### 29.2 Approximation Ratio

The approximation ratio measures how close the algorithm's solution is to the optimal solution.

### 29.3 Applications

Approximation algorithms are used for vertex cover, set cover, travelling salesman variants, scheduling, and facility location.

## 30. Branch and Bound

### 30.1 Branch and Bound

Branch and bound explores a search tree like backtracking but uses bounds to discard branches that cannot improve the current best answer.

### 30.2 Difference from Backtracking

Backtracking usually checks feasibility. Branch and bound is mainly used for optimization and compares possible best values.

### 30.3 Applications

Common applications include 0/1 knapsack, travelling salesman problem, assignment problem, and integer programming.

## 31. Lower Bounds

### 31.1 Lower Bound

A lower bound proves that no algorithm can solve a problem faster than a certain complexity under a given model of computation.

### 31.2 Sorting Lower Bound

Any comparison-based sorting algorithm requires `Omega(n log n)` comparisons in the worst case.

### 31.3 Searching Lower Bound

Unsorted searching requires `Omega(n)` comparisons in the worst case. Binary search achieves `O(log n)` only when data is sorted.

### 31.4 Decision Tree Model

The decision tree model represents comparisons as branches. It is commonly used to prove lower bounds for comparison sorting.

## 32. NP-Completeness Examples

### 32.1 SAT

Boolean Satisfiability (SAT) asks whether a Boolean formula has an assignment that makes it true. SAT was the first problem proven NP-Complete.

### 32.2 3-SAT

3-SAT is a restricted SAT problem where each clause has exactly three literals. It is also NP-Complete.

### 32.3 Clique

The clique problem asks whether a graph contains a complete subgraph of size `k`. It is NP-Complete.

### 32.4 Vertex Cover

Vertex cover asks whether there is a set of at most `k` vertices that touches every edge. It is NP-Complete.

### 32.5 Hamiltonian Cycle

Hamiltonian cycle asks whether a graph has a cycle that visits every vertex exactly once. It is NP-Complete.

### 32.6 Travelling Salesman Problem

The decision version of TSP asks whether there is a tour of cost at most `k`. It is NP-Complete.

## Quick Complexity Table

| Data Structure / Algorithm | Average Time | Important Note |
| --- | --- | --- |
| Array access | `O(1)` | Direct index access |
| Linked list search | `O(n)` | Sequential access |
| Stack push/pop | `O(1)` | LIFO |
| Queue enqueue/dequeue | `O(1)` | FIFO |
| Binary search | `O(log n)` | Requires sorted data |
| BST search | `O(h)` | `h` is tree height |
| Balanced BST search | `O(log n)` | Height is controlled |
| Hash table search | `O(1)` | Average case |
| BFS/DFS | `O(V + E)` | Graph traversal |
| Merge sort | `O(n log n)` | Stable, extra space |
| Quick sort | `O(n log n)` | Average case |
| Heap sort | `O(n log n)` | In-place, not stable |
| Dijkstra | `O((V + E) log V)` | With priority queue |
| Segment tree query/update | `O(log n)` | Range queries and updates |
| Fenwick tree query/update | `O(log n)` | Prefix queries and point updates |
| Sparse table query | `O(1)` | Static idempotent range queries |
| KMP string matching | `O(n + m)` | Uses LPS table |
| SCC algorithms | `O(V + E)` | Kosaraju or Tarjan |
| Network flow | varies | Depends on algorithm and capacities |

## Practice Plan

- Start with arrays, strings, recursion, stacks, and queues.
- Move to linked lists, trees, heaps, and hashing.
- Learn bit manipulation, two pointers, sliding window, prefix sums, and monotonic stack/queue patterns.
- Practice segment tree, Fenwick tree, and sparse table for range query problems.
- Practice graph traversal, shortest paths, MST, and topological sort.
- Add advanced graph topics: SCC, bridges, articulation points, bipartite matching, and network flow.
- Learn sorting and searching complexities by heart.
- Solve dynamic programming problems only after recursion and recurrence basics are clear, then move to tree DP, bitmask DP, digit DP, and interval DP.
- Study randomized, approximation, branch-and-bound, lower-bound, and NP-completeness topics for theory questions.
- For every solved problem, write the approach, complexity, and one common mistake.

## Goal

I should be able to solve common DSA problems, explain the chosen data structure or algorithm, and analyze time and space complexity clearly.

# Binary Search Tree (BST) - Python Implementation

This repository contains a Python implementation of a **Binary Search Tree (BST)**.

## Overview

A **Binary Search Tree** is a hierarchical data structure where each node follows the rule:
- Values **smaller** than the current node are placed in the **left subtree**.
- Values **greater** than the current node are placed in the **right subtree**.

While BSTs share some similarities with **heaps** (which are array-based), they are fundamentally different. 
- A **heap** is a complete binary tree where nodes are filled **left to right** without gaps.
- A **BST** organizes nodes based on value comparisons.

## Implementation Details

The BST implementation consists of a `Tree` class with **11 methods**.

### 1. **`__init__`** (Constructor)
Creates a tree node with attributes:
- `value` – Stores the node's value.
- `left` – Points to the left subtree.
- `right` – Points to the right subtree.

### 2. **`isempty`**
Checks whether the current node is empty (i.e., its value is `None`).

### 3. **`isleaf`**
Determines if the current node is a **leaf** (i.e., both `left` and `right` are empty).

### 4. **`makeempty`**
Removes a **leaf node** by setting its value to `None`.  
Used in the deletion process.

### 5. **`copyright`**
Handles node deletion when the node has children.  
- If a node to be deleted **has only a right child**, its value is replaced with the right child’s value.  
- The right child’s children are promoted accordingly.

### 6. **`find`**
Searches for a given value in the BST and returns:
- `True` – If the value exists.
- `False` – If the value is not found.

### 7. **`insert`**
Inserts a new value into the BST while maintaining its ordering.

### 8. **`maxval`**
Finds the **maximum** value in the BST.

### 9. **`minval`**
Finds the **minimum** value in the BST.

### 10. **`delete`**
Deletes a value from the BST, using:
- `makeempty` (for leaf nodes).
- `copyright` (for nodes with children).

### 11. **`inorder`**
Performs an **in-order traversal**, returning a sorted list of values in **ascending order**.

## Time Complexity

| Operation   | Average Case | Worst Case (Unbalanced) |
|------------|-------------|------------------------|
| **Search**  | O(log n)    | O(n)                   |
| **Insert**  | O(log n)    | O(n)                   |
| **Delete**  | O(log n)    | O(n)                   |

### Why is balancing important?
For optimal performance, BST operations should run in **O(log n)**. However, if the tree becomes **skewed** (all nodes leaning left or right), operations degrade to **O(n)**.

To prevent skewness, **AVL Trees (self-balancing BSTs)** can be used to maintain balance automatically.

---

### 🚀 Contributions & Enhancements  
Feel free to contribute improvements, such as adding **AVL tree balancing** or **additional traversal methods**!

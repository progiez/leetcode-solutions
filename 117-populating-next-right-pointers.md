# 117. Populating Next Right Pointers in Each Node II LeetCode Solution

In this guide, you will get 117. Populating Next Right Pointers in Each Node II LeetCode Solution with the best time and space complexity. The solution to Populating Next Right Pointers in Each Node II problem is provided in various programming languages like C++, Java, and Python. This will be helpful for you if you are preparing for placements, hackathons, interviews, or practice purposes. The solutions provided here are very easy to follow and include detailed explanations.

## Table of Contents

1. [Problem Statement](#problem-statement)
2. [Complexity Analysis](#complexity-analysis)
3. [C++ Solution](#c-solution)
4. [Java Solution](#java-solution)
5. [Python Solution](#python-solution)
6. [Additional Resources](#additional-resources)

---

## 🧩 Problem Statement

Given a binary tree

```cpp
struct Node {
  int val;
  Node *left;
  Node *right;
  Node *next;
}
```

Populate each next pointer to point to its next right node. If there is no next right node, the next pointer should be set to NULL.  
Initially, all next pointers are set to NULL.

### Example 1:
Input: root = [1,2,3,4,5,null,7]  
Output: [1,#,2,3,#,4,5,7,#]  
Explanation: Given the above binary tree (Figure A), your function should populate each next pointer to point to its next right node, just like in Figure B. The serialized output is in level order as connected by the next pointers, with ‘#’ signifying the end of each level.

### Example 2:
Input: root = []  
Output: []

### Constraints:
- The number of nodes in the tree is in the range [0, 6000].
- -100 <= Node.val <= 100

### Follow-up:
You may only use constant extra space.  
The recursive approach is fine. You may assume implicit stack space does not count as extra space for this problem.

---

## 📊 Complexity Analysis

- **Time Complexity:** O(n)
- **Space Complexity:** O(1)

---

## 💻 C++ Solution
```cpp
class Solution {
 public:
  Node* connect(Node* root) {
    Node* node = root;  // the node that is above the current needling

    while (node != nullptr) {
      Node dummy(0);  // the dummy node before needling
      // Needle the children of the node.
      for (Node* needle = &dummy; node; node = node->next) {
        if (node->left != nullptr) {
```

👉 [See full code here](https://progiez.com/117-populating-next-right-pointers-in-each-node-ii-leetcode-solution)

---

## ☕ Java Solution
```java
class Solution {
  public Node connect(Node root) {
    Node node = root; // the node that is above the current needling

    while (node != null) {
      Node dummy = new Node(); // a dummy node before needling
                               // Needle the children of the node.
      for (Node needle = dummy; node != null; node = node.next) {
        if (node.left != null) {
          needle.next = node.left;
```

👉 [See full code here](https://progiez.com/117-populating-next-right-pointers-in-each-node-ii-leetcode-solution)

---

## 🐍 Python Solution
```python
class Solution:
  def connect(self, root: 'Node') -> 'Node':
    node = root  # the node that is above the current needling

    while node:
      dummy = Node(0)  # a dummy node before needling
      # Needle the children of the node.
      needle = dummy
      while node:
        if node.left:
          needle.next = node.left
```

👉 [See full code here](https://progiez.com/117-populating-next-right-pointers-in-each-node-ii-leetcode-solution)

---

## 📚 Additional Resources

- [🔗 Explore all LeetCode problem solutions at Progiez](https://progiez.com/leetcode-solutions)
- [🔗 Explore all problems on LeetCode website](https://leetcode.com/problemset/)
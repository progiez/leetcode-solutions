

# 117. Populating Next Right Pointers in Each Node II LeetCode Solution

![117. Populating Next Right Pointers in Each Node II LeetCode Solution](https://progiez.com/wp-content/uploads/2025/02/117-Populating-Next-Right-Pointers-in-Each-Node-II-LeetCode-Problem-Solution.webp)

In this guide, you will get 117. Populating Next Right Pointers in Each Node II LeetCode Solution with the best time and space complexity. The solution to Populating Next Right Pointers in Each Node II problem is provided in various programming languages like C++, Java, and Python. This will be helpful for you if you are preparing for placements, hackathons, interviews, or practice purposes. The solutions provided here are very easy to follow and include detailed explanations.

## Table of Contents
- [Problem Statement](#problem-statement)
- [Complexity Analysis](#complexity-analysis)
- [C++ Solution](#c-solution)
- [Java Solution](#java-solution)
- [Python Solution](#python-solution)
- [Additional Resources](#additional-resources)
- [FAQ](#-frequently-asked-questions-faq)

---

## Problem Statement

Given a binary tree:

```cpp
struct Node {
  int val;
  Node *left;
  Node *right;
  Node *next;
}
```

Populate each next pointer to point to its next right node. If there is no next right node, the next pointer should be set to `NULL`. Initially, all next pointers are set to `NULL`.

### Example 1:
**Input:** root = [1,2,3,4,5,null,7]  
**Output:** [1,#,2,3,#,4,5,7,#]  
**Explanation:** The function should connect nodes in the same level using the `next` pointer.

### Example 2:
**Input:** root = []  
**Output:** []

### Constraints:
- The number of nodes in the tree is in the range [0, 6000]
- `-100 <= Node.val <= 100`

### Follow-up:
You may only use constant extra space. The recursive approach is fine. Implicit stack space is allowed.

---

## Complexity Analysis

- **Time Complexity:** O(n)
- **Space Complexity:** O(1)

---

## C++ Solution

```cpp
class Solution {
 public:
  Node* connect(Node* root) {
    Node* node = root;  // the node that is above the current needling

    while (node != nullptr) {
      Node dummy(0);  // the dummy node before needling
      // Needle the children of the node.
      for (Node* needle = &dummy node; node = node->next) {
        if (node->left != nullptr) {
... 
```
 [See full code ](https://progiez.com/117-populating-next-right-pointers-in-each-node-ii-leetcode-solution)

---

## Java Solution

```java
class Solution {
  public Node connect(Node root) {
    Node node = root;

    while (node != null) {
      Node dummy = new Node();
      for (Node needle = dummy; node != null; node = node.next) {
        if (node.left != null) {
          needle.next = node.left;
... 
```
 [See full code ](https://progiez.com/117-populating-next-right-pointers-in-each-node-ii-leetcode-solution)
---

## Python Solution

```python
class Solution:
  def connect(self, root: 'Node') -> 'Node':
    node = root

    while node:
      dummy = Node(0)
      needle = dummy
      while node:
        if node.left:
          needle.next = node.left
... 
```
 [See full code ](https://progiez.com/117-populating-next-right-pointers-in-each-node-ii-leetcode-solution)

---

## Additional Resources

- 🔗 [Explore all LeetCode solutions on Progiez](https://progiez.com/leetcode-solutions)
- 🔗 [LeetCode Problem Set](https://leetcode.com/problemset/)

---

## ❓ Frequently Asked Questions (FAQ)

### What is the main challenge of LeetCode 117?
The challenge is connecting `next` pointers in a binary tree using **constant extra space**.

### Can I use a queue for this solution?
Yes, but it will require O(n) space. The optimal solution avoids it by using existing `next` pointers.

### Is recursion allowed?
Yes. The stack space used in recursion is acceptable as per the problem statement.

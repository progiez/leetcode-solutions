# LeetCode 100. Same Tree LeetCode Solution

🔗 [View full solution with explanation here](https://progiez.com/100-same-tree-leetcode-solution)

---
### 🚀 Python

```python
class Solution:
  def isSameTree(self, p: TreeNode | None, q: TreeNode | None) -> bool:
    if not p or not q:
      return p == q
    return (p.val == q.val and
            self.isSameTree(p.left, q.left) and
            self.isSameTree(p.right, q.right)) # code by PROGIEZ
```

---

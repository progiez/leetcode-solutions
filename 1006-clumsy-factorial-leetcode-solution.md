# LeetCode 1006. Clumsy Factorial LeetCode Solution

🔗 [View full solution with explanation here](https://progiez.com/1006-clumsy-factorial-leetcode-solution)

---
### 🚀 Python

```python
class Solution:
  def clumsy(self, n: int) -> int:
    if n == 1:
      return 1
    if n == 2:
      return 2
    if n == 3:
      return 6
    if n == 4:
      return 7
    if n % 4 == 1:
      return n + 2
    if n % 4 == 2:
      return n + 2
    if n % 4 == 3:
      return n - 1
    return n + 1 # code by PROGIEZ
```

---

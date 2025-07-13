# LeetCode 1002. Find Common Characters LeetCode Solution

🔗 [View full solution with explanation here](https://progiez.com/1002-find-common-characters-leetcode-solution)

---
### 🚀 Python

```python
class Solution:
  def commonChars(self, words: list[str]) -> list[str]:
    return functools.reduce(lambda a, b: a & b,
                            map(collections.Counter, words)).elements() # code by PROGIEZ
```

---

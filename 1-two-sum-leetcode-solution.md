# LeetCode 1. Two Sum LeetCode Solution

🔗 [View full solution with explanation here](https://progiez.com/1-two-sum-leetcode-solution)

---
### 🚀 Python

```python
class Solution:
  def twoSum(self, nums: list[int], target: int) -> list[int]:
    numToIndex = {}

    for i, num in enumerate(nums):
      if target - num in numToIndex:
        return numToIndex[target - num], i
      numToIndex[num] = i #code by PROGIEZ
```

---
